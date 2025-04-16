# RAG Chatbot with Conversational Memory

## Overview
This project implements a Retrieval-Augmented Generation (RAG) chatbot using Google Gemini, LangChain, and Chroma. It supports both basic and session-aware responses with conversational memory and optimized response time. The chatbot can ingest and process external documents to answer user queries based on relevant context.

## Features
- Built two types of RAG chains:
  - **Basic RAG Chain** without memory
  - **Conversational RAG Chain** with session-based memory
- Used Google Gemini as the language model backend
- Retrieved relevant information using a Chroma vector store
- Embedded text chunks using Gemini embeddings
- Parsed and chunked external documents with RecursiveCharacterTextSplitter
- Added session ID and chat history support using LangChain’s memory components
- Evaluated both chains on four representative queries
- Measured success rate, word count, response time, and performance improvements
- Achieved a **100% success rate** in answering test queries
- Reduced query processing time by **22.26%** compared to the baseline

## How to Run
1. Install dependencies:
   ```bash
   pip install langchain chromadb google-generativeai
   ```

2. Set up your environment:
   ```bash
   export GOOGLE_API_KEY="your_api_key_here"
   ```

3. Run the script:
   ```bash
   python main.py
   ```

4. Review logs and evaluation results in the terminal output.

## Evaluation Metrics
- **Total queries tested:** 4  
- **Success rate:** 100%  
- **Average response time (Basic):** ~1.097 sec  
- **Average response time (Conversational):** ~0.853 sec  
- **Time improvement:** 22.26% from baseline  

## Notes
- The chat history is passed as a list to avoid prompt formatting errors.
- Session ID is used for tracking conversation context across multiple queries.
