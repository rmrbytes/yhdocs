
# Business Requirement Specs YH 2.0.1

### Scope

to record the business requirements of the integrated youth hub platform.

### Modules being integrated

- youth-hub
- pathways
- partner-app

>  **P2E is not part of the integration** and will be treated as an external skills platform that is integrated with YH

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

# Context Diagram

```mermaid
flowchart TD
  O1[Job Providers]
  FA(Field Agents)
  Skill[Skill Providers]
  P((YHU Platform))
  B[Beneficiary]
  V[Verifiers]
  M[Managers]

  O1 & FA --> |posts jobs| P
  FA --> |self-employment opportunities| P
  Skill --> |offer courses| P
  P -->|career & learning resources| B 
  P --> |verify credentials| V
  P --> |Monitor| M
```


==The entity names above will be changed after confirmation of glossary and terms==

## Dig Deep

1. [Pathways](pathways.md)
2. [Data Structures](structures.md)
3. [Enums](enums.md)
4. [Glossary](glossary.md)

