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
└── README.md
```

## Code Examples

### RAG Implementation (4_RAG/RAG Code.ipynb)

This Jupyter notebook demonstrates how to build a movie recommendation system using Retrieval-Augmented Generation (RAG). The notebook covers:

1. **Data Loading and Preprocessing** - Working with TMDB movie metadata
2. **Embedding Creation** - Using sentence transformers to create vector embeddings
3. **Vector Database Setup** - Implementation with ChromaDB
4. **Retrieval Methods**:
   - Basic retrieval with query expansion
   - HyDE (Hypothetical Document Embedding) for improved retrieval
   - Query decomposition for complex queries

The example uses Google's Gemini model for generating responses based on retrieved context.

## Getting Started

To run the notebook examples:

1. Clone this repository
2. Install the required dependencies:
   ```
   pip install sentence_transformers chromadb google-genai pandas numpy pydantic
   ```
3. Set up appropriate API keys for the LLM services used in the examples
4. Run the Jupyter notebooks