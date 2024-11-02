# Resume Parser And AI Suggestor and PDF Generator

This Flask-based application processes resumes to extract useful information (like name, contact, skills, and education), generate career suggestions, and create PDF summaries.

## Features

- **Resume Upload**: Accepts PDF resumes and extracts text.
- **Info Extraction**: Identifies name, contact, email, skills, education, and work experience using NLP and regex.
- **Career Suggestions**: Uses Google’s Gemini API to suggest skill improvements based on current skills and job goals.
- **PDF Generator**: Creates downloadable PDFs summarizing the parsed resume data.

## Setup

1. Clone the repository:
    ```
    git clone <your_repo_url>
    cd <repo_folder>
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

