<!-- cSpell:ignore SDLC -->

# Software Development Life Cycle (SDLC)

## Phases

1. Requirements & Analysis
    * Performed by product owners and qualified team members
    * In-house experts should be involved where possible, directing people at best practices
    * What problem does the software near to solve?
        * What and who are the challenges, requirements, cultural constraints and stakeholders?
    * How will the software fit into their current infrastructure?
        * Current technologies used (no point deploying a MACOS focused application if they only run Windows etc)
        * Identify IT process and road-map
    * Identify the desired user experience
        * Should the software be feature rich?
        * How many users does the software need to support?
        * How will it scale?
    * How will the above all be tested to ensure it is meeting the customers requirements?

2. Design
    * Take into consideration the customers requirements identified in step 1
    * Usually completed by software architects
    * Proof-of-concept (POC) happens here
    * Classically, two documents are created; High-Level Design (HLD) and Low-Level Design (LLD)
        * HLD 
            * 10,000 foot view
            * Any technical language is avoided here, where possible
            * General description of the architecture, components and relationships between one another
        * LLD
            * Describes components, protocols and how they are used to communicate within a given software.
    * This is typically avoided in Agile.
        
3. Implementation
    * Takes high and level designs and used them as input to create a given software
    * Often referred to as 'coding' or 'development' phase
    * Typically, test engineers now begin writing their testing plan
    * At the end of this phase, the software is ready for in-depth testing
        * This can be manual or automated (modern software is automated)

4. Testing
    * Takes implementation phase as input
    * Software is installed in an isolated testing environment
    * Test plan is followed, which outlines every single test which has been completed, both functionality and technically
        * Common technical tests
            * Integration testing
            * Performance testing
            * Security testing
    * When tests don't pass, bugs are logged and passed back to developers - once fixed, they are tested again
    * Once software is 'bug free', the software is ready for production

5. Deployment
    * Take the 'bug free' software from testing as input
    * Software is deployed in a production environment, if no issues; product manager and architects decide if the software is ready to be released
    * At the end of this phase, software is pushed to customers and end users

6. Maintenance
    * Support is provided via BAU functions
    * Bugs which are found in production are fixed
    * Software improvements are conducted
    * Should significant software improvements be required, the SDLC is completed again