# Medical-Knowledge-Assistant-using-RAG-and-LangChain
Built a medical question-answering system using LLaMA 2, LangChain, Sentence Transformers, and ChromaDB to retrieve relevant information from medical documents. Implemented RAG-based responses and evaluated answer groundedness and relevance.


##  Project Overview

The **Medical Knowledge Assistant** is a Generative AI project that explores how Large Language Models (LLMs) can answer medical questions using information retrieved from a medical reference document.

The project uses **LLaMA 2, LangChain, Hugging Face embeddings, and ChromaDB** to implement Retrieval-Augmented Generation (RAG). It also explores prompt engineering as a baseline for generating answers without retrieving information from the document.

##  Objectives

- Build a medical question-answering prototype using an LLM.
- Extract and process information from a medical reference PDF.
- Generate vector embeddings for document chunks.
- Retrieve relevant information using semantic similarity search.
- Generate answers using retrieved context.
- Explore answer groundedness and relevance evaluation.

##  Key Features

- **LLM Integration:** Uses LLaMA 2 for text generation.
- **Prompt Engineering:** Establishes a baseline for answering questions.
- **Document Processing:** Loads medical reference documents using PyMuPDF.
- **Text Chunking:** Splits documents into overlapping chunks for retrieval.
- **Semantic Search:** Uses sentence embeddings to identify relevant content.
- **Vector Database:** Stores document embeddings in ChromaDB.
- **Retrieval-Augmented Generation:** Combines retrieved context with user questions to generate answers.
- **Answer Evaluation:** Includes an experimental workflow for assessing groundedness and relevance.

##  Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Language Model | LLaMA 2 13B Chat |
| LLM Framework | LangChain |
| Embeddings | Sentence Transformers |
| Model and Embedding Access | Hugging Face |
| Vector Database | ChromaDB |
| PDF Processing | PyMuPDF |
| Data Processing | Pandas |
| Development Environment | Jupyter Notebook / Google Colab |

##  Project Workflow

1. **Initialize the LLM:** Load the LLaMA 2 language model.
2. **Create a baseline:** Generate answers using prompt engineering.
3. **Load the document:** Read the medical reference PDF.
4. **Split the text:** Divide the document into chunks of 1,000 characters with a 200-character overlap.
5. **Generate embeddings:** Convert text chunks into vector representations using `sentence-transformers/all-MiniLM-L6-v2`.
6. **Store embeddings:** Index the document chunks in ChromaDB.
7. **Retrieve context:** Search for relevant chunks based on the user's question.
8. **Generate responses:** Provide the retrieved context and question to LLaMA 2.
9. **Evaluate responses:** Explore whether generated answers are grounded in the retrieved content and relevant to the question.

##  Getting Started

### Prerequisites

- Python
- Jupyter Notebook or Google Colab
- Hugging Face account and appropriate access credentials
- Sufficient memory and storage for the language model
- The medical reference PDF used by the notebook

##  Evaluation

The notebook includes an experimental evaluation workflow focused on:

- **Groundedness:** Whether the generated answer is supported by the retrieved context.
- **Relevance:** Whether the answer addresses the question asked.

The evaluation pipeline may require additional work to extract reliable numerical scores. No validated clinical accuracy or medical safety claims are made.

##  Future Enhancements

- Improve retrieval accuracy and context selection.
- Include source references and page numbers in generated answers.
- Implement structured evaluation scores.
- Compare prompt-engineering and RAG-based responses systematically.
- Add error handling when relevant information is unavailable.
- Develop an interactive interface for question answering.
- Add automated tests and a reproducible dependency file.

##  Disclaimer

This project is intended for educational and demonstration purposes only. It is **not a medical diagnostic tool** and must not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult qualified healthcare professionals for medical concerns.


