AI EHR Summarizer
=================

An AI-powered tool that ingests complex Electronic Health Records (EHR) — including clinical notes, lab results, and imaging summaries — and outputs concise, medically-relevant summaries for physicians and healthcare providers. Built using Mistral-7B, LangChain, and Streamlit.

Features
--------

- Summarizes raw EHR data into readable, accurate summaries.
- Supports clinical notes, discharge summaries, and lab reports.
- Uses LangChain with Mistral-7B (or OpenAI/GPT-4 optionally).
- Frontend built with Streamlit for easy user interaction.
- Stores patient data and summaries using PostgreSQL.
- Converts EHR into FHIR-compliant structure.

Tech Stack
----------

Frontend       : Streamlit, Python  
Backend (AI)   : LangChain, Mistral-7B, HuggingFace  
Data Format    : FHIR (HL7)  
Database       : PostgreSQL, SQLAlchemy  
Preprocessing  : Pandas, Regex, fhir.resources  

Project Structure
-----------------

ai-ehr-summarizer/
│
├── app/              # AI pipeline, prompt templates, FHIR preprocessing  
├── frontend/         # Streamlit UI and session handling  
├── models/           # Mistral model config and loading  
├── database/         # Schema and DB init scripts  
├── data/             # Raw and processed clinical data  
├── notebooks/        # Data exploration and evaluation  
├── utils/            # Logging, helper functions  
├── requirements.txt  # Python dependencies  
├── Dockerfile        # For containerized deployment (optional)  
└── README.md  

Getting Started
---------------

1. Clone the repository:

   git clone https://github.com/yourusername/ai-ehr-summarizer.git  
   cd ai-ehr-summarizer

2. Install dependencies:

   python -m venv venv  
   source venv/bin/activate  
   pip install -r requirements.txt

3. Initialise the database:

   python database/init_db.py

4. Run the Streamlit app:

   streamlit run frontend/main_app.py

Sample Use Case
---------------

Upload a clinical note (e.g., a discharge summary), and the app will:

1. Preprocess it into FHIR format  
2. Generate a concise summary using Mistral-7B or GPT  
3. Store results in the database  
4. Display everything in a clean UI

Sample Input
------------

Discharge Summary:  
"The patient presented with fever, cough, shortness of breath...  
Treated with antibiotics and discharged in stable condition."

Sample Output
-------------

- Patient had a respiratory infection  
- Treated with antibiotics  
- Responded well to treatment  
- No ICU admission  
- Discharged stable on day 4

Ideal For
---------

- Medical AI researchers  
- Hospitals/Clinics with EHR data  
- HealthTech startups  
- Medical students for case summarization  



MIT License — Free to use, modify, and distribute.
