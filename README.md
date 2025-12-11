# Medical AI Assistant
A comprehensive medical information system that combines vector database retrieval with real-time web search to provide accurate, evidence-based medical responses. The system uses an LLM pipeline architecture with quality evaluation and multi-source information synthesis.
# Features
* Hybrid Information Retrieval: Combines local medical knowledge base with real-time web search
* LLM Pipeline Architecture: Vector DB → Web Search → Response Generation → Quality Evaluation
* Quality Assurance: Built-in critic agent evaluates response quality and suggests improvements
* Medical Document Processing: Processes PDF medical literature with intelligent chunking
* Real-time Web Search: Fetches current medical information from trusted sources
* Interactive Web Interface: Modern, responsive chat interface with source citations
* Session Management: Maintains conversation history and chat sessions
# Architecture
<img width="972" height="505" alt="architecture-d" src="https://github.com/user-attachments/assets/e9b0539d-d3da-42dc-b23a-81785ca797f5" />
# Components
1. Document Processing (utils/read_preprocess.py)

PDF text extraction and cleaning
Medical document preprocessing
2.Text Chunking (utils/chunk_data.py)

Intelligent document segmentation
Overlap management for context preservation
3.Vector Database (utils/qdrant_db.py)

Qdrant integration for semantic search
Embedding storage and retrieval
4.Embeddings (utils/embeddings.py)

Cohere API integration for text embeddings
Rate limiting and error handling
5.LLM Agent (utils/retrieval_qa.py)

Groq API integration for response generation
Context synthesis from multiple sources
6.Web Scraper (utils/tavily.py)

Real-time medical information retrieval
Trusted medical source filtering
7.Critic Agent (utils/critic_agent.py)

Response quality evaluation
Improvement suggestions
