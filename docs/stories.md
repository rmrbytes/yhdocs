!!! info "Story: Referral Partner Job Application"
    <a id="referral-partner-job-application">
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

    Links:

    1. [Datastore: Referral Partner](../structures/#ds_referral_partner)
    2. [Datastore: Referral Jobs](../structures/#ds_referral_jobs)