# LLM Chat App

A lightweight FastAPI-based chatbot using OpenAI's API.

## 🚀 Features
- `/chat` POST endpoint for interacting with GPT.
- Modular project structure
- Easy to deploy with Docker
- `.env` support for API key management

## 🔧 Setup

Create a `.env` file:
```bash
OPENAI_API_KEY=your-openai-key
```

Install dependencies and run:
```bash
pip install -r requirements.txt
uvicorn llm_chat_app.main:app --reload
```

### Example Request
POST `/chat`
```json
{
  "message": "Hello, who are you?"
}
```

### Response
```json
{
  "response": "I am an AI developed by OpenAI..."
}
```

## 🐳 Docker
```bash
docker build -t llm-chat-app .
docker run --env-file .env -p 8000:8000 llm-chat-app
```
