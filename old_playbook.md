# Old playbook

## 1. Goals
We have fun at work, free from stress and super productive.

This is our commands we gave ourselves. Please feel free to propose changes anytime.

Why we are doing this

We love to develop apps and websites which will be loved by users and clients.
Be transparent, dependable and plan-able for our client
Sync crowd testing and processes of our clients
Reduce miss-understandings and unclear tickets
Little crossfire from clients throughout the week
Little "jumping" in and out of projects

## 2. Staffing

Every project is staffed

With a project manager
One platform lead and one (or more) supporting frontend developer per platform
One (or more) backend developers

## 3. Timing and Budget

We practice Rapid Software Development. We aim to get apps to the store within 8 weeks after the briefing.

1w concept, wireframing and architecture

1w design, estimation, setup

6w coding (6 development cycles)

2w testing and fixing (by crowd and client)

Overhead: We should not spend more than

15% on project management (including the project manager!)

15% on fixing bugs after releasing the first beta

15% on QA and testing

15% on refactoring

## 4. The Development Process

Overview
Weekly meetings on Friday
PM's and Team Leads meet on Friday in appear.in/stanwood
Project leads go through Ready for Development and delegate tickets to the team
What did we achieve/not finish last week?
Which epics are we tackling this week?
Roadblocks: We raise them
But do not solve them.
Ticket life-cycle

PM creates a ticket, adds the relevant description and moved to Needs estimation
The ticket is added to Needs estimation and assigned to Project lead
Project lead review the ticket for sufficient information and estimates 1h/ 2h/ 4h
Once estimated, the ticket is moved to Needs approval and assigned to PM
PM approves, moves the ticket to Approved backlog and assigns the Project lead
On Friday, planned tickets for the following sprint are moved to Ready for development
The developer grabs a ticket in order of priority and moves to Working on
Once the ticket is complete, the developer creates a Pull Request assigned to the Project lead and moves the ticket to Code Review
Project lead approves the PR and assigns the ticket back to the developer
The developer moves the ticket to QA when the branch is merged to develop and assigns the QA manager to test the ticket
The QA approves the ticket and moves to Done; the according developer is assigned again
1. Development
Goal: Create a testable version by Friday.

Process

Developers: Implement and review all tickets from the development cycle ready for development till Thursday evening.

Project manager/ QA managers: Reviews all tickets on develop branch and report bugs.

Developers: Fix those bugs.

Project leads: Merges release to develop. Ensures develop is working and testable build deployed to TestFairy, 

Guidelines

The person responsible for the next step must be assigned to the ticket. i.e. when asking a question that question that blocks the ticket, please assign the person you asked.
Order of work: Weekly priority sent up until Monday; Priority: Critical, Status: Needs estimation, QA, Working on, Ready for Dev
2. Preparing development cycle Kickoff (Friday Afternoon)
QA manager

Reviews the feedback from testing and creates bugs tickets in Jira
Project manager

Distributes the test version to the client with release notes for review
Moves the weeks worth of tickets to Ready for Development before the kickoff meeting
Project lead

Add remaining estimation to tickets in Approved Backlog
Assigns tickets to project leads
3. QA
All tickets must receive

Code review
App/web: a functional review by the PM or QA manager
API: a functional review by front-end developer
Developer: After completion and testing himself off the ticket

Creates a pull request from his feature/hotfix/bugfix branch to develop branch
Assigns the Project leads for code review on GitHub
Project leads should code review and approve PR (reviewer is not merging PR)
Author of PR should merge his Pull Request
The author moves the ticket to QA
QA manager

In case the adjustments are approved, the ticket is moved to Done or
If more work is required, the ticket is moved back to Working on.
In both cases the according developer is assigned again 
In case of disagreements, ask the platform lead developer or Hannes.

4. Testing
The project lead developer creates a testable version on Friday EOD.
QA manager ships a testable build to the testing agency.
Each release will be tested by internal testers or our test agency over the weekend.
5. Client feedback
Client

