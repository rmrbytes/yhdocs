??? note ":material-database: Data Store: Referral Partner"
    <a id="ds_referral_partner"></a>

    These are organisations that upload available jobs and ask Seekers to apply on their website.

    ```yaml
    id: 
        type: string 
        auto_generated: true
    partner_name: 
        type:string
        required: true
    website: 
        type:url
    logo: 
        type: image
    industry:
        type: string
    rep_info:
        rep_name: 
            type: string
            required: true
        rep_email: 
            type: string # email
            required: true
        rep_phone: 
            type: string # phone
            required: true
        rep_designation: 
            type: string
            required: true   
    ```

??? note ":material-database: Data Store: Referral Job"
    <a id="ds_referral_partner"></a>

    These are jobs posted by Referral partners. Seekers will be redirected to the Partner website for application submission.

    ```yaml
    id: 
        type: string 
        auto_generated: true
    partner_name: 
        type: string
        derived: FK to referral parnter
    job_title: 
        type: string
        required: true
    job_company: 
        type: string
        required: true
    job_location: 
        type: string
        required: true
    job_description: 
        type: string
        addl: markdown_supported
    date_of_posting: 
        type: date
        required: true
    monthly_salary: 
        type: number
        required: true 
    mode_of_work: 
        type: enum 
    experience_required: # in years
        type:number
    job_link: 
        type: url 
    ```
    
    Links:

    1. [Enum: Mode of Work](/enums/#enums_mode_of_work)
