

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