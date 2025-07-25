🧠 Gemini RAG Chatbot with Reinforcement Learning :: Live link : https://iris-navy.vercel.app/
This project is an AI-powered chatbot that leverages Google's Gemini LLM, retrieval-augmented generation (RAG), and Q-learning to provide highly relevant, context-aware responses from a custom document database.

The system uses semantic search powered by FAISS, dynamically optimized through reinforcement learning, and served through a FastAPI backend and a modern Next.js frontend.

This chatbot can be used to build intelligent assistants for tasks like internal documentation Q&A, educational tutors, customer support, and more.

⚙️ Tech Stack
Layer	Technology	Purpose
Frontend	Next.js, shadcn/ui, Tailwind CSS	User interface for chatting
Backend	FastAPI	API logic, semantic search, RL processing
LLM	Google Gemini API	Generates human-like answers from retrieved context
RAG Framework	LangChain	Constructs prompts and handles LLM flow
Embeddings	Gemini Embeddings / SentenceTransformers	Converts chunks into vectors for similarity search
Database	FAISS	Fast semantic search over document embeddings
Reinforcement Learning	Q-Learning	Dynamically adjusts chunking strategy to optimize answers
OCR (Optional)	Tesseract	Reads text from PDF/images if needed
Environment	.env + python-dotenv	Manages API keys and sensitive configuration

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
