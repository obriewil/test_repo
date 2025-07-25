About Benny
Tech Stack:
AI Model: Azure OpenAI GPT-3.5-Turbo
Backend: Python FastAPI
Personality: Custom prompt engineering for wellness coaching
Integration: REST API

1. Set Up & Run
# create virtual environment
cd benny-ai-service
python -m venv benny-env
source benny-env/bin/activate  # macOS/Linux benny-env\Scripts\activate   # Windows
pip install -r requirements.txt
# run
cd src/api
python main.py

port: http://127.0.0.1:8001

2. API Endpoints

HEALTH CHECK
GET /health

Returns: {"status": "healthy", "benny_ready": true}

CHAT
POST /chat
Content-Type: application/json

{
    "message": "How can I eat more fiber?"
}

Response:

json 
{
    "success": true,
    "response": "Fiber is an important part of healthy digestion...",
    "tokens_used": 300
    "error": null
}

React Example
// Chat with Benny
const chatWithBenny = async (message) => {
  const response = await fetch('http://localhost:8001/chat', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ message }),
  });
  
  const data = await response.json();
  return data.success ? data.response : "Benny is taking a break!";
};

RECOMMEND
POST /recommend
Content-Type: application/json

{
    "nutrition": "",
    "fitness": "",
    "stress": "",
    "sleep: ""
}

Response
{
    "success": true,
    "response": "Focus on establishing a consistent bedtime routine...",
    "tokens_used": 32,
    "error": null
}

Test Benny in the Browser
Use http://127.0.0.1:8001/docs to test endpoints in the browser

Frontend Integration
chat function: fetch('http://localhost:8001/chat')


Citations
Claude AI used for planning and implementing chatbot development.
- Benny testing generation
Youtube Videos for learning about Azure, OpenAI, chatbot development
https://youtu.be/jQyYeYWD97I?si=8GYBJ7TQR6ChuIBh
https://www.youtube.com/watch?v=u0AUwOKxUsg
https://www.youtube.com/watch?v=fQ9RFR1KTbY
https://www.youtube.com/watch?v=GD7MnIwAxYM
https://www.youtube.com/watch?v=GD7MnIwAxYM

