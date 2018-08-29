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