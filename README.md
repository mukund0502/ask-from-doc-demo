# Ask From Doc - Demo Application

Ask From Doc is a **document-based Question Answering (QA) application** that allows you to interact with your own documents using natural language queries. This repository provides a demo implementation showcasing how the application works.

## Features
- Supports multiple file formats: **PDF, DOCX, TXT, Images**
- Offers three modes of interaction:
  1. **Save to DB** – Upload a document and save its processed content into a database for future queries  
  2. **Ask Query from Document** – Upload a document and instantly ask questions about it without saving  
  3. **Just Ask Query** – Directly ask questions without uploading any document (uses pre-saved data if available)  

## How It Works
1. The user uploads a file (PDF, DOCX, Text, or Image).  
2. The document’s content is extracted and processed (OCR for images is supported).  
3. Depending on the selected mode:
   - In **Save to DB**, the processed data is stored in a vector database for future queries.  
   - In **Ask Query from Document**, the system directly processes the file and returns results.  
   - In **Just Ask Query**, the user can query data already stored in the database.  
4. The application uses **Retrieval-Augmented Generation (RAG)** to fetch relevant information and provide contextual answers.

## Tech Stack
- **Python** (FastAPI / Streamlit for demo interface)  
- **LangChain** for orchestration  
- **Vector Database** (e.g., FAISS, Chroma, or Azure Cognitive Search integration)  
- **LLM Backend**  Azure OpenAI 
- **OCR**: Tesseract for image-based text extraction  
