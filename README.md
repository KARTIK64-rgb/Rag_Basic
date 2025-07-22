# Basic RAG with LangChain and Google Gemini

This notebook demonstrates a simple Retrieval-Augmented Generation (RAG) setup using LangChain and Google Gemini.

## Project Overview

The goal of this project is to build a basic RAG pipeline that allows you to ask questions about documents using a language model. It combines document retrieval with powerful generation capabilities to produce accurate, context-aware answers.

## Workflow

1. **Document Loading**  
   Load a `.txt` file using LangChain's `TextLoader`.

2. **Text Splitting**  
   The document is split into smaller, manageable chunks using a character splitter. This ensures better embedding and retrieval performance.

3. **Embeddings**  
   Convert each chunk into vector format using Hugging Face's `all-MiniLM-L6-v2` embedding model.

4. **Vector Store (FAISS)**  
   Store the embedded vectors in a FAISS index, enabling fast and efficient similarity search.

5. **Retriever Setup**  
   Use the FAISS vector store to retrieve chunks that are most relevant to the input query.

6. **LLM (Google Gemini)**  
   The retrieved chunks and the user question are passed into the Google Gemini model (`gemini-1.5-flash-latest`) using LangChain's `ChatGoogleGenerativeAI`.

7. **Answer Generation**  
   Gemini processes the question and context to generate a relevant and concise answer.

## Result

You can input any question related to the content of the document, and the system will retrieve the most relevant parts and use Google Gemini to answer it.

---

This setup is useful for building custom document Q&A systems, intelligent chatbots, or knowledge assistants using your own data.
