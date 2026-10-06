# 🎓 ERM Tutor-AI: A RAG-Based Educational Tutor

This project was initially completed and presented in November 2025, during which the system was running exclusively in a local environment. In October 2026, the source code and database were published to GitHub and deployed via Streamlit Cloud, allowing its functionality to be accessed and tested directly online.

Developed as part of a thesis project for the Master of Educational Technology program at Saarland University[cite: 3], this project integrates Generative Artificial Intelligence (GAI) with the Retrieval-Augmented Generation (RAG) framework to create an interactive AI tutor assistant for students taking the Empirical Research Methods (ERM) course.

---

## 📖 Background and Problem Statement

Although Large Language Models (LLMs) possess remarkable generative capabilities, they are prone to "hallucinations"—a phenomenon where the AI generates information that sounds plausible but is factually incorrect or unfounded. In a higher education context that demands strict precision, these inaccuracies can mislead students and disrupt the learning process[cite: 32]. 

To mitigate this risk, ERM Tutor-AI combines the capabilities of a GPT-based model with a curated knowledge database containing validated ERM course materials and literature[cite: 11]. By leveraging the RAG architecture, the system is forced to retrieve information directly from official course materials before generating a response, ensuring that the provided answers are always accurate, contextually relevant, and free from misinformation[cite: 11].

---

## 🛠️ Technology Stack

*   **Frontend / UI:** Streamlit[cite: 57] for building an interactive, user-friendly web interface that facilitates real-time dialogue[cite: 61, 62].
*   **Large Language Model (LLM):** OpenAI GPT-4o accessed via API for advanced natural language understanding and generation[cite: 57, 58].
*   **Orchestration Framework:** LangChain to manage the data flow between the user interface, the vector database, and the LLM[cite: 60].
*   **Vector Database:** ChromaDB[cite: 57] for storing embedded text chunks and performing efficient semantic similarity searches[cite: 60].
*   **Embeddings:** `sentence-transformers` (via Hugging Face) to convert text chunks into high-dimensional numeric representations to capture semantic meaning[cite: 58].
*   **Document Parsing:** Markitdown for extracting structured metadata from course PDFs to ensure high searchability and transparency[cite: 60].

---

## 📂 Project Structure

```text
erm_tutorai/
│
├── chroma_db/                 # Pre-built vector database containing ERM course embeddings
├── src/
│   ├── RAG_ChatBot.py         # Backend logic, LLM integration, and RAG pipeline
│   └── streamlit.py           # Frontend UI, chat interface, and session state management
│
├── logo_ermai.png             # Application logo and visual assets
├── requirements.txt           # List of project dependencies
└── README.md                  # Project overview and instructions
