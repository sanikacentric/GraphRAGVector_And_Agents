# GraphRAG Vector Store & Agents

A Jupyter notebook implementation combining Graph-based Retrieval-Augmented Generation (GraphRAG) with vector store retrieval and AI agents for advanced knowledge graph querying and multi-hop reasoning.

## Description

Traditional RAG systems retrieve isolated document chunks, losing the relational context between entities. GraphRAG addresses this by building a knowledge graph from documents, enabling agents to traverse entity relationships and perform multi-hop reasoning. This repository demonstrates how to combine GraphRAG with vector store retrieval and agentic workflows for more contextually rich answers.

## Features

- **Knowledge Graph Construction** — Extract entities and relationships from documents to build a structured knowledge graph
- - **Graph-based Retrieval** — Traverse entity relationships for multi-hop question answering beyond what vector search alone can provide
  - - **Vector Store Integration** — Combine graph retrieval with semantic vector search for hybrid retrieval
    - - **AI Agent Orchestration** — Use agents to decide when to use graph traversal vs. vector search based on query type
      - - **Community Summarization** — Generate summaries of entity communities within the graph for high-level insight
        - - **LLM-Powered Entity Extraction** — Use LLMs to extract entities and relationships from unstructured text
          - - **Global and Local Search** — Support both global (community-level) and local (entity-level) search modes
           
            - ## Architecture
           
            - ```
              Documents
                  ↓
              [LLM Entity & Relationship Extraction]
                  ↓
              [Knowledge Graph] ←→ [Vector Store]
                  ↓                      ↓
              [Graph Traversal]  [Semantic Search]
                  ↓                      ↓
                       [AI Agent]
                         ↓
                  Contextual Answer
              ```

              ## Tech Stack

              | Component | Technology |
              |---|---|
              | Language | Python 3 |
              | Graph Framework | GraphRAG / NetworkX |
              | Vector Store | FAISS / Chroma |
              | LLM | OpenAI GPT-4 / Azure OpenAI |
              | Embeddings | OpenAI Embeddings |
              | Framework | LangChain |
              | Notebook | Jupyter (Google Colab) |

              ## Setup Instructions

              ### Prerequisites

              - Python 3.9+
              - - OpenAI API key (or Azure OpenAI)
               
                - ### Installation
               
                - ```bash
                  git clone https://github.com/sanikacentric/GraphRAGVector_And_Agents.git
                  cd GraphRAGVector_And_Agents
                  pip install graphrag langchain openai faiss-cpu networkx jupyter
                  ```

                  ### Configuration

                  ```bash
                  export OPENAI_API_KEY=your-openai-api-key
                  ```

                  ### Running the Notebook

                  ```bash
                  jupyter notebook GraphRAGVectorStore_Agents.ipynb
                  ```

                  ## Use Cases

                  GraphRAG excels at queries that require understanding relationships between entities, such as "What companies did the CEO previously work at?" or "Which drugs interact with compound X?" — questions that require traversing connected facts rather than finding a single relevant passage.

                  ## License

                  Open source — for educational and AI research purposes.