Gives feedback over the course of the week (report bugs, request changes).
Is invited to do that directly in Jira.
Only tickets we get till Thursday can be part of the next development cycle.
Project manager

Reviews reproduce and details client requests/bug reports
Creates and details Epics, breaks down to Tasks
Coordinates priorities with the client on an ongoing basis
Project lead

Breaks down Tasks to sub-tasks for each platform and create API sub-task tickets
Estimates sub-tasks and tasks (if no subtasks)
Moves them to Needs approval

## 6. Releasing

Major/Minor Release

Monday-Wednesday. Thursday if critical
Hotfix Release

Hotfixes on a Friday, only if 10%+ users are affected
5. Types of Work
1. Epic
Group of tasks for a section in the app or topic.
Usually along the user flow in the app:
Design, Setup, Onboarding, Section 1, Section 2... , SDKs, Release
We try to finish epics entirely in a development cycles, so that the client and our testers can fully review that block.
Tickets that the client actively decides to not implement or fix are assigned to the Version Later to hide them out of the backlog in order to keep the backlog relevant and up to date.
Each Epic has a link to the github Documentation of that Epic.
Each Epic needs to have these elements:
Link to Zeplin designs
List of all UI elements
Where is the element getting its data from?
Where is the element writing it's data to
A list a and description of all interactions including
view did appear
data was loaded successfully
an error occurred when loading the data
all possible user interactions
2. Tasks
Has a link to the github documentation and Zeplin of that Task.

3. Sub-Tasks
Tasks are broken down by the project lead into Sub-Tasks.

Each task is assigned to one platform and one developer.
Tasks should not be more then 4 hours or split up into sub tasks
Tasks should be linked to corresponding tasks on other platforms.
MUST NOT have any requirements. Those belong into the Task
Estimation and logging of hours must happen on sub-tasks
4. Bugs
Clients and testers will create bug tickets. Bugs must contain:

Steps to reproduce
Screenshot (ideally from TestFairy)
Details on the device, OS, user and state
5. Client feedback
Clients, TestFairy and crashlytics will create issues as "Client Feedback". The project manager details and reproduces those before changing the type to "Bug".

6. Behavior regarding the client
Be nice, but not too nice. ;P

7. Unclear bugs
If we cannot reproduce a bug, we keep it in the Backlog as an "Unclear bug" assign the epic Later in the hope that someone can reproduce the bug.

## 6. Versioning
We use versions as an additional tool to organize tickets. The rules are loose.

However: When releasing a version to testers and clients a version must put together with all implemented tickets since the last release.

Major Releases

Are used sparingly. Only 1-2 major releases per year.

1.0, 2.0, 3.0

Minor Releases

Every release with features in it increments the second digit of the version

1.1, 2.3, 2.5

Hotfix Releases

Releases that merely fix bugs are incremented with the third digit of the version.

1.1.1, 2.3.4

Build numbers

We use automatically increasing build numbers from Bitrise. We use the same build version as Bitrise build #.

## 7. JIRA
Statuses
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

Guidelines
Discussions on issues belong in the comments in the issue.

## 8. Slack

Add a full name, picture, phone number and email
Username: @firstname if taken @nickname
Same on every other platform that we use.
#general Official stuff
#status Good morning, be-right-back, back, good night + what are you going to do today
#random GIFs, cat videos etc. to
#programming_X General programming talks and ask for help


When switching project, please ping both @pms in the project channel
When responding to todos in slack, please open a thread, use "On it {time}" (i.e. "On it in 1h") and "Done"/:white_check_mark:
Do not use threads on images and files.


Project channels starting with "_". All real-time discussion belongs there. acknowledge
Jira, Zeplin, Github, Bitrise post to the channel project channel.
No project talk in direct messages, please
As this is lost to the company.
When asking someone something, always use @username. Some developers are a member of dozens of channels and might miss your question.
BTW: Hannes is sometimes offline for a couple of hours when with a client. Best ask via comment in a Jira ticket then.

