🧠 Gemini RAG Chatbot with Reinforcement Learning :: Live link : https://iris-navy.vercel.app/

This project is an AI-powered chatbot that leverages Google's Gemini LLM, retrieval-augmented generation (RAG), and Q-learning to provide highly relevant, context-aware responses from a custom document database.

The system uses semantic search powered by FAISS, dynamically optimized through reinforcement learning, and served through a FastAPI backend and a modern Next.js frontend.

This chatbot can be used to build intelligent assistants for tasks like internal documentation Q&A, educational tutors, customer support, and more.

## 🧰 Tech Stack

| Layer        | Technology Used                         | Description                                                                 |
|--------------|------------------------------------------|-----------------------------------------------------------------------------|
| **Frontend** | Next.js + TypeScript + shadcn/ui         | Modern React-based frontend with elegant UI components                     |
| **Backend**  | FastAPI                                   | Fast and scalable backend serving API requests                             |
| **LLM API**  | Google Gemini Pro (via `google-generativeai`) | Used for chat, vision, and natural language processing tasks                |
| **RAG**      | LangChain + FAISS                         | For Retrieval-Augmented Generation and semantic document retrieval         |
| **Learning** | Q-Learning Agent                          | Dynamically tunes chunk size & retriever logic for improved performance     |
| **File Input** | PyMuPDF / pdfplumber / python-docx     | Parses PDF and DOCX files for knowledge ingestion                          |
| **Storage**  | FAISS Vector DB                           | Stores embeddings for fast similarity-based search                         |
| **Embedding**| Gemini Embeddings                         | Vector representations of text chunks                                      |
| **UI Host**  | Streamlit (for internal testing only)     | Optional rapid prototyping for testing ML logic               

📄 Published Paper
📘 This project is backed by research!
Read our published paper here: https://ijsrem.com/download/gen-ai-based-chatbot-on-top-of-llama-for-ssr-documents/

Perfect. Here's an additional **"🚀 Getting Started"** section that shows **how to set up the full project (frontend + backend + .env)**. I'll combine it into the final README afterward:

---

## 🚀 Getting Started

Follow these steps to run the **Gemini RAG Chatbot with RL** on your local machine.

### 🔐 1. Clone the Repository

```bash
git clone https://github.com/Aaryansingh20/Rag-chat.git
cd rag-chat
```

---

### 📦 2. Backend Setup (FastAPI)

#### ⬇️ Install dependencies

Make sure you have Python 3.10+ and `pip` installed.

```bash
python -m venv venv
source venv/bin/activate  # or `venv\Scripts\activate` on Windows
pip install google-generativeai
pip install -r requirements.txt
```

#### 🔑 Create `.env` file

Inside the `backend` folder, create a `.env` file:

```env
GEMINI_API_KEY="your_gemini_api_key"

```

#### 🚀 Start the backend server

```bash
uvicorn api:app --reload
```

> The FastAPI server will run at `http://localhost:8000`

---

### 🌐 3. Frontend Setup (Next.js + shadcn/ui)

#### ⬇️ Install dependencies

```bash
cd rag-frontend
npm install
```

#### 🔑 Create `.env.local` file

Inside the `frontend` folder:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

#### 🏁 Start the frontend dev server

```bash
npm run dev
```

> The frontend will be available at `http://localhost:3000`

---
