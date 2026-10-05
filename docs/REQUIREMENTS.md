# AI_Job_Scout Requirements

## User Workflow 1 — Create Job Search Profile

The user should be able to create a job search profile containing:

- Name
- Current/target role
- Years of experience
- Skills
- Preferred locations
- Work preference (remote/hybrid/on-site)
- Target job titles
- Resume

### Expected Result

The system stores the user's profile and uses it later
to find and evaluate relevant jobs.


## User Workflow 2 — Discover Jobs

The system should collect job listings from supported job sources.

For each job, the system should capture:

- Job title
- Company
- Location
- Work type
- Job description
- Required skills
- Experience requirements
- Job URL
- Source
- Posted date
- Discovered date

The system should normalize jobs from different sources into
a common format.

The system should detect duplicate job listings.

### Expected Result

The user can see jobs from different supported sources
in one place instead of manually searching each source.

## User Workflow 3 — AI Job Matching

The system should evaluate how well each discovered job matches
the user's job search profile.

The system should compare:

- Target role
- Years of experience
- Technical skills
- Job requirements
- Responsibilities
- Location preference
- Work preference

The system should produce:

- Match score
- Matching skills
- Missing skills
- Experience match
- Short explanation of the match
- Recommendation

The recommendation can be:

- Strong Match
- Potential Match
- Low Match

### Expected Result

The user should be able to quickly understand whether a job is
worth considering instead of manually reading every job description.

## User Workflow 4 — Save and Track Applications

The user should be able to save a job for later consideration.

When the user decides to apply, the system should allow them
to create an application record for that job.

The application should track:

- Job
- Company
- Application date
- Resume used
- Application status
- Notes
- Last updated date

### Application Status

The initial application statuses should be:

- Saved
- Ready to Apply
- Applied
- Assessment
- Interview
- Offer
- Rejected
- Withdrawn

The user should be able to update the status as the application
progresses.

### Expected Result

The user should have a single place to see all jobs they have
saved or applied to and the current status of each application.


## User Workflow 5 — Referral Discovery and Outreach

For a discovered job, the system should identify potential people
who may be able to help the user with a referral or provide relevant
information about the opportunity.

Potential contacts may include:

- Current employees of the hiring company
- Recruiters associated with the company
- Hiring managers
- Relevant engineering managers
- Former employees
- Professional connections
- Other relevant contacts

The system should associate potential contacts with the relevant
company and job where possible.

### Referral Opportunity

For each potential contact, the system should provide:

- Name
- Current role
- Company
- Professional profile/link
- Relationship/context if known
- Why the person may be relevant
- Referral opportunity score/recommendation

### Outreach Preparation

For a relevant job, AI_Job_Scout should help the user identify
potential referral connections and prepare personalized outreach.

The system should:

1. Identify relevant people associated with the hiring company,
   where the required information is available.

2. Show the user relevant contact information, including:
   - Name
   - Current job title
   - Company
   - LinkedIn profile
   - Relevance to the job
   - Potential referral relevance

3. Allow the user to select a contact.

4. Generate a personalized cold referral message using:
   - Candidate profile
   - Candidate skills and experience
   - Target job
   - Job description
   - Contact's role
   - Company
   - Known relationship or relevant context, when available

5. The generated message must not invent:
   - Relationships
   - Work experience
   - Skills
   - Achievements
   - Personal connections
   - Other candidate or contact information

6. Allow the user to:
   - Review the generated message
   - Edit the message
   - Copy the message
   - Open the contact's LinkedIn profile

7. The "Open LinkedIn + Message" action should redirect the user
   directly to the selected contact's LinkedIn profile.

8. AI_Job_Scout should not automatically send the LinkedIn message.
   The user manually sends the message through LinkedIn.

9. After the user sends the message, the user should be able to
   record the outreach in AI_Job_Scout.

10. The system should track:
    - Contact
    - Job
    - Outreach channel
    - Message
    - Outreach status
    - Sent date
    - Follow-up date
    - Response
    - Notes

### Outreach Status

The initial outreach statuses should be:

- Draft
- Ready to Send
- Sent
- Follow-up
- Replied
- Referral Received
- No Response
- Closed

### Expected Result

