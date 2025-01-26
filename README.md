# Medical_QA

This project demonstrates a question-answering system built using LangChain and deployed using Streamlit. It leverages a vector database (FAISS) to retrieve relevant information from a collection of PDF documents and then uses a language model (ctransformers) to generate answers. Users can interact with the system through a chat-like interface.

**Project Structure:**

- **injest.py:** 
    - Loads PDF documents from the `data/` directory.
    - Splits the documents into smaller chunks.
    - Creates embeddings using a Hugging Face model (`sentence-transformers/all-MiniLM-L6-v2`).
    - Stores the embeddings and corresponding documents in a FAISS vector database.
- **model.py:**
    - Loads the FAISS vector database.
    - Loads the LLM (ctransformers) model.
    - Defines a retrieval QA chain using LangChain.
    - Provides a function (`qa_bot`) to handle user queries.
    - Includes a simple command-line interface for user interaction.
    - Includes a Chainlit chat interface for user interaction.

**Requirements:**

- Python 3.x
- langchain
- langchain_community
- faiss-cpu
- ctransformers
- chainlit
