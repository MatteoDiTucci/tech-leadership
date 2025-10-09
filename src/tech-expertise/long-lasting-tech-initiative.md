# Long lasting tech initiative

## Problem
Several weeks are set aside for a tech initiative.  
The changes are invisible outside the codebase, so it is hard to define success and communicate progress to stakeholders.

## Context
Examples of long-lasting tech initiatives are:
- refactoring an e-commerce cart logic as it is too complex and slow
- migrating the integration layer with a content management system
- improve the continuous deployment pipeline as it is too slow

## Solution
Treat tech initiatives exactly like products ones. Artifacts are different, but the lifecycle is the same.  
Stakeholders can be inside and outside the team, sometimes are simply the engineers maintaining a system.

### Problem definition
Get the stakeholders together to define:
- what is the problem
- who is impacting
- what are the consequences
- initial risk, assumption, issues, dependencies (RAIDs)

### Analysis
Analyze the problem and compare different solutions.  
Leverage technical spikes to update the RAIDs.  
If the problem is complex rather than complicated, start from anywhere and course correct as more information is gained.

### Definition of success
The definition of success must be codified in artifacts accessible to everybody and that can evolve with time.
For example:
- Current state and target state of a system in the form of diagrams
- Observability dashboard with key metrics (e.g. performance, number of errors, number of dependencies, number of invocations, etc.)

This must be done as the very first user story of the initiative.

### Communicate progress
The artifacts that define success reflects the progress of the initiative so far.  
Ideally this is automatically shown, for instance in the case of observability dashboards.  
Other times, they need to be updated manually, like with architecture diagrams.

## Notes
Codifying the definition of success in shared and evolving artifacts has two benefits.  
The most important one is exposing a shared mental model across the engineers working on the initiative.  
Secondly, it is an effective way to communicate with stakeholders.