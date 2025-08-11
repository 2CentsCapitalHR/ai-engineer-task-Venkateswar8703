# ADGM-Compliant Corporate Agent with Document Intelligence USING RAG

## Overview
This Corporate Agent provides a document review tool for ADGM corporate incorporation documents. It uses a Retrieval-Augmented Generation (RAG) pipeline with Gemini (Google PaLM API) to analyze `.docx` files, highlight issues, and provide compliance suggestions based on official ADGM references.
 
---

## Features

- Upload multiple `.docx` documents for review  
- Automatic detection of key incorporation documents  
- Highlights potential legal issues and missing clauses  
- RAG-powered suggestions using Gemini LLM with official ADGM references  
- Outputs a reviewed `.docx` with comments and a structured JSON report  
- Download reviewed documents as a ZIP archive  

---

## Requirements

- Python 3.8+  
- Google API Key with access to PaLM API (Gemini)  
- Internet connection for API calls  

---

## Setup Instructions

1. **Clone the repository or unzip the codebase:**  
   ```bash
   git clone <your_repo_url>
   cd <repo_folder>
2. **Create a Python virtual environment:**
   python -m venv venv
   source venv/bin/activate   # Linux/macOS
   \venv\Scripts\activate    # Windows
3. **Install dependencies:**
   pip install gradio sentence-transformers transformers pypdf python-docx google-generativeai numpy
4. **Set your Google API Key environment variable:**
   On Linux/macOS: export GOOGLE_API_KEY="your_api_key_here"
   On Windows (PowerShell):setx GOOGLE_API_KEY "your_api_key_here"
5. **Place official ADGM reference documents (.docx or .pdf) in the folder named** adgm_refs
   This folder is used to build the retrieval index for RAG.
6. **Run the Gradio demo:**
   python app.py
7. **Open the URL provided by Gradio in your browser:Usage**
     
   ---
       -Upload one or more .docx files related to ADGM incorporation.
       -Click Analyze Documents.
       -View structured JSON analysis and download reviewed documents with comments.
   ---
