# Agentic AI Chat Assistant (Gradio + Groq + Tool Use)

🤖 This is an  **Agentic AI chatbot** — an AI agent that can autonomously take actions using predefined tools, guided by personalized context from your resume and professional summary. Designed for personal or professional websites, this assistant can answer career-related questions, collect user information, and log unknown queries—all with minimal human oversight.

---

🧠 What is Agentic AI?

**Agentic AI** refers to AI systems capable of:
- Maintaining goals (e.g. represent you professionally)
- Taking actions (e.g. call tools like 'record_user_details', 'record_unknown_question')
- Reacting autonomously to user input with tools and memory
- Staying "in character" across interactions

This project is a practical, lightweight implementation of Agentic AI using OpenAI-compatible APIs and structured tool usage.

---

🔍 Key Features

💬 Conversational Input
Users ask natural language questions about your skills, background, or experience.

📄 Personalized Context
The assistant uses two primary sources:
- ✅ `resume.pdf` — parsed to extract your details
- ✅ `summary.txt` — a curated description of your background

🛠️ Autonomous Tool Use
The AI agent has access to these tools:
- `record_user_details`: Captures user email, name, and notes
- `record_unknown_question`: Logs unanswerable questions
- 🔔 Both tools trigger **Pushover** alerts in real time

🔗 Backend LLM
- Powered by `llama-3.3-70b-versatile` from Groq API
- Tools are executed using the OpenAI tool calling format

🖥️ Gradio UI
- Clean interface using `gr.ChatInterface(type="messages")`
- Runs locally via browser at `http://127.0.0.1:7860`
