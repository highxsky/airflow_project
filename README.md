# Functional Documentation: Airflow DAG for Job Offers Retrieval

## Purpose
Demonstrate an Airflow DAG for retrieving and storing job offers related to data analytics from the France Travail API.

## Main Steps

### 1. Connect to API
- Authenticate using OAuth2 with client ID and secret.
- Retrieve an access token for API requests.

### 2. Retrieve Job Offers
- Fetch job offers with the following criteria:
  - Keywords: "data"
  - Departments: Paris (75), Hauts-de-Seine (92)
  - Contract type: CDI
  - Creation date: Last 30 days
  - Experience level: Senior (over 3 years)

### 3. Store Data
- Save selected job details in a local database:
  - Job title
  - Description
  - Creation date
  - Job category
  - Industry sector
  - Contract type
  - Salary information

## Notable Features
- **On-Demand Execution**: Manually trigger the DAG to update job offers.
- **Data Processing**: Clean and format job data before storage.
- **Partial Response Handling**: Ensure all available job offers are retrieved.

## Conclusion
This DAG demonstrates a functional workflow for retrieving and storing job offers related to data analytics from the France Travail API.