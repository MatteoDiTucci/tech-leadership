# Next Quarter Planning

## Problem
Leadership wants to know the delivery timeline of the team for the next quarter:
- what will be delivered
- when it will be delivered

## Context
- Different stakeholders push for different initiatives
- The problem behind each initiative is clear, but the solution is not
- Cross-functional team

## Solution
- Assign a time appetite for each initiative until the whole quarter is covered
- At the end of an initiative time appetite, decide to either:
    - move to the next initiative, as planned
    - keep working on the current initiative and subtract the extra time appetite from an upcoming initiative

### Time appetite
Time appetite means the amount of weeks the team desire to work on an initiative.  
Time appetite only covers delivery, not planning (see later).  
The key idea is to deliver the best within a fixed time frame and then reassess global priorities.

### Small go-lives
The key for the time appetite approach is small go-lives.  
Small go-lives makes it easy to decide to move to the next initiative or rather stay on the current one.  
Even if an initiative has a small time appetite, something is always delivered to the stakeholders of interest. 

Continuous Deployment helps a lot, but it is not a necessary condition.
Small go-lives bring many nice side effects per se:
- Faster customer feedback
- Faster operational feedback (i.e. performance, bugs, observability, etc.)
- Reduced work in progress and cognitive load

### Planning while delivering
The planning of an initiative is done before its delivery.  
For planning we mean:
- problem definition
- solution definition
- risks, assumptions, issues and dependencies spiking and resolution
- scope slicing (i.e. scope defined for each small go-live)

The planning is performed by
- Product manager
- UX designer
- Engineer champion (i.e. the engineer who coordinates the others on the initiative)

The planning happens while delivering on another initiative:
- be mindful of the extra work for the people involved in planning
- the engineer championing the current initiative should not contribute to planning the next one

### Time appetite vs estimates
Time appetite reverses the classic approach with estimates where:
- by guessing effort, the team define the scope to be delivered in the quarter for each initiative
- Team is constantly late to deliver, or worse quality is cut to respect the timeline
- Stakeholders are frustrated as their initiatives are late or nothing is delivered at all


## Notes
My proposed solution is a lightweight version of the [Shape Up approach from Basecamp](https://basecamp.com/shapeup)