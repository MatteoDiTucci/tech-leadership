# Practice the interesting, automate the boring

## Problem
How to use Large Language Models (LLMs) to increase throughput without sacrificing learning.

## Context
Engineers use LLMs to code.
Code throughput increases, but knowledge retention decreases among engineers.  

Effects on [DORA metrics](https://dora.dev/guides/dora-metrics-four-keys/):
- increased deployment frequency (good)
- smaller lead time (good)
- higher mean time to recovery (bad)

Qualitative effects:
- shallower technical conversations
- engineers do not remember how they implemented the internals of a feature

## Solution
Do not use LLMs when practice is needed. Instead, use LLMs to automate routine tasks.   
The rule of thumb is: if something is boring, delegate it to a LLM. If something is still interesting, do it yourself.

### Learning requires practice
Learning requires repetition. Mental models strengthen and gain higher resolution with deliberate practice.  
Delegating a new skill to LLMs after doing it just a few times hinders learning.

### When to use LLM

#### Prototyping
Quickly building different prototypes to compare them, thus increasing the chance of making the right choice.    
Examples are: software architectures, UI mock-ups, hackathons, etc.

#### New instance of an existing feature
Implement a new instance of a very well established feature.  
For instance: yet another product list page for a new product category.

#### Refactoring at scale
Once the same refactoring has been done several times, and engineers move from _being comfortable doing it_ to _being bored by doing it_.

#### Simplifying information gathering
Explore documentation efficiently, reduce the initial cognitive load with new technologies (e.g. boilerplate code for external systems integration).

#### One time occurrences
When doing something we are not planning or interested in doing again in the future.    
For example, low impact internal tool (i.e. boring, not interesting).

### When not to use LLM

#### Practicing a new skill
If you are learning test driven development (TDD), don't let the LLM code.  
Ask for feedback to the LLM, especially if not pairing. Be mindful to weight and discuss the feedback with others more experienced.

### Spaced repetitions
Without practice, it is normal to become rusty even after having mastered something.  
We are back to a situation when doing something ourselves is interesting.  
Stop delegating to LLMs until it is boring again.


## Notes

### Not black and white
There is a difference between using LLMs to prompt your way through an entire feature, and using it to make a function more idiomatic in TypeScript.    
LLMs can act as a good sparring partner, or bring us to places where we would not like to be.  
They are not good or bad per se, we just need to learn when it is better to slow down or speed up.

### Engineering instead of vibe coding
The context size of each agent is key.  
Have one agent acting as a planner and multiple agents acting as builders.  
The builders must have very specific roles and perform very small tasks.
For instance, if doing TDD: one agent write the tests, one agent makes the tests pass, one agent refactors.  
Have a common initial prompt to specify coding conventions, testing strategy, tech principles, and cross-functional requirements.  
Each repository has a folder containing the above prompts. For mono-repo, this is per service.


# Credits
Thanks to Sebastian Roidl for the "Engineering instead of vibe coding" section.