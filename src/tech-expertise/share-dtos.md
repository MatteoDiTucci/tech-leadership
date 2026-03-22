# Share DTOs

## Problem
One service integrates with another one.  
To avoid regressions, contract testing is in place, for instance by using [Pact](https://docs.pact.io/).  
Engineers complain about the overhead of the contract testing harness and its maintenance.

## Context
The services are part of the same mono-repo, and they are written in the same language (e.g. Kotlin).  
Before contract testing, other solutions like API versioning were tried, but they implied even more maintenance and cognitive load.    

## Solution
Use the same DTOs (Data Transfer Objects) across the two services.    
Contract testing comes out of the box thanks to static types and it's verified at compile time.

### Where the DTOs live
Extract the DTOs from the producer service into a new folder which becomes a dependency of both the producer and consumer service.    
The new folder is just a new NPM package in the Javascript/TypeScript world, or a new Gradle project for Java/Kotlin.  
Whenever a change in the DTOs is made, the continuous deployment pipeline of both services is triggered.

### Expand and contract
The team of the producer service follows an expand-and-contract approach whenever a change in the DTOs is needed.    
This prevents regressions, big bang releases and planned downtime.

### Integration tests
Integration tests are still needed, but they are few and less complex.  
Usually they are just a simple happy path, plus the sad paths (e.g. 5XX, 4XX, timeout, connection error)

### Teams collaboration
As with contract testing, shared DTOs do not replace team collaboration.  
However, the feedback loop is faster and the overhead much lower.

