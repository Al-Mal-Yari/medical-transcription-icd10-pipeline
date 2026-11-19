# medical-transcription-icd10-pipeline
An LLM-powered data pipeline built in DataCamp DataLab that uses OpenAI Function Calling to extract patient ages and treatments from medical transcriptions, mapping them to ICD-10 codes.

# Medical Transcription Extraction & ICD-10 Coding Pipeline

> **Note on Repository History:** This project was originally developed and completed within the **DataCamp DataLab** notebook environment. As a result, you will see very few commits in this repository, and the code is largely copied directly from the completed notebook to showcase the final result. The anonymized `transcriptions.csv` dataset was provided by DataCamp for educational purposes.

## Overview
This project demonstrates how to transform unstructured medical transcription data into a clean, structured pandas DataFrame. By leveraging the OpenAI API's structured **Function Calling** capabilities, the pipeline reliably extracts key medical data points without conversational filler or hallucinations.

## How it Works
1. **Data Extraction:** Iterates through the raw text dataset, using strict JSON schemas to extract the patient's age and recommended treatments.
2. **ICD-10 Matching:** Passes the extracted treatments and medical specialties to a secondary LLM call, prompting the model to act as a medical coder to assign the correct ICD-10 code.
3. **Data Structuring:** Parses the JSON tool-call arguments and compiles the results into a pandas DataFrame (`df_structured`) for downstream analysis.

## Key Tools Used
*   **Python** (pandas, json)
*   **OpenAI API** (GPT-4o-mini, Function Calling, `tool_choice`)
*   **DataCamp DataLab** (Environment & Dataset)
