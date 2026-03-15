# Enterprise-Knowledge-Graph-RAG 🕸️🔍

A production-grade **Retrieval-Augmented Generation (RAG)** pipeline that leverages **Knowledge Graphs** to enable multi-hop reasoning and high-precision information retrieval from complex enterprise data.

This project is built based on my experience at **Tata Consultancy Services (TCS)**, where I developed advanced RAG systems for enterprise-scale data retrieval.

## 🌟 Why Knowledge Graphs for RAG?
Standard vector-only RAG often fails at:
- **Multi-hop reasoning**: "Find all policies for a customer who lives in a specific region and has a history of X."
- **Contextual relationships**: Understanding hierarchies and semantic links between entities.
- **Explainability**: Tracing exactly which relationships led to an answer.

This engine solves these by combining **Vector Search** (for semantic similarity) with **Graph Traversal** (for structural context).

## 🚀 Key Features
- **Hybrid Retrieval**: Seamlessly combines Neo4j graph queries with Pinecone vector search.
- **GraphRAG Architecture**: Extracts entities and relationships from unstructured documents to build a dynamic graph.
- **Multi-Agent Orchestration**: Specialized agents for query decomposition and graph traversal.
- **Enterprise-Grade**: Support for high-volume data ingestion and complex schema mapping.

## 🛠 Tech Stack
- **Graph DB**: Neo4j (Cypher query language)
- **Vectors**: Pinecone / ChromaDB
- **Frameworks**: LangChain, LangGraph, Pydantic
- **Models**: Google Gemini 1.5 Pro, Claude 3.5 Sonnet
- **Orchestration**: Python 3.11+

## 🏗 Implementation Strategy
1. **Extraction**: LLM-based entity and relationship extraction from PDF/Text.
2. **Indexing**: Dual-indexing into a Graph Database (structural) and a Vector Database (semantic).
3. **Retrieval**: Query expansion -> Graph Traversal -> Vector Context -> Re-ranking.
4. **Generation**: Final context synthesis into a grounded response.

---
*Developed by Dhinesh Gundam*