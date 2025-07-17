# WellnessAI (CS467 Online Capstone)
WellnessAI is a web-based application that empowers users to take control of their health through personalized, goal-driven guidance across fitness, nutrition, and stress management. By combining intelligent habit tracking with natural language support from a large language model (LLM), the app acts as a virtual wellness coach—offering daily encouragement, progress insights, and adaptive planning based on the user's evolving goals.

Unlike traditional health apps that isolate one aspect of wellness, WellnessAI blends goal prioritization, AI recommendations, and an intuitive user interface to promote long-term engagement and real, sustainable change.


# Project Overview
WellnessAI is a full-stack wellness web application designed to help users set and achieve personalized goals across nutrition, fitness, and stress management domains. The app uses an LLM (via OpenAI's API) to deliver daily affirmations, intelligent planning, goal recommendations, and conversational support based on user progress and preferences.

Key Features Include:
- Ranked goal-setting interface
- Daily check-ins and progress tracking
- Weekly AI-generated insights
- Integrated chat interface for support and planning
- Secure user authentication
- Scalable architecture with modular services

# Project Structure
CS467_WellnessAI/

|__ frontend/            # React-based UI

|__ backend/             # FastAPI backend

|__ benny-ai-service/    # Microservice that handles OpenAI LLM interactions

|__ bennyDB/    # Database for storing user information and daily check ins

|__ testing/    # Testing for individual features

|__ tests.py & tests.js/    # Regression testing files for checking before merges


# Prerequisites
Make sure you have the following installed:

- Node.js
- Python 3.9+
- PostgreSQL
- pip
- Git

# Running the App
## 1. Clone the repository

git clone https://github.com/obriewil/CS467_WellnessAI.git

cd CS467_WellnessAI


## 2. Run the Frontend

cd frontend

npm install

npm start

PORT: http://localhost:3000


## 3. Run the Backend (FastAPI)

cd backend

python -m venv venv

source venv/bin/activate  # or venv\Scripts\activate on Windows

pip install -r requirements.txt

uvicorn main:app --reload

PORT: FastAPI will start at http://localhost:8000

Make sure to set up your .env file with proper database and OpenAI API credentials.


## 4. Run the AI Service (Benny-AI-Service)

### Create Virtual Environment (MacOS/Linux)
cd benny-ai-service    

python -m venv benny-env 

source benny-env/bin/activate

pip install -r requirements.txt 


### Create Virtual Environment (Windows)
cd benny-ai-service 

python -m venv benny-env 

benny-env\Scripts\activate 

pip install -r requirements.txt 

*This microservice interfaces with the OpenAI API and handles prompt generation and AI logic.

### Run AI Service
cd src/api 

python main.py

PORT: http://localhost:8001

*Ensure this service is running before backend operations that require LLM calls.


# Running Tests
** NEED TO FILL IN**

# Tech Stack

Frontend: React, Tailwind CSS, React Router

Backend: FastAPI, PostgreSQL, SQLAlchemy

AI Service: Python + OpenAI API

Testing: **FILL IN** (frontend), Pytest (backend)

# Team Members

BriAnna Foreman – LLM integration, AI prompt engineering

James Liu – Frontend UI/UX & component development

Michael Jagielski – Backend databases and data flow

William O’Brien – DevOps, API integration, microservice orchestration

# License
MIT License

# Contact
For inquiries or contributions, feel free to open an issue or contact any team member.

