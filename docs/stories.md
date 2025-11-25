# User Stories

The following user stories are in this page:

1. [Referral Partner Job Application](#referral-partner-job-application)

## Referral Partner Job Application

```mermaid
sequenceDiagram
    actor O as Referral Partner
    participant P as Platform
    actor S as Seeker

    O->>P: 1. Push Available Jobs (via API/Form)
    S->>P: 2. Search Jobs
    P->>P: 3. Match Jobs to Seeker Profile
    P->>S: 4. Display Matching Jobs
    S->>P: 5. Filter Jobs (optionally)
    S->>P: 6. Clicks 'Apply' Button
    P->>O: 7. Redirect to Partner website
```

**Links**:

1. [Datastore](structures.md)