## 9. Zeplin

- All designs incl. assets are there.
- Designers: Upload files there and puts sketch file on GDrive
- Tickets live in Jira. But only for briefing and status.
- Commenting happens in Zeplin
- Upload a photo and an profile picture to Zeplin.
- Use the same handle as in slack.

**Naming convention for wires/mockups in Sketch**

- Digit 1: Epic
- Digit 2: View
- Digit 3: Variant
example: 1.1.2 Onboarding - Welcome Screen - Disabled

## 10. InVision

- Clickdummies for Userflow are there.
- export from Zeplin or directly from Sketch (search for Craft Plugin for Sketch to keep InVision in sync)
- Ninja trick: You get user flow for free, when adding Invision links. Make a screenshot, export to zeplin.

## 11. GitHub

We are using a custom Gitflow
2fa enabled
Branches

- master: deployed version
- develop: clean development version, for testing and beta release

- feature/SEL-12-awesome-feature
- hotfix/SEL-13-awesome-hotfix (fixing something in master)
- bugfix/SEL-14-awesome-bugfix(fixing)
Naming in Jira

- PR: SEL-123 {Ticket description}
- Branch: feature,hotfix,bugfix/SEL-123-{Ticket-description}
- Commit: SEL-123 {Ticket description} or SEL-123 {Commit description}
Guidelines

- Never push or merge directly into master and develop. Only reviewed pull requests are allowed to be merged.
- All feature/hotfix branches must be merged into the release branch via pull requests during the sprint
- Commit & push approx. all 3 hours
- Create pull request for every issue before you move to "QA" and assign the reviewer in github
- On go live: Lead merges to master, creates a tag and adds release notes from Jira, PM: 
Naming

In order for jira and toggl to auto import the code changes, we need to follow some naming conventions.

This greatly speeds up code review, QA and invoicing.

- Pull request: SEL-123 {Ticket description}
- Branch: feature,hotfix,bugfix/SEL-123-{ticket-description}
- Commit: SEL-123 {ticket description} or SEL-123 {commit description}
Code Review

What to look our for.

PR/CR Guidelines
Only use github comments for the initial and short discussions. Longer discussions should happen in Slack (public project channel). Report the results (+link) of that discussion in github.

When new libraries are added which have not been preapproved via the library list please include one of the following developers as a reviewer and describe why you used that particular library (and what possible pitfalls it has) in the PR description.

iOS: Ronan, Tal
Android: Miłosz, André, Sven
Web: Stefan
Documentation

Always keep the project doumentation up to date before moving your ticket to QA https://github.com/stanwood/Documentation

- Update when putting a ticket on code review
- Branch master: Docs for live version
- Develop branches: develop/{PROJECT ID}
- Feature branches: feature/{PROJECT ID}/{description}
- Create pull requests similar to the original code base
- Merge to master on go live and create a tag
We document EPICs and Tasks in that repo and only link from Jira tickets.

- links to design (zeplin) 
- "Task", i.e. "I as a use want to do XYZ."
- list of all UI elements, including
   - source of the data (static, firebase config, API, calculated) with links to documentation
   - list of all UI interactions (tap, long tap, flick, pinch, zoom, rotation) and resulting behaviour
   - broken by status (different behaviour for i.e. logged or premium users)

## 12. Bitrise

- master and develop must always build
- master always deploys to App Stores or production web server
- develop deploys to clients Monday 9am
- Clients feedback come to jira via TestFairy feedback tool

## 13. Time Tracking

Working hours

