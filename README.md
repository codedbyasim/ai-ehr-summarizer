# AI EHR Summarizer

An AI-powered tool that ingests complex Electronic Health Records (EHR) — including clinical notes, lab results, and imaging summaries — and outputs concise, medically-relevant summaries for physicians and healthcare providers. Built using Mistral-7B, LangChain, and Streamlit.

---

## Features

- Summarises raw EHR data into readable, accurate summaries.
- Supports clinical notes, discharge summaries, and lab reports.
- Uses **LangChain** with **Mistral-7B** (or OpenAI/GPT-4 optionally).
- Frontend built with **Streamlit** for easy user interaction.
- Stores patient data and summaries using **PostgreSQL**.
- Converts EHR into **FHIR-compliant** structure.

---

## Tech Stack

| Layer         | Tools/Frameworks                     |
|---------------|--------------------------------------|
| **Frontend**  | Streamlit, Python                    |
| **Backend AI**| LangChain, Mistral-7B, HuggingFace   |
| **Data Format**| FHIR (HL7)                         |
| **Database**  | PostgreSQL, SQLAlchemy              |
| **Preprocessing**| Pandas, Regex, fhir.resources    |