For every relevant job, the user should be able to discover
potential referral connections, generate a personalized referral
message, open the contact's LinkedIn profile directly, manually
send the message, and track the outreach and response inside
AI_Job_Scout.

### Outreach Channels

The initial system may support preparation and tracking for:

- LinkedIn
- Email

Actual message sending should require user approval and should use
supported/appropriate integrations or user-controlled actions.

### Expected Result

For a relevant job, the user should be able to discover potential
referral opportunities and quickly prepare personalized outreach
instead of manually searching for relevant people and writing every
message from scratch.


## User Workflow 6 — Resume and Application Preparation

The user should be able to use their existing resume and candidate
profile to prepare for a specific job.

For a selected job, the system should:

1. Analyze the job description.
2. Compare the job requirements with the candidate profile.
3. Identify relevant experience and skills.
4. Identify missing or weak requirements.
5. Suggest improvements to the candidate's resume for the specific job.
6. Generate a tailored resume version.
7. Generate a personalized cover letter.
8. Generate answers for common application questions when appropriate.

### AI Safety and Accuracy

The system must not invent:

- Work experience
- Companies
- Job titles
- Skills
- Achievements
- Certifications
- Education
- Metrics
- Projects

Generated content should be based only on information available
in the candidate's verified profile, resume, and user-provided data.

The user must be able to review and edit generated content before
using it in an application.

### Resume Versions

Each tailored resume should be stored as a separate version.

The system should record:

- Original resume
- Target job
- Generated resume
- Version
- Created date

### Expected Result

For a selected job, the user should be able to understand what
parts of their experience are relevant, identify gaps, and prepare
a job-specific resume and cover letter that they can review before
submitting the application.

## User Workflow 7 — Daily Automated Job Search

The system should automatically run job searches based on the user's
job search profile.

The scheduled job search should:

1. Start according to the user's configured schedule.
2. Collect new jobs from supported sources.
3. Normalize the job data.
4. Detect and remove duplicate jobs.
5. Store newly discovered jobs.
6. Analyze relevant job descriptions.
7. Match jobs against the user's profile.
8. Identify strong and potential matches.
9. Make newly matched jobs available on the user's dashboard.

### User Configuration

The user should be able to configure:

- Search frequency
- Preferred search time
- Target roles
- Preferred locations
- Remote/hybrid/on-site preference
- Other job search preferences

### Expected Result

The user should not need to manually search multiple job sources
every day.

AI_Job_Scout should automatically discover and organize relevant
new opportunities and present them on the user's dashboard.


# MVP Scope

## Included in MVP

### Candidate Profile

- Candidate profile
- Skills
- Experience
- Target roles
- Preferred locations
- Work preferences
- Resume

### Job Discovery

- Job collection from supported sources
- Job normalization
- Job deduplication
- Job storage
- Job search and filtering
- Original job/source link

### AI Job Intelligence

- Job description analysis
- Skill extraction
- Experience requirement extraction
- Candidate/job matching
- Match score
- Match explanation
- Skill-gap analysis

### Application Management

- Save jobs
- Mark jobs as ready to apply
- Track applications
- Application status
- Application notes
- Application history

### Resume and Application Preparation

- Resume analysis
- Job-specific resume recommendations
- Tailored resume generation
- Cover letter generation
- Application question assistance
- User review before using generated content

### Referral and Outreach

- Identify relevant potential contacts where supported data is available
- Show contact information and LinkedIn profile
- Referral relevance
- Generate personalized referral messages
- Copy message
- Redirect user to the contact's LinkedIn profile
- User manually sends the LinkedIn message
- Track outreach
- Track follow-ups and responses

### Daily Job Automation

- Scheduled job searches
- Automatic job collection
- Automatic processing
- Automatic matching
- New-job dashboard updates


## Not Included in MVP

The following are intentionally excluded from the first version:

- Automatic LinkedIn message sending
- Mass LinkedIn messaging
- Automatic application submission across arbitrary job portals
- Uncontrolled browser automation
- Scraping or bypassing platform restrictions
- Mobile application
- Kubernetes
- Microservices
- Kafka
- Complex autonomous multi-agent systems
- Advanced analytics
- Automatic recruiter communication
- Automatic interview scheduling