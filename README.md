# 🚀 Advanced RAG Implementations

A collection of state-of-the-art Retrieval-Augmented Generation (RAG) techniques implemented using [LangChain](https://langchain.com/) and [LangGraph](https://langchain-ai.github.io/langgraph/). 

This repository explores different architectures to improve the accuracy, robustness, and reliability of RAG systems.

## 📂 Project Structure

| Directory | Notebook | Description |
|-----------|----------|-------------|
| `correctiveRAG/` | **[corrective_rag.ipynb](correctiveRAG/corrective_rag.ipynb)** | **Corrective RAG (CRAG)**: Improves robustness by "correcting" retrieval failures. If retrieved documents are irrelevant, it falls back to a web search. Implemented with **LangGraph**. |
| `adv_RAG/` | **[self_RAG.ipynb](adv_RAG/self_RAG.ipynb)** | **Self-RAG**: A framework where the LLM critiques its own retrieval and generation to ensure high quality and relevance. |
| `adv_RAG/` | **[crossEncoder.ipynb](adv_RAG/crossEncoder.ipynb)** | **Cross-Encoder Reranking**: Utilizes Cross-Encoders to re-rank retrieved documents, significantly improving the precision of the context provided to the LLM. |

## 🛠️ Tech Stack

- **Frameworks**: [LangChain](https://www.langchain.com/), [LangGraph](https://langchain-ai.github.io/langgraph/)
- **LLMs**: Google Gemini (`gemini-1.5-flash`), Groq (Llama 3, etc.)
- **Vector Store**: [ChromaDB](https://www.trychroma.com/)
- **Search**: [Tavily AI](https://tavily.com/)
- **Embeddings**: Google Generative AI Embeddings

## 🔑 Prerequisites

Ensure you have the following API keys set in your environment (or `.env` file):

```bash
GOOGLE_API_KEY=your_google_api_key
TAVILY_API_KEY=your_tavily_api_key
GROQ_API_KEY=your_groq_api_key
```

## 📦 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Mahendra1706/RAG-s.git
   cd RAG-s
   ```

2. **Install dependencies**:
   ```bash
   pip install langchain langchain-google-genai langchain-community langchain-core langgraph chromadb tavily-python python-dotenv ipykernel
   ```

## 🏃‍♂️ Usage

1. Open the desired notebook using Jupyter Lab or VS Code.
2. Ensure your `.env` file is set up with the necessary API keys.
3. Run the cells to see the RAG pipelines in action!

---
