# Medical-chatbot

A **Retrieval-Augmented Generation (RAG) medical chatbot** built with **Flask, Pinecone, and Groq LLM**. This project allows users to ask health-related questions and receive accurate, context-aware answers from a curated medical knowledge base.

---

## 🚀 Features

* **Flask Web App** – User-friendly interface for real-time chat.
* **RAG Pipeline** – Uses a retriever to fetch context from a Pinecone vector database.
* **LLM Integration** – Powered by **Groq's `gemma2-9b-it` model** for intelligent, conversational responses.
* **Similarity Search** – Ensures top-3 relevant chunks are retrieved for precise answers.
* **Environment Secure** – API keys and configurations are stored using `.env` for safety.
## 📂 Project Structure

```
Medical-chatbot/
│
├── app.py                # Main Flask application
├── src/
│   ├── helper.py         # Helper functions (e.g., downloading embeddings)
│   ├── prompt.py         # System and conversation prompts
│
├── templates/
│   └── index.html        # Frontend interface
│
├── .env                  # Environment variables (API keys)
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

---

## ⚙️ Setup and Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/palakbansal8810/Medical-chatbot.git
cd Medical-chatbot
```

### 2️⃣ Create and Activate Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Set Up Environment Variables

Create a `.env` file in the root directory:

```bash
PINECONE_API_KEY=your_pinecone_api_key
GROQ_API_KEY=your_groq_api_key
```

### 5️⃣ Run the Application

```bash
python app.py
```

Visit the app at **[http://localhost:8000](http://localhost:8000)** in your browser.

---

## 🧠 How It Works

1. **User Query** → User inputs a medical question.
2. **Retriever** → Searches Pinecone for similar, relevant embeddings.
3. **LLM Chain** → Groq LLM uses the retrieved content to generate a contextual answer.
4. **Response** → The chatbot displays the answer on the web interface.

---


