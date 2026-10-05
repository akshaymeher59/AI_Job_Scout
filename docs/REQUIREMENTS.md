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