# Developer Operations

## 1. Background

We love to develop apps and websites which will be loved by users and clients.

We want to be transparent and dependable for our client. We also want to sync crowd testing and processes of our clients as well as reduce miss-understandings and unclear tickets.

At last we want to limit crossfire from clients throughout the week and "jumping" in and out of projects.

## 2. Staffing

Every project is staffed

- With a project manager
- One platform lead and one (or more) supporting frontend developer per platform
- One (or more) backend developers

## 3. Timing and Budget

We practice Rapid Software Development. We aim to get apps to the store within 8 weeks after the briefing.

- 1w concept, wireframing and architecture
- 1w design, estimation, setup
- 6w coding (6 development cycles)
- 2w testing and fixing (by crowd and client)

Overhead: We should not spend more than

- 15% on project management (including the project manager!)
- 15% on fixing bugs after releasing the first beta
- 15% on QA and testing
- 15% on refactoring

## 4. The Development Process

### Weekly cycle

- Project manager move the weeks worth of tickets to `Ready for Development` before Friday noon.
- Weekly staffing and update meetings on Friday between project managers and team leads
	- What did we achieve/not finish last week?
	- Which epics are we tackling this week?
	- Roadblocks: We raise them. But do not solve them.
	- Solving staffing issues and bottlenecks
- After: Team and project leads go through `Ready for Development` and delegate tickets to the team
- Development
- Developers: Implement and review all tickets from the development cycle ready for development till Thursday evening.
- Project manager/QA managers: Reviews all tickets on develop branch and report bugs.
- Developers: Fix those bugs.
- Project leads ensure develop is working and testable build deployed to TestFairy
- QA manager review the feedback from testing agency and create bugs tickets in Jira.
- Project manager distributes the test version to the client with release notes for review

### Ticket life-cycle

- Project manager creates a ticket, adds the relevant description and moved to `Needs estimation` and assigned to Project lead
- Project lead reviews the ticket for sufficient information and estimates 1h/ 2h/ 4h
- Once estimated, the ticket is moved to `Needs approval` and assigned to project manager
- Project manager (or client) approves, moves the ticket to `Approved backlog` and assigns the project lead
- On Friday, planned tickets for the following sprint are moved to `Ready for development`
- The developer grabs an assigned ticket in order of priority and moves to `Working on`
- Once the ticket is complete, the developer creates a Pull Request assigned to the project lead and moves the ticket to `Code Review`
- Project lead approves the PR and assigns the ticket back to the developer
- The developer moves the ticket to `QA` when the branch is merged to develop and assigns the QA manager to test the ticket
- The QA approves the ticket and moves to Done; the original developer is assigned again
- The QA manager moves rejected tickets are moved to `Ready for development`

### Guidelines

The person responsible for the next step must be assigned to the ticket. i.e. when asking a question that question that blocks the ticket, please assign the person you asked.

Order of work: Weekly priority sent up until Monday; Priority: Critical, Status: Needs estimation, QA, Working on, Ready for Development

All tickets must receive

- Code review
- App/web: a functional review by the Project manager or QA manager
- API: a functional review by front-end developer

### Pull requests

- Developers creates a pull requests from their feature/hotfix/bugfix branch to develop branch.
- Assigns the Project leads for code review on GitHub.
- Project leads reviews code and approves PR (reviewer is not merging PR)
- Author of pull request merges to develop and moves the ticket to QA.

### Testing

The project lead developer creates a testable version on Friday EOD.

QA manager ships a testable build to the testing agency.
Each release will be tested by internal testers or our test agency over the weekend.

### Client feedback

Client give feedback over the course of the week (report bugs, adds request changes).
For that they are invited to do that directly in Jira.

Only tickets we get till Thursday can be part of the next development cycle.

Project managers review, reproduce and detail client requests/bug reports and creates and details Epics, breaks down to Tasks and coordinates priorities with the client on an ongoing basis.

The project lead breaks down Tasks to sub-tasks for each platform and create API sub-task tickete, estimates sub-tasks and tasks (if no subtasks) and moves them to `Needs approval`

## Release policy

### Major/Minor Release

Monday-Wednesday. Thursday if critical.
 
### Hotfix Release

Hotfixes on a Friday, only if 10%+ users are affected

### Major Releases

Are used sparingly. Only 1-2 major releases per year.

1.0, 2.0, 3.0

### Minor Releases

Every release with features in it increments the second digit of the version

1.1, 2.3, 2.5

### Hotfix Releases

Releases that merely fix bugs are incremented with the third digit of the version.

1.1.1, 2.3.4

### Build numbers

We use automatically increasing build numbers from Bitrise. We use the same build version as Bitrise build.