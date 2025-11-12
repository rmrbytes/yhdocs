### 💼 User Story: Partner Job Posting

*As a* **Partner Organisation**, *I want* to easily publish job opportunities, *so that* beneficiaries can apply directly, streamlining the hiring process.

```mermaid
sequenceDiagram
    actor O as Partner Org
    participant P as Platform
    participant DS as Data Store (Jobs)

    title Job Opportunity Creation Flow

    O->>P: 1. Send New Job Data (via API/Form)
    activate P
    P->>P: 2. Validate Job Data (Schema, Business Rules)
    P->>DS: 3. **WRITE**: Persist Job Record
    activate DS
    DS-->>P: 4. Confirmation (Job ID)
    deactivate DS
    P->>O: 5. Acknowledge Success (Job ID)
    deactivate P

    Note right of P: **Job is now available for matching.**
```

```mermaid
sequenceDiagram
    actor S as Seeker
    participant P as Platform
    participant DS as Data Store (Jobs/Apps)

    title Seeker Search and Application Flow

    S->>P: 1. Request Job Search/Feed
    activate P
    P->>DS: 2. **READ**: Retrieve Matched Job Listings
    activate DS
    DS-->>P: 3. Return Job Records
    deactivate DS
    
    P->>S: 4. Display Jobs Matching Needs
    S->>P: 5. Select Job & Click 'Apply' Link

    P->>P: 6. Validate Application Data
    P->>DS: 7. **WRITE**: Persist Application Record
    activate DS
    DS-->>P: 8. Confirmation (Application ID)
    deactivate DS
    P->>S: 9. Application Submission Confirmation
    deactivate P
```

```mermaid
sequenceDiagram
    actor O as Partner Org
    participant P as Platform
    actor S as Seeker # Renamed Beneficiary to Seeker

    O->>P: 1. Push Available Jobs (via API/Form)
    P->>P: 2. Filter & Match Jobs to Seeker Profiles
    P->>S: 3. Notify/Display Matching Jobs
    S->>P: 4. Clicks 'Apply' Link/Button
    P->>O: 5. Redirect/Forward Application Details
    P->>S: 6. Send Application Confirmation
```

```mermaid
sequenceDiagram
    actor O as Partner Org
    participant P as Platform
    actor S as Seeker
    actor F as Facilitator

    title Application and Verification Flow

    O->>P: 1. Job Published
    P->>S: 2. Match Notification Sent
    S->>P: 3. Seeker Submits Application
    
    Note right of S: Seeker's role is complete for now.
    
    P->>F: 4. Application Assigned for Review
    activate F
    F->>P: 5. Application Reviewed & Approved
    deactivate F
    
    P->>O: 6. Forward Approved Application
    P->>S: 7. Confirmation: Application Forwarded to Partner
```