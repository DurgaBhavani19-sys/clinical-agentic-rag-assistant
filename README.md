# Clinical Agentic RAG Assistant

A production-style multi-agent Retrieval-Augmented Generation (RAG) system designed to demonstrate how agentic AI can retrieve trusted knowledge, generate grounded responses, validate outputs, and expose the workflow through an API.

> Portfolio Project: This is an independent implementation built with public/synthetic data to demonstrate production AI engineering patterns. It does not contain proprietary employer code, data, or internal systems.

## Project Overview

AI assistants used in high-stakes domains need more than a single LLM prompt. They need reliable retrieval, source grounding, validation, safety controls, and observable workflows.

This project implements a multi-agent architecture in which specialized agents collaborate to process a user request.

## Architecture

The system follows this workflow:

User Query  
↓  
Orchestrator  
↓  
Retrieval Agent  
↓  
Vector Database / Knowledge Base  
↓  
Drafting Agent  
↓  
Safety & Compliance Agent  
↓  
Grounded Response + Source Citations

The orchestration layer manages state and determines how requests move between specialized agents.

## Core Agents

### Retrieval Agent
Retrieves relevant document chunks from the knowledge base using semantic search.

### Drafting Agent
Uses retrieved context to generate a grounded response while maintaining references to source material.

### Safety & Compliance Agent
Reviews generated responses for unsupported claims, unsafe output, and policy violations before returning the final response.

### Orchestrator
Coordinates agent execution, maintains workflow state, and controls transitions between agents.

## Key Features

- Multi-agent workflow orchestration
- Retrieval-Augmented Generation (RAG)
- Semantic document retrieval
- Vector-based knowledge search
- Source-grounded responses
- Safety and validation layer
- Structured citations
- RAG evaluation
- REST API using FastAPI
- Docker containerization
- Automated testing
- CI/CD with GitHub Actions

## Technology Stack

**Language**
- Python

**Generative AI**
- LLM APIs
- LangChain
- LangGraph

**Retrieval**
- Embeddings
- Vector search
- FAISS / Pinecone-compatible architecture

**Evaluation**
- RAGAS-style retrieval and response evaluation
- Groundedness and relevance testing

**API & Deployment**
- FastAPI
- Docker
- GitHub Actions

## Planned Repository Structure

```text
clinical-agentic-rag-assistant/
├── src/
│   ├── agents/
│   ├── rag/
│   ├── guardrails/
│   ├── tools/
│   └── api/
├── data/
│   └── sample/
├── evaluation/
├── tests/
├── architecture/
├── .github/
│   └── workflows/
├── requirements.txt
├── Dockerfile
└── README.md
## Disclaimer

This repository is an independent portfolio project created for educational and demonstration purposes. It uses public or synthetic data and does not contain confidential healthcare information, PHI, proprietary employer code, or internal company architecture.
