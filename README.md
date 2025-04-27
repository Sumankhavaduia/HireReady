# HireReady - AI Powered Resume Builder

**HireReady** is an intelligent resume builder that helps users create professional resumes quickly and efficiently, enhanced by AI-powered features. The platform allows users to craft resumes by filling out basic details, with additional functionality to improve job descriptions, skills, and summaries via AI suggestions. 

---

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Setup and Installation](#setup-and-installation)
    - [Frontend Setup](#frontend-setup)
    - [Backend Setup](#backend-setup)
    - [Environment Variables](#environment-variables)
5. [Usage](#usage)
6. [AI Features](#ai-features)
    - [AI Resume Summary](#ai-resume-summary)
    - [AI Skill Suggestions](#ai-skill-suggestions)
    - [AI Experience Enhancement](#ai-experience-enhancement)
7. [Contributing](#contributing)
8. [License](#license)
9. [Acknowledgments](#acknowledgments)

---

## Overview

**HireReady** simplifies resume creation for job seekers by offering an easy-to-use interface for building resumes and providing AI-powered suggestions to enhance the content. Whether you're creating your first resume or looking to refine an existing one, HireReady can help improve your chances of landing a job by providing recommendations based on industry standards.

---

## Features

- **User Authentication**: Sign up/login functionality using JWT authentication.
- **Resume Creation**: Fill out basic resume details like personal information, skills, and experience.
- **AI Resume Summary**: Generate a professional summary for your resume based on your job title and experience.
- **AI Skill Suggestions**: Suggest relevant skills based on job titles and experience.
- **AI Experience Enhancement**: Refine and enhance job descriptions using AI.
- **PDF Download**: Download your resume as a PDF once it's created and customized.
- **Multiple Templates**: Select from various professional resume templates to customize the layout.

---

## Tech Stack

- **Frontend**: React, Tailwind CSS
- **Backend**: Django, Django REST Framework
- **AI**: OpenAI GPT-3 or GPT-4 API (for resume enhancement features)
- **Authentication**: JWT (JSON Web Tokens) for secure user login
- **PDF Generation**: jsPDF (for generating downloadable PDFs)
- **Database**: SQLite (for development) or PostgreSQL (for production)

---

## Setup and Installation

### Frontend Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/hire-ready.git
    cd hire-ready
    ```

2. Navigate to the frontend directory:

    ```bash
    cd frontend
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

4. Run the React development server:

    ```bash
    npm start
    ```

    The app will be available at `http://localhost:3000`.

### Backend Setup

1. Navigate to the backend directory:

    ```bash
    cd backend
    ```

2. Set up a virtual environment (optional but recommended for Python projects):

    ```bash
    python -m venv venv
    ```

3. Activate the virtual environment:

    - On Windows:

    ```bash
    venv\Scripts\activate
    ```

    - On macOS/Linux:

    ```bash
    source venv/bin/activate
    ```

4. Install the required Python dependencies:

    ```bash
    pip install -r requirements.txt
    ```

5. Apply migrations to set up the database:

    ```bash
    python manage.py migrate
    ```

6. Run the Django development server:

    ```bash
    python manage.py runserver
    ```

    The backend will be available at `http://localhost:8000`.

---

## Environment Variables

The following environment variables are required for the backend to function properly:

- `SECRET_KEY`: Django secret key for session and CSRF protection.
- `DEBUG`: Set to `True` for development and `False` for production.
- `DB_NAME`: The name of the database used in your project.
- `DB_USER`: Database user.
- `DB_PASSWORD`: Database password.
- `DB_HOST`: Database host (default: `localhost`).
- `DB_PORT`: Database port (default: `5432` for PostgreSQL).
- `OPENAI_API_KEY`: API key for accessing OpenAI's GPT model.

Create a `.env` file in the `backend/` folder and add the necessary variables:

```plaintext
SECRET_KEY=your-secret-key
DEBUG=True
DB_NAME=hire_ready
DB_USER=your-db-user
DB_PASSWORD=your-db-password
DB_HOST=localhost
DB_PORT=5432
OPENAI_API_KEY=your-openai-api-key

