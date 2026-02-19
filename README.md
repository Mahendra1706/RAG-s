# RAG Implementations

A collection of Retrieval-Augmented Generation (RAG) techniques built with LangChain & LangGraph.

## Structure

```
RAG/
├── corrective_RAG/             # Corrective RAG (CRAG) architecture
│   ├── corrective_rag.ipynb         # CRAG with web search fallback
│   └── corrective_upgrd_RAG.ipynb   # Upgraded CRAG with sentence-level refinement
│
├── self_RAG/                   # Self-reflective RAG architecture
│   ├── self_RAG.ipynb               # LLM critiques its own retrieval & generation
│   └── self_RAG_2.ipynb             # Extended experiments
│
├── graph_RAG/                  # Graph-based RAG architecture
│   └── GraphRAG.ipynb               # Knowledge graph retrieval with Neo4j
│
├── retrieval_techniques/       # Retrieval enhancement techniques
│   ├── crossEncoder.ipynb           # Cross-encoder reranking
│   └── self_query_retrieval.ipynb   # LLM-driven metadata filtering
│
└── papers/                     # Reference papers
    ├── attention_is_all_need.pdf
    └── LoRA.pdf
```

## Setup

**API Keys** (`.env` file):
```
GOOGLE_API_KEY=
TAVILY_API_KEY=
GROQ_API_KEY=
COHERE_API_KEY=
NEO4J_URI=
NEO4J_USERNAME=
NEO4J_PASSWORD=
```

**Install:**
```bash
pip install langchain langchain-google-genai langchain-community langchain-groq \
    langchain-cohere langchain-chroma langgraph chromadb tavily-python \
    python-dotenv langchain-neo4j neo4j faiss-cpu pypdf
```

Open any notebook in Jupyter or VS Code and run the cells.
