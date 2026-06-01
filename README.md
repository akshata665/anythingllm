# AnythingLLM – Retrieval-Augmented Generation (RAG) Document Assistant

## Overview

AnythingLLM is an AI-powered Retrieval-Augmented Generation (RAG) platform that enables users to upload documents and interact with them through a conversational chatbot interface.

The system processes uploaded documents, generates vector embeddings, stores them in a vector database, retrieves relevant information based on user queries, and uses Large Language Models (LLMs) to generate context-aware responses.

This deployment has been configured using Docker and integrated with Groq/Ollama models for efficient document-based question answering.

---

## Key Features

### Document Intelligence

* Upload PDF, DOCX, TXT, CSV, and Markdown files
* Automatic document parsing and text extraction
* Intelligent document chunking
* Embedding generation and vector indexing

### AI Chat Interface

* Natural language conversations
* Context-aware responses
* Multi-thread conversations
* Workspace-based document management

### Retrieval-Augmented Generation (RAG)

* Semantic vector search
* Relevant context retrieval
* Grounded AI responses
* Reduced hallucinations

### Model Integration

* Groq LLM support
* Ollama local model support
* OpenAI-compatible providers
* Flexible model switching

### Deployment

* Docker-based deployment
* Local execution
* Multi-platform support
* Simple configuration

---

# System Architecture

```text
User Query
     │
     ▼
Document Retrieval
     │
     ▼
Vector Similarity Search
     │
     ▼
Relevant Context Extraction
     │
     ▼
LLM Processing
     │
     ▼
Generated Response
```

---

# RAG Workflow

```text
Document Upload
       │
       ▼
Text Extraction
       │
       ▼
Chunk Creation
       │
       ▼
Embedding Generation
       │
       ▼
Vector Storage
       │
       ▼
User Query
       │
       ▼
Semantic Retrieval
       │
       ▼
LLM Response
```

---

# Technology Stack

| Component        | Technology        |
| ---------------- | ----------------- |
| Frontend         | React             |
| Backend          | Node.js           |
| AI Models        | Groq, Ollama      |
| Vector Database  | LanceDB           |
| Containerization | Docker            |
| Retrieval Engine | RAG Pipeline      |
| Embeddings       | Vector Embeddings |

---

# Installation

## Prerequisites

Install:

* Docker Desktop
* Git
* Groq API Key (Optional)
* Ollama (Optional for local inference)

---

## Clone Repository

```bash
git clone https://github.com/akshata665/anythingllm.git
cd anythingllm
```

---

## Configure Environment

Navigate to:

```bash
cd docker
```

Create environment file:

```bash
copy .env.example .env
```

---

## Start Application

```bash
docker compose up -d
```

Verify:

```bash
docker ps
```

Expected output:

```text
anythingllm   Up (healthy)
```

---

## Access Application

Open:

```text
http://localhost:3001
```

---

# Configure AI Provider

## Groq

1. Navigate to Settings → AI Providers
2. Select Groq
3. Enter API Key
4. Choose model
5. Save Changes

## Ollama

Install model:

```bash
ollama pull llama3
```

Run:

```bash
ollama serve
```

Configure:

```text
Provider: Ollama
URL: http://host.docker.internal:11434
Model: llama3
```

---

# Usage

## Create Workspace

Create a workspace to organize documents and conversations.

## Upload Documents

Supported formats:

* PDF
* DOCX
* TXT
* CSV
* Markdown

## Generate Embeddings

Select uploaded document and click:

```text
Embed File
```

## Ask Questions

Example:

```text
Summarize this document
```

```text
What are the key concepts discussed?
```

```text
Generate interview questions from this document
```

```text
Explain Unit 1 in simple terms
```

---

# Sample Use Cases

### Education

* Study material chatbot
* Question answering
* Notes summarization

### Research

* Literature review assistant
* Knowledge retrieval

### Enterprise Knowledge Management

* Internal document search
* SOP retrieval
* Technical documentation assistant




---

# License

This project is intended for educational, research, and document intelligence applications.
