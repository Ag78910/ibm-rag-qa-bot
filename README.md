#  Final Project: Build a RAG AI Assistant using LangChain & IBM watsonx.ai

This repository contains my **final project** for the **IBM AI Engineer Professional Certificate**.  
It demonstrates how to build a **Retrieval-Augmented Generation (RAG)** Question Answering (QA) assistant using **LangChain**, **IBM watsonx.ai**, and **Gradio**.

---

##  Author
**Alejandro Galindo Valencia**  
*IBM AI Engineer Professional Certificate — Capstone Project*

---

##  Project Overview

This project implements a **PDF Question-Answering Bot** capable of answering user queries based on the content of an uploaded document.  

The architecture combines:
- **IBM watsonx.ai** LLMs for natural language generation.
- **LangChain** for document management and retrieval orchestration.
- **ChromaDB** for vector storage and similarity search.
- **Gradio** for an easy-to-use web interface.

---

##  RAG Pipeline

1. **Document Upload** – The user uploads a PDF.
2. **Text Splitting** – The PDF is divided into overlapping text chunks.
3. **Embedding Generation** – Chunks are converted into vector embeddings using **Watsonx Embeddings**.
4. **Vector Store** – Embeddings are stored and indexed in **ChromaDB**.
5. **Retrieval + Generation** – The system retrieves relevant chunks and generates an answer using a **watsonx.ai LLM**.

---

##  Features

-  PDF document upload  
-  Text chunking for efficient retrieval  
-  Semantic search via ChromaDB  
-  AI-powered responses using IBM watsonx.ai  
-  Simple, interactive Gradio web interface  

---

##  Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/Ag78910/ibm-rag-qa-bot.git
   cd ibm-rag-qa-bot
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

##  How to Run Locally

1. Open the Jupyter Notebook:  
   `Final Project Build a RAG AI Assistant using LangChain.ipynb`

2. Run all cells to start the Gradio interface.

3. Alternatively, export the logic into a Python file (`app.py`) and run:
   ```bash
   python app.py
   ```

4. Open your browser and navigate to:  
    [http://localhost:7860](http://localhost:7860)

---

##  Security Note

The app can be launched locally with:
```python
rag_application.launch()
```

This is completely **safe**, as it only runs on your own machine.  

If you uncomment the following line:
```python
# rag_application.launch(server_name="0.0.0.0", server_port=7860)
```
the app will become accessible **within your local network only** (e.g., other devices on the same Wi-Fi).  
This does **not expose your computer to the internet**, unless you manually open that port in your router/firewall.

---

##  Requirements

```text
ibm-watsonx-ai
langchain
langchain-ibm
langchain-community
chromadb
pypdf
gradio
```

---

##  Example Usage

1. Upload a PDF document.
2. Type a question related to its content.
3. The AI assistant will generate an answer based on retrieved document chunks.

---

##  License

This project was developed for educational purposes as part of the  
**IBM AI Engineer Professional Certificate**.

Feel free to fork, explore, and learn from it! 

---

*Happy Building!*   
— *Alejandro Galindo Valencia*
