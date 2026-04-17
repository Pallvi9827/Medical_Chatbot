# Medical RAG Chatbot Prototype

This project is a prototype Retrieval-Augmented Generation (RAG) chatbot for answering medical questions from a medical PDF knowledge source.

## Project Overview

The notebook demonstrates an end-to-end RAG workflow:

- Load medical PDF documents
- Extract and preprocess document text
- Split text into smaller chunks
- Generate embeddings using Sentence Transformers
- Store and retrieve vectors using Pinecone
- Build a retriever for semantic search
- Create a question-answering chain using LangChain and OpenAI

## Tech Stack

- Python
- Jupyter Notebook
- LangChain
- PyPDF
- Sentence Transformers
- Pinecone
- OpenAI API

## Workflow

1. Load PDF documents from the `data/` folder
2. Extract text using `PyPDFLoader`
3. Clean and reduce document metadata
4. Split long text into smaller chunks
5. Generate embeddings with `all-MiniLM-L6-v2`
6. Store chunk embeddings in Pinecone
7. Retrieve top relevant chunks for a user query
8. Use an LLM with retrieved context to answer questions

## Project Structure

```text
MEDICAL_CHATBOT/
│
├── data/
│   └── Medical_book.pdf
├── research/
│   └── trials.ipynb
├── .gitignore
├── LICENSE
├── requirements.txt
└── README.md
```
## Example Query
The retriever was tested with sample queries such as:
	•	What is Acne?
	•	What is Acromegaly and gigantism?

## Important Note
The final LLM response generation cell is commented out in the uploaded notebook because it requires active OpenAI API billing/credits.

The retrieval pipeline, embeddings, Pinecone indexing, retriever setup, and QA chain construction are implemented in the notebook.

## Status
Prototype notebook version for demonstrating a medical RAG chatbot pipeline.

## Future Improvement
	•	Build a FastAPI backend
	•	Add a frontend UI
	•	Replace notebook code with modular Python scripts
	•	Add source citations in final answers
	•	Deploy as a web application

## Author
Pallvi..... Machine Learning / AI Student


