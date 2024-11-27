# Resume Parser And AI Suggestor and PDF Generator

This Flask-based application processes resumes to extract useful information (like name, contact, skills, and education), generate career suggestions, and create PDF summaries.

## Features

- **Resume Upload**: Accepts PDF resumes and extracts text.
- **Info Extraction**: Identifies name, contact, email, skills, education, and work experience using NLP and regex.
- **Career Suggestions**: Uses Google’s Gemini API to suggest skill improvements based on current skills and job goals.
- **PDF Generator**: Creates downloadable PDFs summarizing the parsed resume data.

![Screenshot 2024-11-27 224328](https://github.com/user-attachments/assets/78940d3a-4ca7-4c3a-8e25-0de71dedfd5f)
![Screenshot 2024-11-27 224245](https://github.com/user-attachments/assets/d02a700f-b6bb-43f7-a1f9-559fc34b6caa)
![Screenshot 2024-11-27 224355](https://github.com/user-attachments/assets/21e9cf6e-a5e2-419b-9ab2-efd96a11325b)


## Setup

1. Clone the repository:
    ```
    git clone https://github.com/Sa1f27/AI-Resume-Parser.git
    cd AI-Resume-Parser
    ```

2. Install dependencies:
    ```bash
    pip install Flask spacy pdfminer.six fpdf google-generativeai
    ```
3. Download spaCy's language model:
    ```
    python -m spacy download en_core_web_sm
    ```

4. Set your Google Generative AI key:
   - Replace `Your_key` in `api_key="Your_key"` with your API key from Google.

## Usage

1. Start the Flask application:
    ```
    python app.py
    ```
2. Open a browser and go to `http://127.0.0.1:5000/`.

## API Endpoints

- **POST /upload**: Upload a resume to extract data.
- **POST /generate_pdf**: Generate a summary PDF with parsed details.
- **POST /generate**: Generate career suggestions based on provided skills.
- **GET /downloads/<filename>**: Download generated PDFs.

## File Structure

- `app.py`: Main Flask application.
- `templates/index.html`: Frontend template for uploads.
- `uploads/`: Stores uploaded resumes and generated PDFs.

