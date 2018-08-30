# Jira

## Background
We use Jira as our central tool for organizing our development process around tickets.

## Types of Work

### 1. Epic

- Group of tasks for a section in the app or topic.
- Usually along the user flow in the app:
- Design, Setup, Onboarding, Section 1, Section 2... , SDKs, Release
- We try to finish epics entirely in a development cycles, so that the client and our testers can fully review that block.
- Tickets that the client actively decides to not implement or fix are assigned to the Version Later to hide them out of the backlog in order to keep the backlog relevant and up to date.
- Each Epic has a link to the github Documentation of that Epic.
- Each Epic needs to have these elements:
		- Link to Zeplin designs
		- List of all UI elements
			- Where is the element getting its data from?
			- Where is the element writing it's data to
		-A list a and description of all interactions including view did appear
		- data was loaded successfully
		- an error occurred when loading the data
	- all possible user interactions

### 2. Tasks

Has a link to the github documentation and Zeplin of that Task.

### 3. Sub-Tasks

Tasks are broken down by the project lead into Sub-Tasks.

Each task is assigned to one platform and one developer.
Tasks should not be more then 4 hours or split up into sub tasks
Tasks should be linked to corresponding tasks on other platforms.

MUST NOT have any requirements. Those belong into the Task
Estimation and logging of hours must happen on sub-tasks

### 4. Bugs

Clients and testers will create bug tickets. Bugs must contain:

- Steps to reproduce
- Screenshot (ideally from TestFairy)
- Details on the device, OS, user and state

### 5. Client feedback

Clients, TestFairy and crashlytics will create issues as "Client Feedback". The project manager details and reproduces those before changing the type to "Bug".

### 6. Unclear bugs
If we cannot reproduce a bug, we keep it in the Backlog as an "Unclear bug" assign the epic Later in the hope that someone can reproduce the bug.

## Versioning

We use versions as an additional tool to organize tickets. The rules are loose.

However: When releasing a version to testers and clients a version must put together with all implemented tickets since the last release.

## Statuses

[X. Statusname [Person in charge]: Description]

Inbox [PM]: Clients and tools dump stuff in here, project managers add details

Needs Estimation [Project Lead]: Developer adds an "Original Estimate". // Suggestion: [(developer_estimation * 1.5 )+ 15%(for Code Review)]

Needs Approval [Client or PM]: Clients approves/declines.

Approved Backlog [Project Lead]: Approved by client, but not ready to be taken by developer in this sprint

Ready for Development [Dev]: Sprint backlog, filled by the project manager. Developer takes ticket from there and moves to next status.

Working On [Dev]: Developer implements, (if UI-task: adds screenshots), assigns other dev to code review

Code Review [Dev]: reviewer approves, assigns author, author merges to dev, author moves to QA with QA-instructions

QA [PM or QA Manager]: Project managers: reviews or asks QA-Manager to review. if failed: Assigns back to author working on if approved: moves to client review (if no client: done)

Needs client review [Client]: Client approves/declines 10. Done [PM] (Won't fix [PM]: Tickets, that will not get solved and need no further attention) (Duplicate [PM]: Duplicates, need to be linked to the original first) Crashlytics Issues

PM should create a bug ticket and add the issues link in the description

PM should add a checklist with -Issue Closed

The developer should close the issue on Crashlytics once the bug has been fixed and the ticket is moved to Done

Prio: 'Blocker' We use this to indicate that we cannot proceed with a ticket due to something missing by someone else. i.e. an API to be finished or a design to be created.

The project manager reviews those blockers regularly to check, if the the constraint has been lifted.

### Guidelines

Discussions on issues belong in the comments in the issue. If something is discussed in slack or in a call, the project lead is responsible for summarising the decision on the ticket.