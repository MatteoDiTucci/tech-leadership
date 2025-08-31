# Lightweight Business Configuration

# Problem
An e-commerce has some commercial configuration to update every now and then.
For example: what products are in pre-sale, what products are under promotion, etc.

How to enable non-technical roles to update such configuration with minimal effort?

# Context
- Update frequency: once a day
- Data to change: a handful of products SKU or dates
- Existing systems:
    - Front-end app
    - Product catalog back-end app
    - Headless content management system (third party)
- Current path to prod:
    - Continuous Deployment
- Current solution:
    - Configuration is stored in code as a handful of JSON files inside the front-end app
    - For any configuration change, a support ticket to engineers is created

# Solution
Non-technical roles change configuration autonomously using GitHub web interface.
<img width="1596" height="333" alt="image" src="https://github.com/user-attachments/assets/7d232fb5-ed50-4efc-aadd-e7d0bab997b4" />

## Security
- Non-technical roles adhere to the same security practices as engineers (e.g. strong passwords, password manager, 2nd factor authentication, encrypted laptop filesystem, etc.)
- Non-technical roles have write privileges on the front-end app repository, but not admin ones

## Testing
- Unit tests over the JSON files cover against:
    - malformed JSON
    - content validation (e.g. pre-sale dates in the past)
    - business invariant violations (e.g. avoid duplicates)

## Failure and recovery
- If a non-technical role makes a mistake with a JSON file, then the Continuous Deployment pipeline breaks
- An engineer reverts the change and then reaches out to the author to fix the issue together

## Pros
- No need to create a dedicated system to handle the commercial configuration
- Network fault-tolerant: commercial configuration is embedded at build time
- Unit tests acting as a quality gateway before changes affects production
- Configuration changes versioned in git

## Cons
- Not custom validation possible in the GitHub web interface (e.g. invalid date format)
- Basic JSON file manipulation needed by non-technical roles
- Changes need to wait a handful of minutes to be deployed in production
- Non-technical roles need to create a GitHub account, per person


# Note

## Next iterations
- If the proposed JSON approach suffer from poor UX, the content management system is likely the next step
- If the business configuration grows in complexity, we have identified a standalone business subdomain. This requires its own back-end system with a UI to configure the changes

# Credits
- Erik Simon: for proposing custom extensions to the content management system as an interesting alternative
- Lukasz Plotnicki: for helping me to simplify the proposed solution without falling into security traps like locally forking the GitHub repo
