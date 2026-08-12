<div align="center">

# LLM-AI-Projects

### Applied LLM & Generative AI Projects

Building practical AI applications using **LLMs, RAG, LangChain, embeddings, vector databases, NLP and document intelligence.**

<br>

**Student Profile Analyser**   •   **PDF Chatbot**

<br>

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square\&logo=python\&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-Framework-1C3C3C?style=flat-square)](https://www.langchain.com/)
[![RAG](https://img.shields.io/badge/RAG-Retrieval%20Augmented%20Generation-6C5CE7?style=flat-square)](#)
[![LLM](https://img.shields.io/badge/LLM-GenAI-FF6B6B?style=flat-square)](#)
[![Gradio](https://img.shields.io/badge/Gradio-Interface-F97316?style=flat-square\&logo=gradio\&logoColor=white)](https://www.gradio.app/)

</div>

---

## Overview

This repository contains two practical **LLM-powered applications** developed to explore how modern Generative AI systems can work with external information rather than relying solely on a model's pre-trained knowledge.

Both projects use concepts including:

* Large Language Models
* Retrieval-Augmented Generation (RAG)
* LangChain
* Text preprocessing
* Tokenization
* Document chunking
* Embeddings
* Vector databases / vector stores
* Semantic retrieval
* Prompt engineering
* API-based LLM integration
* Interactive Gradio interfaces

The projects demonstrate two different applications of the same underlying idea:

> **Process information → represent it semantically → retrieve relevant context → use an LLM to generate a useful response.**

---

# 01 · Student Profile Analyser

### AI-powered profile analysis & personalized career assistance

The **Student Profile Analyser** processes a student's profile, including information provided through a profile document/PDF, and uses AI to extract and analyse relevant information.

The system can interpret a student's background, skills, projects and experience and use that information to generate **personalized career-oriented outputs**, including cover letters tailored to specific company requirements.

### What it does

**Profile Analysis**

Reads and analyses the student's profile to identify relevant information such as:

* Education
* Technical skills
* Projects
* Experience
* Areas of expertise
* Relevant achievements
* Career-oriented information

**Company-Specific Cover Letters**

The system can generate a personalized cover letter based on:

> **Student Profile + Company Requirements → Tailored Cover Letter**

Rather than generating a generic cover letter, the system uses the candidate's actual profile and the requirements of the target company/role to produce a more relevant response.

### Core Pipeline

```text
Student Profile / PDF
          │
          ▼
   Document Processing
          │
          ▼
   Text Extraction
          │
          ▼
 Chunking & Preprocessing
          │
          ▼
     Embeddings
          │
          ▼
   Vector Representation
          │
          ▼
 Relevant Information Retrieval
          │
          ▼
       LLM + Prompt
          │
          ▼
 Profile Analysis / Cover Letter
```

### Key Features

| Feature                    | Description                                               |
| -------------------------- | --------------------------------------------------------- |
| 📄 Profile Processing      | Processes student profile information and documents       |
| 🔍 Information Retrieval   | Retrieves relevant profile information                    |
| 🧠 LLM Analysis            | Uses an LLM to analyse extracted information              |
| 🎯 Personalized Generation | Generates outputs based on the candidate's actual profile |
| 🏢 Company Adaptation      | Tailors cover letters to specific company requirements    |
| ✍️ Prompt Engineering      | Uses structured prompts for controlled generation         |
| 🔗 RAG Pipeline            | Grounds generation using retrieved profile information    |
| 💬 Interactive Interface   | Provides an accessible interface for interaction          |

### Technologies

`Python` · `LangChain` · `RAG` · `LLMs` · `Embeddings` · `Vector Database` · `NLP` · `Tokenization` · `Prompt Engineering` · `Gradio`

---

# 02 · PDF Chatbot

### Ask questions. Get answers directly from your documents.

The **PDF Chatbot** is a Retrieval-Augmented Generation system that allows users to upload a PDF document and interact with it using natural language.

Instead of asking an LLM to answer purely from its existing knowledge, the application first processes the document, retrieves the most relevant information, and then provides that information to the LLM as context.

This makes the system particularly useful for interacting with:

* Research papers
* Reports
* Study material
* Documentation
* Technical PDFs
* Books and notes
* Other text-based PDF documents

---

## How the PDF Chatbot Works

```text
             PDF
              │
              ▼
       Text Extraction
              │
              ▼
      Text Cleaning
              │
              ▼
    Document Chunking
              │
              ▼
        Tokenization
              │
              ▼
     Embedding Generation
              │
              ▼
       Vector Database
              │
              │
      ┌───────┴────────┐
      │                │
 User Question    Stored Chunks
      │                │
      ▼                │
 Query Embedding       │
      │                │
      └───────┬────────┘
              ▼
     Semantic Retrieval
              │
              ▼
     Relevant Context
              │
              ▼
       Prompt + Context
              │
              ▼
             LLM
              │
              ▼
       Final Answer
```

### Key Features

| Feature                 | Description                                             |
| ----------------------- | ------------------------------------------------------- |
| 📑 PDF Processing       | Reads and processes uploaded PDF documents              |
| ✂️ Chunking             | Splits large documents into manageable sections         |
| 🔤 Tokenization         | Processes text according to model/token constraints     |
| 🧬 Embeddings           | Converts text into semantic vector representations      |
| 🗄️ Vector Storage      | Stores document representations for efficient retrieval |
| 🔎 Semantic Search      | Finds contextually relevant sections of the document    |
| 🧠 RAG                  | Grounds LLM responses in retrieved document content     |
| 💬 Natural Language Q&A | Allows users to ask questions conversationally          |
| ⚡ LLM APIs              | Integrates external LLM providers through APIs          |
| 🖥️ Gradio UI           | Provides an interactive user interface                  |

---

# 🧠 Retrieval-Augmented Generation

RAG is the central architecture used across these projects.

Traditional LLM applications:

```text
User Question
      ↓
     LLM
      ↓
   Response
```

The RAG approach adds an external knowledge retrieval layer:

```text
User Question
      ↓
Query Embedding
      ↓
Vector Search
      ↓
Relevant Information
      ↓
Context + Question
      ↓
     LLM
      ↓
Grounded Response
```

This allows the application to work with information that is **specific to the user's documents or profile**.

---

# 🔬 Core Concepts

### Document Chunking

Large documents are divided into smaller chunks before embedding.

Chunking helps:

* Manage context-window limitations
* Improve retrieval granularity
* Reduce irrelevant information
* Provide focused context to the LLM

---

### Tokenization

Text is processed into tokens that can be understood and managed according to the requirements of the underlying language model.

Tokenization is particularly important when working with:

* Context windows
* Long documents
* Chunk sizes
* Prompt construction
* API usage limits

---

### Embeddings

Documents and queries are transformed into numerical vector representations that capture semantic meaning.

This enables the system to retrieve information based on **meaning rather than exact keyword matching**.

For example:

```text
"How much experience does the candidate have?"
```

can retrieve information related to:

```text
"Worked as an AI Engineer Intern for 6 months..."
```

even though the wording is different.

---

### Vector Database

The generated embeddings are stored in a vector database/vector store.

When a user asks a question, the query is embedded and compared against stored document vectors to identify the most relevant chunks.

```text
Documents
   ↓
Chunks
   ↓
Embeddings
   ↓
Vector Store
   ↓
Similarity Search
   ↓
Relevant Context
```

---

# 🔗 LangChain

LangChain is used to orchestrate different components of the LLM applications.

Depending on the pipeline, this includes:

* Document loaders
* Text splitters
* Embedding models
* Vector stores
* Retrievers
* Prompt templates
* LLM integrations
* Retrieval chains

The use of modular components makes it easier to experiment with different models, retrieval strategies and prompts.

---

# 🤖 LLM Integrations

The projects experiment with API-based LLM providers including:

### Groq

Used for high-speed inference with supported language models.

### Google Gemini

Used for LLM-based analysis and generation.

The applications are designed around API-based model access rather than requiring large language models to be hosted locally.

---

# 🔐 API Key Security

API keys are required for accessing external LLM services.

**API keys should never be committed to this repository.**

Instead, credentials should be provided through environment variables or notebook secrets.

Example:

```python
import os

GROQ_API_KEY = os.getenv("GROQ_API_KEY")
GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")
```

For Google Colab, API credentials can be stored using Colab's secret-management functionality rather than directly writing them into notebook cells.

---

# 🛠️ Technology Stack

<div align="center">

| Area            | Technologies                   |
| --------------- | ------------------------------ |
| Programming     | Python                         |
| LLM Framework   | LangChain                      |
| Architecture    | RAG                            |
| Models          | Groq, Google Gemini            |
| NLP             | Tokenization, Text Processing  |
| Retrieval       | Semantic Search                |
| Representation  | Embeddings                     |
| Storage         | Vector Database / Vector Store |
| Documents       | PDF Processing                 |
| Interface       | Gradio                         |
| Development     | Google Colab                   |
| Version Control | Git / GitHub                   |

</div>

---

# 📁 Repository Structure

```text
LLM-AI-Projects/
│
├── Student-Profile-Analyser/
│   ├── Student_Profile_Analyser.ipynb
│   └── README.md
│
├── PDF-Chatbot/
│   ├── PDF_Chatbot.ipynb
│   └── README.md
│
├── README.md
└── .gitignore
```

---

# ▶️ Running the Projects

The projects are currently provided as **Google Colab notebooks**.

Each notebook contains the implementation and can be opened directly in Colab.

### Student Profile Analyser

**[→ Open Student Profile Analyser in Google Colab](YOUR_COLAB_LINK_HERE)**

### PDF Chatbot

**[→ Open PDF Chatbot in Google Colab](YOUR_COLAB_LINK_HERE)**

> Some functionality requires API credentials for the configured LLM providers.

---

# 📌 Project Status

| Project                  | Status                   |
| ------------------------ | ------------------------ |
| Student Profile Analyser | ✅ Implemented            |
| PDF Chatbot              | ✅ Implemented            |
| RAG Pipeline             | ✅ Implemented            |
| Vector Retrieval         | ✅ Implemented            |
| LLM API Integration      | ✅ Implemented            |
| Interactive Interface    | ✅ Implemented            |
| Public Cloud Deployment  | ⏳ Not currently deployed |

---

# 🚧 Future Improvements

Potential extensions for these projects include:

* Improved retrieval strategies
* Hybrid keyword + semantic search
* Reranking retrieved documents
* Multi-document conversations
* Conversation memory
* Source citations
* RAG evaluation metrics
* Hallucination detection
* Streaming responses
* Persistent vector storage
* Cloud deployment
* Authentication
* Improved document parsing
* Automated evaluation pipelines

---

# 🎯 What These Projects Demonstrate

These projects were built to explore the practical engineering challenges involved in developing **LLM-powered applications beyond simple API calls**.

The implementations demonstrate experience with:

**LLMs → Prompt Engineering → Embeddings → Vector Search → RAG → Context Retrieval → Generation**

rather than treating an LLM as a standalone chatbot.

---

<div align="center">

### Built with Python · LangChain · RAG · Vector Search · LLMs

**Shambhavi Srivastavv**

*AI Engineer · Generative AI · LLM Applications*

</div>