Totally up to you, but make it transparent to the project team, leads, and Hannes.
Public holidays and vacations: Please use the Holiday calendar. A 4-week head start would be cool, so Hannes and the leads can plan the projects.
Check with the PM that we have no releases or major events planned during that time.
Make sure to answer all messages in slack at least within 1h during 10:00 and 18:00 CET
Post in #status, should you be afk for more than 1 h during 10:00 and 18:00 CET
We get paid by the hour. Our clients honour us with a huge amount of trust - in return we give them total transparency.

Use the jira ticket ID and a description, i.e. LEN-01 My awesome new feature
Assign a project.
Best do it realtime. Hint: Use toggl jira chrome extension - Book non-ticket project work on the General Task of the project, i.e. merging, calls, estimates, internal communications, deployment, etc'.
Book non-project work on project Travel & Admin. Try to book as much project hours as possible.
Send your invoice at the beginning of the following month no later than the 2nd day of that month. Hannes will pay you the following Monday.

## 14. Unit and UI testing

We do not follow TDD on front end dev. In our rapid and agile approach we would spent too much time on writing tests that would become obsolete too fast.
We use unit tests on logic and all data model initializers and JSON parsers.
WORK IN PROGRESS: We will start automated UI on all our apps in the future.

## 15. Other

Split into documents per tool
Slack: "Holiday status"
Process: Reporting overruns
Process: Computers should be english
Process: Masterclases
Toggl: Logging non-ticket work
Slack: Use threads
Process: How to get permissions
Process: Adding flight times
Policy: Logging travel and workshop times
Policy: Always build proxies
Policy: Third party frameworks
Policy: Sharing photos from company events
Policy: Travel booking and expensing
Policy: Hardware Expensing
Policy: Transparency
People: Compensation
People: Recruiters
Policy: Friendliness, no-gender, tolerance, egg-plant
Legal: NDA & Data processing agreements for freelancers
Policy: Hiring freelancers vs. full time employees
Policy: Docusign for contracts
Policy: Data protection by default
Invoicing: Required fields on an invoice, deadlines and template

## 16. Roles

stanwood Roles
Team Lead

Project managers  [WIP]

Project Lead

Senior Developer

Mid-Level Developer [WIP]

stanwood Decision making and responsibilities
We need to have clear policies on

who can decide things
who needs to be asked for advice
who should propose
Of course we always strive to involve everyone in all discussions. 

Topic	Hannes	Team Leads	Heads	PMs	Developers	Examples
Coding practices	
Decide	

Advise	Switching to a new language, dependency management tool, 3rd party libs, coding style
Stack	Decide	Advise	Advise	

Native code vs. react/xamarin/vue/angular, Google App Engine, AWS, Python vs. Node.js, Firebase vs. Azure
Tools	Decide	
Advise	

Github vs. Confluence, Slack vs. Hipchat, CD/CI Tools
Internal frameworks	Decide	Advise	

Propose	Analytics, Rating, Core...
Recruiting	Advise	Decide	

Propose	Finding and hiring new devs
Training	Advise	Decide	

Advise	Masterclasses, pair programming, udemy courses
Personal development	Advise	Decide	


Leadership training, language classes, mentoring

Initial project staffing	Advise	Decide	
Advise	

Ongoing project staffing	Decide	Advise	
Advise	

Contract extension	Advise	Decide	


Freelancers (1x per year), full-time employees after a trial period
Promotions	Advice	Decide	


Mid > Senior > Project lead


Project Development decision process
who can decide things during project development
who needs to be asked for advice


Topic	PM	Project Lead	Senior/Mid Developer	Examples
Ticket description	Implement	Review	

Estimation	
Decide	

Creating subtasks	
Refine	Advice	
Push back on complexity	Advice	Advice	

Release dates	Refine	Advice	

Delegating tickets	
Decide	

Architecture	
Enforce	Implement	
Review code	
Review	

## Project managers

Order of priorities:

1. Client Communication
Keep client informed about progress and blockers 3x per week.
React within 15 minutes to calls.*
React within 1 hour to emails.*
Create tickets to all issues raised within one day.*
* During business hours.

