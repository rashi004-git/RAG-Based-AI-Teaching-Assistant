# RAG-Based-AI-Teaching-Assistant
Developed a RAG-Based AI Teaching Assistant using LLMs, NLP, and vector embeddings to retrieve relevant information from educational documents and provide accurate, context-aware answers to students' queries.

🎓 RAG-Based AI Teaching Assistant

An intelligent AI-powered teaching assistant that helps students understand lecture content by asking questions and receiving relevant, context-aware answers using Retrieval-Augmented Generation (RAG).

The system processes lecture videos, converts them into timestamped transcripts, generates semantic embeddings, and stores them in a vector database. When a student asks a question, the system retrieves relevant lecture content and uses Google's Gemini API to generate an informative answer.

---

🚀 Project Overview

Finding specific topics in lengthy educational videos can be time-consuming for students.

To solve this problem, this project provides an interactive AI chatbot that allows students to ask questions directly from lecture materials.

For example:

«"What is Binary Search?"»

The system searches the available lecture content and generates an answer based on relevant information, along with lecture source and timestamp details.

---

🏗️ System Architecture

Lecture Videos
      |
      ▼
Speech-to-Text Transcription
      |
      ▼
Timestamped Transcripts
      |
      ▼
Text Chunking
      |
      ▼
BGE-M3 Embeddings
      |
      ▼
ChromaDB Vector Database
      |
      ▼
Student Question
      |
      ▼
Question Embedding
      |
      ▼
Similarity Search
      |
      ▼
Relevant Lecture Context
      |
      ▼
Google Gemini API
      |
      ▼
AI Generated Response
      |
      ▼
Interactive Chatbox

---

✨ Key Features

- 🎥 Automatic lecture video transcription
- 📝 Timestamp-based transcript generation
- ✂️ Efficient text chunking
- 🧠 Semantic embeddings using BGE-M3
- 🗄️ Vector storage and similarity search with ChromaDB
- 🤖 AI-generated answers using Google Gemini
- 💬 Interactive web-based chatbot
- 📚 Lecture references with timestamps
- 📋 Copy answer functionality
- 🔒 Secure API key management using environment variables
- 🌐 Flask-based backend API
- ⚡ Local embedding generation through Ollama

---

🛠️ Technologies Used

Backend

- Python
- Flask
- Flask-CORS
- Requests

Generative AI

- Google Gemini API
- Retrieval-Augmented Generation (RAG)

Embedding Model

- BGE-M3
- Ollama

Vector Database

- ChromaDB

Frontend

- HTML
- CSS
- JavaScript
- Marked.js

Data Processing

- JSON
- Python Pickle
- LangChain Text Splitters

---

📁 Project Structure

RAG-AI-Teaching-Assistant/
│
├── backend/
│   ├── app.py
│   └── requirements.txt
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── scripts/
│   ├── transcription.py
│   ├── chunking.py
│   └── embedding.py
│
├── data/
│   └── README.md
│
├── .env
├── .gitignore
└── README.md

Note: API keys, lecture videos, generated databases and other sensitive or large files should be excluded from GitHub.

---

⚙️ Working Process

1. Video Transcription

Lecture videos are converted into text using speech-to-text processing. Each transcript includes start time, end time and lecture content.

2. Text Chunking

The extracted text is divided into smaller sections for better retrieval.

- Chunk Size: 1000
- Chunk Overlap: 200

3. Embedding Generation

The BGE-M3 model converts text chunks into numerical vectors using Ollama.

4. Vector Database Storage

Generated embeddings and their corresponding text are stored in ChromaDB.

5. Semantic Search

When a student submits a question, the system converts it into an embedding and searches for the most relevant lecture sections.

6. AI Answer Generation

The retrieved information is sent to Google's Gemini model, which generates a context-aware response based on the provided lecture content.

---

💻 Installation & Setup

Prerequisites

- Python
- Git
- Ollama
- Google Gemini API Key

Step 1: Clone Repository

git clone <your-repository-url>
cd RAG-AI-Teaching-Assistant

Step 2: Install Dependencies

cd backend
pip install -r requirements.txt

Step 3: Download Embedding Model

ollama pull bge-m3

Verify the installation:

ollama list

Step 4: Configure API Key

Create a ".env" file in the project root:

GEMINI_API_KEY=your_api_key_here

Keep your API key private and never upload the ".env" file.

Step 5: Run Backend

cd backend
python app.py

Flask server:

http://127.0.0.1:5000

Step 6: Run Frontend

Open the frontend using VS Code Live Server or another local web server.

The chatbot interface will be available in your browser.

---

🧪 Example Workflow

Student Question:

"What is Binary Search?"

Processing:

Student Question
       ↓
BGE-M3 Embedding
       ↓
ChromaDB Search
       ↓
Relevant Lecture Content
       ↓
Gemini API
       ↓
Context-Aware Answer

The generated response can include the relevant lecture reference and timestamp.

---

🎯 Benefits of the Project

- Saves students' time when searching through long lectures.
- Provides quick answers to academic questions.
- Makes learning more interactive and accessible.
- Helps students understand topics using lecture-specific context.
- Makes it easier to locate relevant sections in educational videos.

---

🔐 Security

The Gemini API key is accessed through environment variables:

os.getenv("GEMINI_API_KEY")

Sensitive credentials and private data should never be pushed to a public repository.

---

🔮 Future Enhancements

- Multiple course and subject support
- Student login and authentication
- Chat history management
- Automatic quiz and question generation
- Voice-based interaction
- Improved answer streaming
- Cloud deployment
- Student learning analytics

---

📌 Project Status

Version: 1.0

The project demonstrates an end-to-end Retrieval-Augmented Generation pipeline:

Video Processing → Transcription → Chunking → Embeddings → Vector Storage → Retrieval → Gemini → AI Response

---

👩‍💻 Author

Vanshika Chauhan

Aspiring Data Scientist | Data Analyst | AI & ML Enthusiast

---

⭐ Acknowledgement

This project was developed as part of an educational initiative to explore Generative AI, Retrieval-Augmented Generation, Natural Language Processing, semantic search, vector databases and Large Language Models.
