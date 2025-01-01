
# SW3.0 Job Matching System

## Overview

The **SW3.0 Job Matching System** leverages the power of the ChatGPT 3.5 Turbo model to automate the job matching process. Designed for today’s competitive job market, this system identifies job opportunities that align closely with a user’s resume and skillset. If gaps in skills or experience exist, the system provides actionable recommendations. When no gaps are identified, users are encouraged to apply directly to roles deemed a perfect match.

---

## Data Preparation

This project includes two Python scripts for data collection and preparation:

1. **GetJobs.py**  
   Fetches job IDs that match specified search criteria using the Coresignal API's Job endpoints.

2. **ExtractJobDetails.py**  
   Retrieves detailed job descriptions from the Coresignal API's Collect endpoints based on job IDs identified by the `GetJobs.py` script.

The output is a consolidated dataset: `job_details.csv`, which serves as the input for the job-matching algorithm.

---

## Job Matching Algorithm

The job matching process evaluates a user’s resume against individual job descriptions to determine compatibility:

- **ChatGPT Integration**  
  The system uses a pre-configured prompt to enable ChatGPT to act as a "Job Recommendation Assistant." It compares the user’s resume with job descriptions and assesses the fit based on predefined criteria.
  
- **Decision Framework**  
  If gaps are identified in the user's skills or experience, the system excludes the job from recommendations. Conversely, perfectly matched roles are highlighted for immediate application.

- **Model Settings**  
  A temperature of **0.25** ensures the model employs consistent and balanced decision-making, increasing the likelihood of uncovering relevant matches.

---

## Results

The system outputs a comprehensive list of jobs based on the user’s search criteria, categorized as follows:

- **Recommended Jobs**  
  Positions that align perfectly with the user's qualifications, prompting immediate application.

- **Excluded Jobs**  
  Roles where skill or experience gaps were identified, accompanied by constructive feedback for improvement.

---

## Getting Started

1. **Prepare Inputs**  
   - Upload your resume in a compatible format.  
   - Specify job search criteria.

2. **Run the Scripts**  
   - Use `GetJobs.py` to fetch job IDs.  
   - Execute `ExtractJobDetails.py` to compile job descriptions into `job_details.csv`.

3. **Launch the Matching Process**  
   Input your resume and the `job_details.csv` file into the system to generate personalized job recommendations.

---

## Future Enhancements

- Support for additional APIs to expand the job search database.  
- Advanced filtering for customizable job recommendations.  
- Integration of upskilling resources for addressing identified skill gaps.

--- 

This project streamlines the job application process, ensuring users focus their efforts on opportunities with the highest likelihood of success.

For further details, feel free to explore the codebase or reach out with questions and feedback.
