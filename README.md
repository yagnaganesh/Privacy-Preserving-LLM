Overview
--------
-This project demonstrates a privacy-first approach to working with Large Language Models (LLMs). It ensures personal information is never exposed to external models during prompt      processing.
-The system anonymizes sensitive data before sending a prompt to Google Gemini, retrieves the response, and then reconstructs the output by reinserting the original information locally using a custom internal model.

Features
--------
- De-identification of personal data (names, emails, phone numbers, etc.) using an internal NLP model.
- Secure LLM queries with anonymized prompts sent to Gemini.
- Post-processing that reinserts sensitive details after receiving responses.
- Enhanced privacy — no user data leaves the local environment for training or storage.

🛠️ Tech Stack
-------------
- Python (core logic)
- Jupyter Notebook (prototyping & workflow)
- Custom NLP Model (for de-identification & re-identification) (WORK IN PROGRESS FOR NOW USING EXTERNAL LLM'S)
- Google Gemini API (LLM integration)

Workflow
--------
- Input Processing → Detect and replace personal identifiers with placeholders.
- Anonymized Query → Send sanitized prompt to Gemini.
- Response Handling → Receive output and maintain placeholder mappings.
- Reconstruction → Replace placeholders with original personal data locally.
