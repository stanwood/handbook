## Release Procedure Web Projects

### 1. During Development

During the week we merge feature/bugfix branches into `develop`.

The CDCI auto-deploys to the firebase.hosting develop environment.

**Responsibilities**

- @devs: Codes, creates PR and merges
- @project lead: Approves PR
- @qa: Test features on `develop`.

### 2. Creating a testable version

Thursday evening `develop` is merged into `stage` to have a stable environment for QA, test agency and client approval.

The CDCI auto-deploys to firebase.hosting stage environment.

**Responsibilities**

- @pm: Decides on time and date
- @qa: Gives green light
- @project lead: Merges
- QA: Do smoke testing
- Test agency: Smoke testing
- Client: Smoke testing and approval

### 3. Go Live

Between Monday and Wednesday we deploy to production by merging `stage` into `master`.

CDCDI auto-deploys to firebase.hosting production environment.

**Responsibilities**

- @pm: Decides on time and date.
- @qa: Give green light.
- @project lead: Merges.
- @qa: Do post-go-live smoke testing.