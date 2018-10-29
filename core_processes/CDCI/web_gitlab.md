## Web Gitlab

# Gitlab CDCI Web Guidelines

## Steps

### 0. Get the project deploy from your local terminal

- Install and configure firebase CLI https://firebase.google.com/docs/cli/
- Make sure to use the correct folder for deployment, i.e. /dist /public

### 1. Set up variables in settings/cd_ci

- FIREBASE_PROJECT_DEVELOP
- FIREBASE_PROJECT_PRODUCTION
- FIREBASE_PROJECT_STAGE
- FIREBASE_TOKEN

The central token is in 1password

Do not protect them. If you do, they will not be passed to the dev and stage branch.

### 2. Set up CDCD file in root

Add a `.gitlab-ci.yml` file on develop, then merge down to stage and master. 

Be careful! This will deploy to production.

```
image: node:latest

deploy_review:
  stage: test
  environment: develop
  only:
    - develop
  script:
    - {ADD YOUR YOUR BUILD STEPS HERE}
    - npm install -g firebase-tools
    - firebase deploy --token=$FIREBASE_TOKEN --non-interactive --project=$FIREBASE_PROJECT_DEVELOP --only hosting

deploy_stage:
  stage: deploy
  environment: stage
  only:
    - stage
  script:
    - {ADD YOUR YOUR BUILD STEPS HERE}
    - npm install -g firebase-tools
    - firebase deploy --token=$FIREBASE_TOKEN --non-interactive --project=$FIREBASE_PROJECT_STAGE --only hosting
    
deploy_production:
  stage: deploy
  environment: production
  only:
    - master
  script:
    - {ADD YOUR YOUR BUILD STEPS HERE}
    - npm install -g firebase-tools
    - firebase deploy --token=$FIREBASE_TOKEN --non-interactive --project=FIREBASE_PROJECT_PRODUCTION --only hosting
```

### 3. Todos

1. Use cached folders to speed up deployment time
2. Gitlab wants testing (develop) and deployment handled differently. Research how that is done.
3. Use centralised cdci file to save config time.
4. Which firebase token should we use?
5. Create artefacts. Ideally we can download a working snapshot from the build.
6. Review if all those steps are required or if we can skip some
	7. npm install -g npm@5.6.0
	8. npm install
	9. npm run build