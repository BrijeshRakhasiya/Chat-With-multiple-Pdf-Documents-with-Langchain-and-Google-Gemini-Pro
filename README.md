# 📚 Chat With Multiple PDF Documents using LangChain and Google Gemini Pro

This project enables users to **chat with multiple PDF files** using **LangChain**, **FAISS**, and **Google Gemini Pro (Gemini 1.5 Pro)**. It extracts, indexes, and retrieves relevant information from uploaded PDF files to answer user queries conversationally.

---

## 🚀 Features

- 🔍 Upload multiple PDF documents
- 🧠 Semantic search powered by Google Generative AI Embeddings
- 🗂️ Vector storage using FAISS
- 💬 Natural language query answering via Gemini Pro
- 🌐 Streamlit web interface

---

## 🧱 Tech Stack

- Python 🐍
- [Streamlit](https://streamlit.io/) — UI Framework
- [LangChain](https://www.langchain.com/) — Framework for LLM-powered apps
- [FAISS](https://github.com/facebookresearch/faiss) — Vector similarity search
- [Google Generative AI (Gemini)](https://ai.google.dev/) — Embedding and chat model
- PyPDF2 — For PDF text extraction
- python-dotenv — For managing API keys securely

---

## ⚙️ How It Works

1. **Upload PDFs**: Use the Streamlit sidebar to upload one or more PDF files.
2. **Text Extraction**: The content of the PDFs is extracted using `PyPDF2`.
3. **Chunking**: The raw text is split into chunks using `RecursiveCharacterTextSplitter`.
4. **Vectorization**: Each chunk is converted into vector embeddings using Gemini's embedding model (`embedding-001`).
5. **Vector Store**: FAISS is used to store and retrieve relevant chunks based on user queries.
6. **Question Answering**: A prompt-driven Q&A chain powered by Gemini Pro generates responses based on relevant document context.

---

## 🖥️ How to Run Locally

1. **Clone the repository**:
    ```bash
    git clone https://github.com/BrijeshRakhasiya/Chat-With-multiple-Pdf-Documents-with-Langchain-and-Google-Gemini-Pro.git
    cd chat-with-multiple-pdfs-gemini
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Setup Environment Variables**:

    Create a `.env` file in the root directory and add your Google Generative AI API key:
    ```
    GOOGLE_API_KEY=your_google_api_key
    ```

4. **Run the Streamlit app**:
    ```bash
    streamlit run app.py
    ```

---

## 📝 Example Prompt

> 📄 Upload 3–4 PDF files  
> 💬 Ask: "What are the main findings in the second report?"  
> 🤖 The model will retrieve the relevant context and provide a detailed answer.

---


---

## 🔐 API Key Required

Make sure you have access to the **Google Generative AI API** and create a `.env` file as shown above.

---

## 📌 Notes

- The app does not hallucinate: If an answer isn’t in the PDFs, it will respond with _"Answer is not available in the context."_
- Ideal for document-based question answering, compliance checks, and multi-doc research.

---



## 🙌 Author

**Brijesh Rakhasiya**  
💼 AI/ML Enthusiast | 💡 Tech Innovator | 🚀 Builder

---

## 📜 License

This project is licensed under the **GNU General Public License (GPL)**.  
You are free to use, modify, and distribute this software under the terms of the [GNU GPL](https://www.gnu.org/licenses/gpl-3.0.en.html).

---
