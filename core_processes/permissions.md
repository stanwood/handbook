# Permissions

## Background

We are facing four opposing principles when it comes to permissions.

1. Transparency and openness by default: Every team member should be able to read and change anything.
2. CD/CI: We need to save guard against breaking our continuous integration and deployment or production environments. 
3. Data protection: Private end user data (data bases, logs etc.) should be visible only to the smallest amount of people.
4. We do not want a bottleneck on permissions should an admin be not available.

## Principles

1. Data protection: Production data needs to be limited to the least amount of people possible and reviewed regularly.
2. Code, documentation etc: Every team member has read permissions.
3. Write permissions are closely guarded by our Head of Automation.
4. Contact Head of Automation via #operations in Slack if you need permissions.
5. Every admin permission should be with 3 people: CEO, Head of backend development, Head of Automation.