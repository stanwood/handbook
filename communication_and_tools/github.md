# GitHub

## Background

We use Github to host our code.

## Gitflow

We are using a custom Gitflow.

- master: deployed version
- develop: clean development version, for testing and beta release
- stage: merged from develop for testing

- feature/SEL-12-awesome-feature
- hotfix/SEL-13-awesome-hotfix (fixing something in master)
- bugfix/SEL-14-awesome-bugfix(fixing)
Naming in Jira

- PR: SEL-123 {Ticket description}
- Branch: feature,hotfix,bugfix/SEL-123-{Ticket-description}
- Commit: SEL-123 {Ticket description} or SEL-123 {Commit description}

## Guidelines

- Never push or merge directly into master and develop. Only reviewed pull requests are allowed to be merged.
- All feature/hotfix branches must be merged into the release branch via pull requests during the sprint
- Commit & push approx. all 3 hours
- Create pull request for every issue before you move to "Code Review" and assign the reviewer in github
- On go live: Lead merges to master, creates a tag and adds release notes from Jira, PM: 

## Naming

In order for jira and toggl to auto import the code changes, we need to follow some naming conventions.

This greatly speeds up code review, QA and invoicing.

- Pull request: SEL-123 {Ticket description}
- Branch: feature,hotfix,bugfix/SEL-123-{ticket-description}
- Commit: SEL-123 {ticket description} or SEL-123 {commit description}

## Code Review

What to look our for.

PR/CR Guidelines

Only use github comments for the initial and short discussions. Longer discussions should happen in Slack (public project channel). Report the results (+link) of that discussion in github.

When new libraries are added which have not been pre-approved via the library list please include one of the following developers as a reviewer and describe why you used that particular library (and what possible pitfalls it has) in the PR description.

iOS: Ronan, Tal

Android: Miłosz, André, Sven

Web: Stefan