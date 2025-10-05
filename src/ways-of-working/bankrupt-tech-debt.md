# Bankrupt tech debt

## Problem
- There is a board which is a graveyard of tech debt tickets.  
- Nobody knows what is in there and what it is important to work on.

## Context
- The tech debt board is shared across multiple teams
- Whenever tech debt is recognized, a new ticket is added to the board and forgotten
- Cyclically, some engineer tries to organize and prioritize the board, but soon it becomes stale again
- All engineers are responsible, which means nobody is responsible

## Solution
- Each engineer picks one tech debt ticket and champions it to completion within the next 2 weeks
- Declare bankruptcy on the tech debt board, as in: delete it and forget about it
- From now on, when planning a new initiative, any relevant tech debt is identified and worked on as part of the initiative itself

### When to work on tech debt
- Tech debt can be tackled before, during or after the go-live of an initiative: it does not matter
- What matters is that a new initiative cannot start until all tech debt of the previous one has been covered

### Tech debt vs deadlines
- It is fine to create new tech debt to respect a deadline
- However, the tech debt must be recouped before starting a new initiative

### How much tech debt
- Perfect is enemy of good: we do not need to completely remove all the tech debt related to an initiative
- However, after an initiative is completed, we need to be in a better state than before starting it
- If the remaining tech debt is relevant, it will soon pop up again as part of a new initiative

### Important tech debt can't be lost
- Do not fear to lose track of important tech debt because of declaring bankruptcy
- If a piece of tech debt is important, it will be evident as part of the analysis of a new initiative

### Tech debt is not tech work
- An initiative can be either product work or tech work
- Tech work is what is needed to keep systems operational, not matter if they are customer-facing or internal
- So tech work not tech debt, and it should be delivered mixed with product work through any given interval of time (e.g. 80/20 product/tech work split)

## Discarded solutions

#### Quarter tech debt
- Here tech debt is bankrupted at the end of each quarter
- We are back to the original problem. However, by setting an expiration date on, we do not cumulate stale tech debt forever
- This might be a good intermediate step before adopting the proposed solution

#### Tech debt board kept up to date
- There is a recurring meeting where all engineers or at least the tech leads go through the tech debt board and prioritize it
- This approach is very expensive in terms of time and cognitive load as the board keeps growing through time
- This is better than just having a graveyard tech board where nobody is responsible
- However, the lack of an expiration date makes it an ever-increasing burden for the responsible engineers

