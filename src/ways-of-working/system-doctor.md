# System Doctor

## Problem
Production systems and internal tools require periodic maintenance and small improvements to remain healthy.  
Engineers neglect such tasks because they are focused on delivery.  
This results in degraded ways of working and lower quality for end users.   

## Context
Examples of periodic maintenance and small improvements:
- Dependencies updates
- Security vulnerability fixes
- Fixing flaky tests
- Improving continuous deployment pipeline speed
- Cleaning up observability dashboards
- Supporting other roles in their work (e.g. back-office automation, easier business configuration, etc.)
- Cross-functional checks (e.g. performance/SEO degradation)

Such tasks are ignored in favor of delivery because their individual impact is low.
However, their cumulative neglect increases feedback loops, making the whole company slower and less effective.

Individual engineers try to address this, but are usually overwhelmed.
Also, knowledge silos form as a result.

## Solution
Introduce a rotating role for all engineers responsible for periodic maintenance and small operational improvements.  

You can call this role system doctor, sheriff, firefighter, commander, etc.    
I personally prefer _system doctor_ or just _doctor_ because it doesn't imply incident response or purely firefighting work.

### Doctor's expectations
When an engineer is the doctor:
- No delivery work is allowed. If the engineer is driving a delivery task, they must immediately hand it over or pause it
- Work is collected in a single cross-team board: the doctor's board. The doctor can only pick up tasks from the doctor's board
- Each task has a due date to prioritize work

### Doctor's board boundaries
- Any task takes less than a day to complete. Anything larger is forwarded to teams' delivery boards for tech leads to discuss
- Any task belongs to a well-defined list of topics; anything else is rejected
- No bugs: the team that introduced them is responsible for fixing them
- Some tasks are recurring, ensuring a certain maintenance frequency.
  For example: dependencies updates, security vulnerability fixes, etc.
- Incident response is the responsibility of the on-call engineer, not the doctor

### Expected benefits
- Systems remain healthy
- The majority of engineers stay focused on their tech and product initiatives
- Engineers are pushed out of their comfort zone and work on all parts of the systems
- Fewer knowledge silos among engineers
- Other departments improve their ways of working