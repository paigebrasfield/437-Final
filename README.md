# 437-Final Project
#### Paige Brasfield and Kayley Salcido

Our application is a resume analyzer that automatically reads, screens, and sorts resumes uploaded based on the information on the resume. 

The user will upload their PDF resume though a web interface. The application will extract key information like name, email, skills, and years of experience. The information will be stored in a structured formate to be easily analyzed.

# Cloud Services Used
- Cloud Storage
- Cloud Functions
- Document AI
- BigQuery
- Cloud Run
# How the services interact
1. The user uploades a PDF resume through frontend
2. Cloud storage stores the resume in a bucket
3. The upload triggers Cloud function automatically
4. Cloud function performs the backend processing:
   - Downloading the file from Cloud Storage
   - Sending the file to Document AI
6. Document AI will extract relevant information
7. The extracted data is parsed and formatted
8. The structured data will be put into BigQuery

# How to setup/install/run

#### Prerequisites
1. Create Google Cloud account
2. Create a project
3. Enable APIs
   - Cloud Functions
   - Cloud Storage
   - Document AI
   - BigQuery
   - Cloud Run

#### Backend
1. Create Cloud Storage bucket
2. Create Document AI processor
   - Save the processor ID
4. Create a BigQuery dataset and table
5. Deploy Cloud Function

#### Frontend
1. Create frontend folder and include:
   - app.py
   - requirements.py
   - Procfile
   - templates/
3. Install dependencies:
   - pip install -r requirements.txt
4. Run locally:
   - python app.py
5. Open IP address given

#### How to Run
1. Open Cloud Run URL
   - Use the top URL
3. Upload resume
4. Go back to the terminal and redeploy the URL
5. Navigate to /search
6. Search for candidates using key words/skills
7. View results in BigQuery





