# RAG Q&A Conversation with PDF including Chat History

This project is a Conversational Retrieval-Augmented Generation (RAG) application that allows users to upload PDF files, extract their content, and interact with the content through a chat interface. The application also maintains chat history for context-aware conversations.

## Features

- **PDF Uploads**: Users can upload one or more PDF files.
- **Content Extraction**: Extracts and processes the content of uploaded PDFs.
- **Conversational Interface**: Allows users to ask questions about the content of the PDFs.
- **Chat History**: Maintains chat history for context-aware question answering.
- **Customizable LLM**: Uses the Groq API for language model interactions.
- **Embeddings**: Utilizes HuggingFace embeddings for document vectorization.

## How It Works

1. **PDF Upload**: Users upload PDF files via the Streamlit interface.
2. **Content Processing**:
   - The content of the PDFs is split into chunks using `RecursiveCharacterTextSplitter`.
   - Embeddings are created for the chunks using HuggingFace models.
   - A vector store is created using Chroma for efficient retrieval.
3. **Question Answering**:
   - Questions are reformulated to be standalone using a history-aware retriever.
   - The system retrieves relevant content from the PDFs and generates concise answers.
4. **Chat History**:
   - Chat history is stored and used to provide context for follow-up questions.

## Requirements

Install the dependencies listed in `requirements.txt`:

```bash
pip install -r [requirements.txt]
