# 🚀 Advanced RAG Implementations

A collection of state-of-the-art Retrieval-Augmented Generation (RAG) techniques implemented using [LangChain](https://langchain.com/) and [LangGraph](https://langchain-ai.github.io/langgraph/). 

This repository explores different architectures to improve the accuracy, robustness, and reliability of RAG systems.

## 📂 Project Structure

| Directory | Notebook | Description |
|-----------|----------|-------------|
| `adv_RAG/` | **[corrective_rag.ipynb](adv_RAG/corrective_rag.ipynb)** | **Corrective RAG (CRAG)**: Improves robustness by "correcting" retrieval failures. If retrieved documents are irrelevant, it falls back to a web search. Implemented with **LangGraph**. |
| `adv_RAG/` | **[self_RAG.ipynb](adv_RAG/self_RAG.ipynb)** | **Self-RAG**: A framework where the LLM critiques its own retrieval and generation to ensure high quality and relevance. |
| `adv_RAG/` | **[crossEncoder.ipynb](adv_RAG/crossEncoder.ipynb)** | **Cross-Encoder Reranking**: Utilizes Cross-Encoders to re-rank retrieved documents, significantly improving the precision of the context provided to the LLM. |
| `adv_RAG/` | **[self_query_retrieval.ipynb](adv_RAG/self_query_retrieval.ipynb)** | **Self-Querying Retrieval**: Uses an LLM to parse natural language queries into structured metadata filters for more precise vector search. |
| `adv_RAG/` | **[GraphRAG.ipynb](adv_RAG/GraphRAG.ipynb)** | **GraphRAG**: Enhances retrieval by modeling information as a knowledge graph, enabling relationship-aware querying and reasoning. Uses **Neo4j** and **LangChain**. |

## 🛠️ Tech Stack

- **Frameworks**: [LangChain](https://www.langchain.com/), [LangGraph](https://langchain-ai.github.io/langgraph/)
- **LLMs**: Google Gemini (`gemini-1.5-flash`), Groq (Llama 3, etc.)
- **Vector Store**: [ChromaDB](https://www.trychroma.com/), [Neo4j](https://neo4j.com/)
- **Graph Database**: [Neo4j](https://neo4j.com/)
- **Search**: [Tavily AI](https://tavily.com/)
- **Embeddings**: Google Generative AI Embeddings, Cohere Embeddings

## 🔑 Prerequisites

Ensure you have the following API keys set in your environment (or `.env` file):

```bash
GOOGLE_API_KEY=your_google_api_key
TAVILY_API_KEY=your_tavily_api_key
GROQ_API_KEY=your_groq_api_key
COHERE_API_KEY=your_cohere_api_key
NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password
```

## 📦 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Mahendra1706/RAG-s.git
   cd RAG-s
   ```

2. **Install dependencies**:
   ```bash
   pip install langchain langchain-google-genai langchain-community langchain-core langchain-groq langchain-cohere langchain-chroma langgraph chromadb tavily-python python-dotenv ipykernel langchain-neo4j neo4j yfiles-jupyter-graphs langchain-experimental
   ```

## 🏃‍♂️ Usage

1. Open the desired notebook using Jupyter Lab or VS Code.
2. Ensure your `.env` file is set up with the necessary API keys.
3. Run the cells to see the RAG pipelines in action!

---
