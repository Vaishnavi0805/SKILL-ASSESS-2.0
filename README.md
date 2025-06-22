# Skill Assess - Your AI Mock Interviewer
Job seekers often face anxiety and unpreparedness due to inadequate interview preparation, with many existing tools neglecting the development of technical skills. Our AI-powered web application, Skill Assess, addresses this issue by providing tailored interview simulations based on specific job descriptions. By focusing on both skill enhancement and confidence building, our platform helps candidates excel in interviews through realistic scenarios and personalized feedback. Our goal is to empower candidates to succeed in the competitive job market by addressing the gap in technical skills and subject-specific knowledge.

## Proposed System

### Input

The system requires three inputs:
1. **Candidate's Resume**: Contains information about the candidate's skills, experience, and educational background.
2. **Job Description**: Outlines the requirements and qualifications for the job the candidate is applying for.
3. **Job Round**: Indicates whether the mock interview is for a Technical round or an HR round.

### Prompt Engineering

The system employs prompt engineering to create two types of prompts for the PaLM model:
1. **Question Generation Prompt**: Generates a set of categorized questions for the mock interview based on the candidate's resume, job description, and job round.
2. **Answer Evaluation Prompt**: Evaluates the candidate's answers using criteria such as relevance, completeness, and clarity.

### Question Generation

The question generation prompt produces a set of tailored questions for the mock interview. The categories vary depending on the job role and round, with technical rounds focusing on technical skills and knowledge, and HR rounds assessing communication skills and cultural fit.

### Answer Evaluation

The answer evaluation prompt assesses the candidate's responses based on specific criteria. Technical rounds evaluate technical accuracy, while HR rounds focus on clarity and communication skills.

### Evaluation Report

Upon completion of the mock interview, the system generates an evaluation report that includes:
1. **Score for Each Criteria**: Scores are assigned based on the candidate's answers and evaluation metrics.
2. **Suggestions for Improvement**: Provides actionable feedback to help candidates enhance their performance in future interviews.
3. **Video Evaluation**: Analyzes emotional cues such as confidence, nervousness, sadness, and fear, offering insights into the emotional context of the responses and helping candidates improve their presentation skills.

## Tech Stack

- **Programming Language**: Python 3.8 or above
-   **AI Model**: Google’s Gemini Model (formerly known as PaLM2, text-bison@001)
- **Web Framework**: Django
- **PDF Processing**: Pdfplumber
- **Computer Vision**: OpenCV’s Face Detector Model
- **Machine Learning**: TensorFlow
- **Speech Processing**: SpeechRecognition

## Setting/Installation

### Prerequisites

Before starting the application, ensure you have the following installed:

-   Python 3.6 or above
-   Pip (Python package installer)

### Installation Steps

1.  **Clone the Repository**:
  
    ```
    git clone <repository_url>  
    cd skill_assess
    ```
    
2.  **Create a Virtual Environment**:
    
    ```
    python -m venv venv
    ```
3.  **Activate the Virtual Environment**:
    
    -   On Windows:
        
    ```
    venv\Scripts\activate
    ```
    
    -   On macOS/Linux:
        
    ```
    source venv/bin/activate
    ```
        
4.  **Install Dependencies**:
    
    ```
    pip install -r requirements.txt
    ```
    
5.  **Configure AWS S3 Bucket**: Before starting the application, configure the AWS S3 bucket settings in `skill_assess/settings.py`. Ensure you have the necessary AWS credentials and bucket information.
    
6.  **Run Migrations**:
    ```
    python manage.py migrate
    ```
7.  **Start the Application**:
    ```
    python manage.py runserver
    ```
    
8.  **Access the Application**: Open your browser and navigate to `http://127.0.0.1:8000/` to access the Skill Assess application.


## Screenshots of Application

Below are some screenshots showcasing the key features and interfaces of the Skill Assess application:


_The home page of Skill Assess, featuring navigation options and an overview of the platform._
<div align="center">
  <img src="https://github.com/Vaishnavi0805/SKILL-ASSESS-2.0/blob/main/screenshots/sa1.png?raw=true" alt="Sample Image" width="700" height="400">
</div>

_Registration page of Skill Assess._
<div align="center">
  <img src="https://github.com/Vaishnavi0805/SKILL-ASSESS-2.0/blob/main/screenshots/sa2.png?raw=true" alt="Sample Image" width="700" height="400">
</div>

_The mock interview interface where candidates can practice answering questions tailored to their job role._
<div align="center">
  <img src="https://github.com/Vaishnavi0805/SKILL-ASSESS-2.0/blob/main/screenshots/sa3.png?raw=true" alt="Sample Image" width="700" height="400">
  <img src="https://github.com/zerothrohit/SKILL-ASSESS-2.0/blob/main/screenshots/interview.png?raw=true" alt="Sample Image" width="700" height="400">
</div>

_The evaluation report, providing scores, suggestions for improvement, and video analysis._
<div align="center">
  <img src="https://github.com/Vaishnavi0805/SKILL-ASSESS-2.0/blob/main/screenshots/sa5.png?raw=true" alt="Sample Image" width="700" height="400">
  <img src="https://github.com/Vaishnavi0805/SKILL-ASSESS-2.0/blob/main/screenshots/sa6.png?raw=true" alt="Sample Image" width="700" height="400">
</div>

---
