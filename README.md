# Pharma Chatbot

An AI-powered pharmaceutical chatbot built to answer medicine and healthcare-related queries using a retrieval-based question answering workflow.

This project transforms pharmaceutical reference documents into a searchable knowledge base and delivers contextual responses through a chatbot interface powered by large language models, vector search, and document retrieval.

---

## Project Summary

**Built an intelligent pharmaceutical question-answering system** by creating a chatbot that retrieves relevant medical knowledge before generating responses.

**Enabled users to ask medicine-related questions in natural language** and receive context-aware answers grounded in document-based knowledge.

**Did this by** combining PDF ingestion, text chunking, embedding generation, vector indexing with Pinecone, and LLM-based response generation using LangChain and OpenAI.

---

## Objective

**Improved access to pharmaceutical information** by developing a chatbot that can respond to domain-specific user queries using a structured document retrieval pipeline.

**Created a retrieval-augmented chatbot system** to reduce hallucinations and improve answer relevance for medicine-related conversations.

**Did this by** loading pharmaceutical documents, converting them into embeddings, storing them in a vector database, and using semantic retrieval to supply context to the language model.

---

## Problem Statement

Users often struggle to find quick, understandable, and relevant answers to pharmaceutical and medicine-related questions from large reference documents.

The goal of this project was to build a chatbot that can:

- understand natural language questions
- retrieve the most relevant pharmaceutical knowledge
- generate contextual answers from trusted source material
- provide a smoother and more interactive healthcare information experience

---

## Solution Overview

**Delivered a document-grounded pharma chatbot** by building a retrieval-based architecture for question answering.

**Connected user queries with relevant pharmaceutical knowledge** instead of relying only on direct model memory.

**Did this by** creating a workflow that:
- loads source documents
- splits content into searchable chunks
- converts chunks into embeddings
- stores embeddings in Pinecone
- retrieves relevant context for each query
- sends the retrieved context to the LLM for final answer generation

---

## Core Workflow

### 1. Document Ingestion
**Converted raw pharmaceutical content into machine-readable input** for the chatbot pipeline.

**Loaded source documents for downstream processing** so the chatbot could answer from domain-specific knowledge.

**Did this by** using document loaders to read PDF-based content and prepare it for chunking and embedding.

### 2. Text Processing
**Improved retrieval quality** by structuring large documents into manageable semantic units.

**Split long pharmaceutical text into smaller chunks** to make retrieval more precise and context windows more efficient.

**Did this by** applying text-splitting logic before embedding generation.

### 3. Embedding and Vector Storage
**Created a searchable semantic knowledge base** for pharma-related information retrieval.

**Converted text chunks into vector embeddings** and stored them in a Pinecone vector database.

**Did this by** using embedding models through LangChain and indexing the output in Pinecone for fast similarity search.

### 4. Retrieval-Augmented Generation
**Improved answer relevance and grounding** by retrieving supporting knowledge before generating responses.

**Used retrieved context to answer user questions** instead of depending only on the language model’s internal memory.

**Did this by** connecting vector search results to the LLM prompt pipeline through LangChain.

### 5. Chatbot Interface
**Turned the retrieval system into an interactive application** users can query directly.

**Built an app layer for question answering** so users can ask medicine-related questions in a simple chatbot-style interface.

**Did this by** wiring the retrieval and generation pipeline into the main application file and serving responses through the chatbot frontend/backend flow.

---

## Key Features

**Delivered a practical AI healthcare assistant experience** through a document-aware chatbot system.

**Enabled end users to query pharmaceutical knowledge interactively** with better relevance than plain keyword search.

**Did this by** implementing:
- PDF-based knowledge ingestion
- semantic document retrieval
- Pinecone vector indexing
- OpenAI-powered answer generation
- LangChain orchestration
- environment-based API key management

---

## Tech Stack

- Python
- LangChain
- OpenAI API
- Pinecone
- Flask or app-based Python interface
- PDF document loaders
- Vector embeddings
- Retrieval-augmented generation

---

````markdown
# Medical ChatBot Using LLM 🧠, LangChain 🦜, Pinecone ⚛

### Tech Stack

- Python
- LangChain
- Flask
- GPT
- Pinecone
- RAG

### Flowchart

<p align="center">
  <img src="https://github.com/omkar-dharkar/Pharma_ChatBot/blob/main/FlowChart.png" height="900" width="1000"/>
</p>

## Setup and Run

### 1. Clone the repository

```bash
gh repo clone omkar-dharkar/Pharma_ChatBot
cd Pharma_ChatBot
````

### 2. Create and activate the conda environment

```bash
conda create -n medicalbot python=3.10 -y
conda activate medicalbot
```

### 3. Install the requirements

```bash
pip install -r requirements.txt
```

### 4. Create a `.env` file in the root directory

Add your Pinecone and OpenAI credentials like this:

```ini
PINECONE_API_KEY="xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY="xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### 5. Store embeddings in Pinecone

```bash
python store_index.py
```

### 6. Run the application

```bash
python app.py
```

### 7. Open in browser

```bash
http://localhost:8080
```

```
```
