# WellnessAI (CS467 Online Capstone)
AI-driven wellness companion for holistic fitness, nutrition, and stress management.
Built with a React frontend, FastAPI backend, and LLM integration for intelligent, personalized support.

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
├── frontend/            # React-based UI
├── backend/             # FastAPI backend
└── benny-ai-service/    # Microservice that handles OpenAI LLM interactions
└── benny-ai-service/    # Microservice that handles OpenAI LLM interactions


# Prerequisites
Make sure you have the following installed:
- Node.js
- Python 3.9+
- PostgreSQL
- pip
- Git

# Running the App
1. Clone the repository
git clone https://github.com/obriewil/CS467_WellnessAI.git
cd CS467_WellnessAI

2. Run the Frontend
cd frontend
npm install
npm start
*Runs on http://localhost:3000

3. Run the Backend (FastAPI)

cd backend
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn main:app --reload
* FastAPI will start at http://localhost:8000

Make sure to set up your .env file with proper database and OpenAI API credentials.

4. Run the AI Service (Benny-AI-Service)
This microservice interfaces with the OpenAI API and handles prompt generation and AI logic.
cd benny-ai-service
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python service.py
Ensure this service is running before backend operations that require LLM calls.

# Environment Variables
Set the following variables in each component's .env file:

backend/.env
DATABASE_URL=postgresql://user:password@localhost:5432/wellnessdb
OPENAI_API_KEY=your-api-key

benny-ai-service/.env
OPENAI_API_KEY=your-api-key

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
MIT License. See LICENSE file for more details.

# Contact
For inquiries or contributions, feel free to open an issue or contact any team member.

