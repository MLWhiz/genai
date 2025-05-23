# GenAI Repository

This repository contains code examples and resources related to a series of blog posts about Generative AI (GenAI) published on [MLWhiz](https://www.mlwhiz.com/). The content focuses on various aspects of GenAI, from architectural concepts to practical implementations.

## Blog Posts in the Series

This repository accompanies the following blog posts:

1. [GenAI Series: A Review of the Architectural Journey](https://www.mlwhiz.com/p/genai-series-a-review-of-the-architectural) - An overview of the evolution and architecture of generative AI systems.

2. [GenAI Series: The Art and Science of Prompt Engineering](https://www.mlwhiz.com/p/genai-series-the-art-and-science) - Techniques and strategies for effective prompt engineering.

3. [GenAI Series: My Tryst with AI-Assisted Development](https://www.mlwhiz.com/p/genai-series-my-tryst-with-ai-assisted) - Experiences and insights on using AI for code development.

4. [GenAI Series: Building RAG Applications](https://www.mlwhiz.com/p/genai-series-building-rag-applications) - Guide to building Retrieval-Augmented Generation applications.

## Repository Structure

```
genai/
├── 1_GenAiArchitecturalJourney/
│   └── README.md
├── 2_PromptEngineering/
│   └── README.md
├── 3_VibeCoding/
│   └── README.md
├── 4_RAG/
│   ├── README.md
│   └── RAG Code.ipynb
├── 5_Advanced_RAG/
│   └── RAG_with_LLAMAIndex.ipynb
└── README.md
```

## Code Examples

### Basic RAG Implementation (4_RAG/RAG Code.ipynb)

This Jupyter notebook demonstrates how to build a movie recommendation system using Retrieval-Augmented Generation (RAG). The notebook covers:

1. **Data Loading and Preprocessing** - Working with TMDB movie metadata from Kaggle
2. **Embedding Creation** - Using SentenceTransformers (`all-mpnet-base-v2`) to create vector embeddings
3. **Vector Database Setup** - Implementation with ChromaDB for efficient similarity search
4. **Advanced Retrieval Methods**:
   - **Basic Retrieval** with query expansion for improved recall
   - **HyDE (Hypothetical Document Embedding)** - Generates hypothetical documents that match the query for better retrieval
   - **Query Decomposition** - Breaks complex queries into simpler sub-queries for comprehensive results
5. **Response Generation** - Uses Google's Gemini model with structured output (Pydantic models)

**Key Features:**
- Movie recommendation based on themes, genres, and plot elements
- Multiple retrieval strategies for different query types
- Structured JSON responses for easy integration

### Advanced RAG Implementation (5_Advanced_RAG/RAG_with_LLAMAIndex.ipynb)

This notebook showcases a production-ready RAG system using LlamaIndex with advanced features:

1. **Enhanced Data Pipeline**:
   - MovieLens 25M dataset integration
   - TMDB API for rich movie metadata (cast, crew, reviews, keywords)
   - Sophisticated document chunking and node creation

2. **Hybrid Retrieval System**:
   - **Vector Search** using BGE embeddings (`BAAI/bge-large-en-v1.5`)
   - **BM25 Keyword Search** for exact term matching
   - **Query Fusion** with reciprocal reranking for optimal results

3. **Advanced Query Processing**:
   - **HyDE Query Transformation** for semantic similarity
   - **Cross-encoder Re-ranking** (`BAAI/bge-reranker-v2-m3`)
   - **Metadata Filtering** by year, director, genre, etc.

4. **Multi-Agent Architecture**:
   - **Similarity Search Tool** - Netflix-style "more like this" recommendations
   - **Advanced Filter Tool** - Amazon Prime-style filtering by multiple criteria
   - **Review Analysis Tool** - Rotten Tomatoes-style critical reception analysis
   - **Mood-based Recommender** - Spotify-style contextual recommendations
   - **ReAct Agent** for complex multi-step reasoning

## Getting Started

To run the notebook examples:

1. Clone this repository
2. Set up appropriate API keys for the LLM services used in the examples
3. Run the Jupyter notebooks