2. Jira Hygiene
Every morning: 

zero the inbox
ping project leads to estimate - if ticket update > 24h
ping assignee - if ticket update > 1w
Ensure:

tickets are well described
documentation regarding that ticket is up to date
everything discussed in Slack is synced back to Jira
3. Internal communication
Keep Hannes and all devs up to date of milestones, next milestones, of the pressing issues, blockers and goals 3x per week.
Update on Friday till 15:00.

4. Fill backlog
Every Friday: Grab the client and fill the backlog of the team 20h-30h / full time dev

5. Keep documentation and Zeplin up to date
6. Upselling
Suggest features and improvements to clients.

## Team lead

Define developer recruitments standards
Interview and recruit new developers
Coordinate project roster
Aim to spread project across the team and to keep a refresh cycle.
Make sure the team is well mixed and get the chance to work with everyone.
Push the boundaries of Platform OS capabilities
Team framework responsibilities, evangelist
Set team member per framework
Oversee the team development, and policy implementation
Work alongside Head of Platform Architecture to define and improve a global architecture
Plan and manage 3 annual workshops
Ask developers for topics*
The lead would organise the workshop, topic etc.
Liaise with the Head of Engineering to make sure platforms aligned
Training
Workshops and master classes
Feedback process: Individualise training per developer
Pair programming
Work alongside the PM's to utilize the best working environment
Support the team with any issues they have, and identify strength and weakness.
Prepare and establish quarterly team review
Navigate and support project leads with ongoing projects.

## Project Lead

Share
User icon
Tal Zion
Last modified May 01, 2018


Responsibilities:
Single contact for PM's
Review ticket description
Enforce stanwood architecture
Estimate new tickets
Delegate the work to their supporting team
Code review


Project leads will oversee the project development, are the direct contact for PM's and will manage the team to meet best coding practice, release dates, and budget.

Responsibilities:
Be the single contact for PM's
Review ticket description
Enforce stanwood architecture
Estimate new tickets
Delegate the work to their supporting team
Code review
Single contact for PM's
During the project ongoing development, you will be the main contact for PM's:

Keep them up to date with current feature development
Inform of over budget tickets
Discuss release dates
Communication is key for the success of the project..

Review ticket description
Create subtasks if needed
Reject features due to complexity
Reject tickets that do not include all the information needed for implementation
Missing endpoints
Missing design
Bug tickets: missing Crashlytics link, steps to replicate, device information
Missing full description of requirements 
Enforce stanwood architecture
Making sure to enforce the architecture on all projects. 

Estimate new tickets
Break down tickets to subtasks if needed.

Delegate the work to their supporting team
As part of being a project lead, you will manage up to three active projects. You will spend 30% of your time and delegate most of the tickets to the supporting developer.

Code review
Making sure code review is done by stanwood best practice and follow the guidelines. PR/CR Guidelines

## Senior Developer

As Senior developers, you have significant experience in software development, knowledge of industry practices and you are the backbone of software development at stanwood.

Responsibilities:
Liaise with project leads
Implement stanwood architecture
Design and implement new features
Push back on features that add complexity
Ongoing bug fixes, and maintenance
Keep project documentation up to date
Maintain and manage existing code base
Liaise with project leads on new deadlines, and new features
Project leads are you main point of contacts discussing:

Feature implementation
Complexity
Budget
Release date
Implement stanwood architecture
Make sure the latest architecture is implemented

Design and implement new features
As a senior developer, you will do most of the heavy lifting during development.

Push back on features that add complexity
Push back on features that add complexity to the project lead. We are not here to solve every client feature request, but look for the quickest, and safest solution that support the code base. 

Ongoing bug fixes, and maintenance


Keep project documentation up to date
Work along side the project lead and update the documentation on a regular basis.

Maintain and manage existing code base
Make sure we are not adding technical debt when maintaining the code base. Should there be a case where the current code base do not support on going development, involve the project lead. 