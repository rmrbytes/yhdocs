# Business Requirement Specs
<a id="index"></a>

!!! info markdown "About this Document"
    ### Scope 
    to record the business requirements of the integrated youth hub platform.

    ### Modules being integrated
    - youth-hub 
    - path-ways 
    - partner-app

    > p2e is not part of the integration

    ## Audience 
    - all business stake holders
    - product team
    - development vendors (later)

    ## Purposes

    1. **Business users**: 
        - to confirm user stories
        - to confirm data structures
        - to confirm actions and business rules

    2. **Product team**:
        - to help design site map
        - to build wireframes

    3. **Dev team**:
        - to help build mock.
        - as input for design specs


!!! info "Context Diagram"
    <a id="context_diagram">
    ```mermaid
    flowchart TD
        O1[Partners]
        FA(Field Agents)
        Skill(Skill Providers)
        P((YHU Platform))
        S[Seeker]
        V[Verifiers]
        M[Managers]
        
        O1 & FA --> |posts jobs| P
        FA --> |self-employment opportunities | P
        Skill --> |offer courses| P
        P -->|career & learning
        resources| S
        P --> | verify credentials| V
        P --> | Monitor| M
    ```


## Dig Deep

!!! info "Index"
    1. [User Stories](../stories)
    2. [Data Structures](../structures)
    3. [Enums](../enums)
    4. [Glossary](../glossary)
