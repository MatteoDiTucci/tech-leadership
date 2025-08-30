# Problem
How to communicate in a software delivery team to make sure:
- Everybody is aligned
- Feedback loop is short
- People have focused time

# Context
- Cross-functional team
- Full remote with overlapping time zones
- Communication tools available:
    - Slack (chat)
    - Asana (project management tool)
    - Google Meet (synchronous meeting)
    - Gmail (email)

# Solution
### Slack
- Urgent questions only
    - Examples: you are stuck, and you can't do anything else without relevant context switching
- Avoid direct messages
    - Even for direct questions, use the team channel as this irradiates information
    - Examples: clarify a requirement which is blocking a user story
- No tagging
    - Use "@ person", "@ channel", "@ here" only for urgent topics
    - Examples: production incidents, you need an answer within an hour
    - Team members are expected to skim through the team channel every couple of hours to triage and reply
- Channels follow a convention
    - [department]-[team-name]
    - Examples: #tech-bunny
- Messages follow a convention
    - The first line is the summary
    - If asking a direct question, put people names on top
    - Examples:
      "[Go-live: countries timeline]
      _Hey Nick_,
      Are we good to launch in Italy after France?"
- Single source of truth
    - OK to have dedicated channels for roles, but some noise is better than overspecialized channels
    - Have a dedicated channel for external stakeholders to ask for help

### Asana
- Definition of done
    - Single source of truth for what needs to be done
    - Crystallize any decision-making
    - The above holds for both product and tech initiatives
- Important, but not urgent
    - Use Slack for urgent communication
    - Team members are expected to skim through the notifications twice a day to triage and reply
    - Bring back decision-making from Slack and meetings to the Project Management tool
- Every initiative has its on board
    - This board clarifies what has been done and what is left to do
    - Tickets are organized in 3 sections: problem definition, analysis, delivery
    - Delivery section can be broken down into multiple sections, one per go-live
- Team delivery board
    - It visualizes the work in progress or soon to be picked up (1-2 weeks)
    - 4 columns: in-refinement, next, in-progress, done
    - When ready to be refined, a ticket from an initiative board, is added to the team delivery board
    - Every ticket is assigned to a person
    - One person can't have more than 1 ticket in progress


### Google Meet
- Only for synchronous collaboration
    - Examples: initiative kick-off, retrospective
- Use the right tool
    - Examples: Tuple for pair programming, Miro for drawing
- Reduce recurring meetings
    - Examples: move user story refinement to async, is standup really needed?
- Keep meetings short and focused
    - Smallest audience possible
    - Organizer is responsible for time keeping
    - Expected outcomes and agenda in meetings invites
    - Everybody's calendar is up to date, so anyone invited to a meeting can change the date-time if needed


### Gmail
- Only to communicate with people outside the company

## Notes
### Everybody needs focused time, managers too
- Decision-making requires focus
- Bad decisions by an engineering manager are more harmful than those made by an engineer
- Sorry [Paul Graham](https://paulgraham.com/makersschedule.html)

### Repetition is key
- Have 1 goal at time for the team
- Use repetition in written and verbal communications to remind what the current goal is
- This simplifies decision-making and prioritization at any level

## Credits
Thanks to David Swallow, who insisted for no direct Slack tagging in our team. We were skeptical, now we love it.