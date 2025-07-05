<div align="center">
  <h3>🚀 Welcome to the GenAI Repository</h3>
  
  <p>
    <img src="https://img.shields.io/badge/GenAI-Research-blue" alt="GenAI Research"/>
    <img src="https://img.shields.io/badge/ML-Whiz-orange" alt="ML Whiz"/>
    <img src="https://img.shields.io/badge/Open-Source-green" alt="Open Source"/>
  </p>
</div>

This repository serves as a comprehensive collection of code examples, research papers, and practical resources from my Generative AI (GenAI) series published on [MLWhiz](https://www.mlwhiz.com/). 

This content spans the full spectrum of GenAI development:
- 📚 Architectural foundations and research papers
- 🛠️ Practical implementation guides
- 💡 Best practices and optimization techniques
- 🔬 Advanced RAG implementations
- 🤖 AI-assisted development workflows
- 🎯 Advanced PEFT techniques for model fine-tuning

## Blog Posts in the Series
| # | Title | Description |
|---|-------|-------------|
| 1 | [GenAI Series: A Review of the Architectural Journey](https://www.mlwhiz.com/p/genai-series-a-review-of-the-architectural) | An overview of the evolution and architecture of generative AI systems |
| 2 | [GenAI Series: The Art and Science of Prompt Engineering](https://www.mlwhiz.com/p/genai-series-the-art-and-science) | Techniques and strategies for effective prompt engineering |
| 3 | [GenAI Series: My Tryst with AI-Assisted Development](https://www.mlwhiz.com/p/genai-series-my-tryst-with-ai-assisted) | Experiences and insights on using AI for code development |
| 4 | [GenAI Series: Building RAG Applications](https://www.mlwhiz.com/p/genai-series-building-rag-applications) | Guide to building Retrieval-Augmented Generation applications |
| 5 | [Advanced RAG Techniques for ML Engineers: Beyond Vector Search](https://open.substack.com/pub/mlwhiz/p/genai-series-beyond-basic-rag-building) | Guide to building Advanced Retrieval-Augmented Generation applications with Agents |
| 6 | [Advanced PEFT Techniques for Model Fine-tuning](https://open.substack.com/pub/mlwhiz/p/fine-tuning-llms-your-guide-to-peft?r=9kivc&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true) | Comprehensive guide to Parameter-Efficient Fine-Tuning methods including LoRA, QLoRA, DoRA, AdaLoRA, and IA³ |
| 7 | [Traditional RAG is Dead, Long Live GraphRAG](https://www.mlwhiz.com/p/traditional-rag-is-dead-long-live) | Evolution beyond traditional RAG systems using knowledge graphs and interconnected intelligence |

## Repository Structure

```
genai/
├── 1_GenAiArchitecturalJourney/
│   ├── README.md
│   └── [12 Research Papers] - Key papers in GenAI evolution
├── 2_PromptEngineering/
│   └── README.md
├── 3_VibeCoding/
│   └── README.md
├── 4_RAG/
│   ├── README.md
│   └── RAG Code.ipynb
├── 5_Advanced_RAG/
│   ├── README.md
│   ├── RAG_with_LLAMAIndex.ipynb
│   └── processed_books.pkl
├── 6_Advanced_PEFT/
│   ├── README.md
│   ├── Advanced PEFT Techniques.ipynb
│   └── requirements.txt
├── 7_GraphRAG/
│   └── README.md
└── README.md
```

## Contents Overview

### 1. GenAI Architectural Journey
Contains a comprehensive collection of 12 foundational research papers that trace the evolution of generative AI:

1. **Attention is All You Need** - The transformer architecture that started it all
2. **Improving Language Understanding by Generative Pre-Training** - GPT-1 introduction
3. **Pre-training of Deep Bidirectional Transformers for Language Understanding** - BERT paper
4. **Language Models are Unsupervised Multitask Learners** - GPT-2 paper
5. **Language Models are Few-Shot Learners** - GPT-3 paper
6. **Training Compute-Optimal Large Language Models** - Chinchilla scaling laws
7. **Scaling Laws for Neural Language Models** - Understanding model scaling
8. **PaLM: Scaling Language Modeling with Pathways** - Google's approach to scaling
9. **Training language models to follow instructions with human feedback** - InstructGPT
10. **Constitutional AI: Harmlessness from AI Feedback** - Anthropic's safety approach
11. **LLaMA: Open and Efficient Foundation Language Models** - Meta's open source models
12. **GPT-4 Technical Report** - Latest developments in the GPT series

### 2. Prompt Engineering
Delve into the art and science of crafting effective prompts for generative models. This section provides insights and techniques to optimize prompt design, ensuring high-quality and relevant outputs from AI models.

### 3. Vibe Coding
Explore the innovative realm of Vibe Coding, where coding meets creativity. This section showcases projects and ideas that blend artistic expression with programming, pushing the boundaries of traditional software development.

### 4. RAG (Retrieval-Augmented Generation)
Learn the fundamentals of Retrieval-Augmented Generation, a technique that enhances generative models with retrieval mechanisms. This section covers the basics and provides a hands-on implementation guide.

### 5. Advanced RAG Techniques
Dive deeper into advanced RAG methodologies, exploring sophisticated techniques and their practical applications. This section is tailored for ML engineers seeking to enhance their skills and knowledge in RAG.

### 6. Advanced PEFT (Parameter-Efficient Fine-Tuning)
Understand the cutting-edge PEFT methods that enable efficient fine-tuning of large language models. This section offers a comprehensive guide to various PEFT techniques, their implementations, and best practices.

### 7. GraphRAG Implementation (7_GraphRAG/)
This section explores the evolution beyond traditional RAG systems using knowledge graphs and interconnected intelligence:

**Key Concepts:**
- **Knowledge Graph Construction**: Transform documents into interconnected entities and relationships
- **Community Detection**: Use algorithms like Leiden to identify knowledge clusters
- **Multi-hop Reasoning**: Traverse relationships to discover hidden connections
- **Local vs Global Querying**: Intelligent strategies for different query types

**The GraphRAG Advantage:**
- Moves beyond treating documents as isolated fragments
- Builds explicit knowledge graphs where nodes represent entities and edges capture relationships
- Enables complex, multi-faceted queries that require understanding of interconnected concepts
- Particularly powerful for domains with rich entity relationships

**When to Use GraphRAG:**
- Complex multi-hop reasoning required
- Rich entity relationships in your domain
- Users ask nuanced, interconnected questions
- Discovering hidden connections is crucial

**Current Tooling:**
- **Microsoft GraphRAG**: Most comprehensive open-source implementation
- **LlamaIndex**: Practical implementations with flexibility
- **AWS Bedrock Knowledge Bases**: First fully-managed GraphRAG service
- **Neo4j/NebulaGraph**: Robust graph database foundations

**Blog Post:** [Traditional RAG is Dead, Long Live GraphRAG](https://www.mlwhiz.com/p/traditional-rag-is-dead-long-live)

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
   - Amazon Books dataset integration
   - Sophisticated document chunking and node creation
   - Includes `processed_books.pkl` with pre-processed data

2. **Hybrid Retrieval System**:
   - **Vector Search** using BGE embeddings (`BAAI/bge-large-en-v1.5`)
   - **BM25 Keyword Search** for exact term matching
   - **Query Fusion** with reciprocal reranking for optimal results

3. **Advanced Query Processing**:
   - **HyDE Query Transformation** for semantic similarity
   - **Cross-encoder Re-ranking** (`BAAI/bge-reranker-v2-m3`)
   - **Metadata Filtering** by author, rating, etc.

4. **Multi-Agent Architecture**:
   - **Similarity Search Tool** - "more like this" recommendations
   - **Advanced Filter Tool** - Filtering by multiple criteria
   - **Mood-based Recommender** - Contextual recommendations
   - **ReAct Agent** for complex multi-step reasoning

### Advanced PEFT Implementation (6_Advanced_PEFT/Advanced PEFT Techniques.ipynb)

This comprehensive notebook demonstrates cutting-edge Parameter-Efficient Fine-Tuning (PEFT) techniques for optimizing large language models:

1. **LoRA (Low-Rank Adaptation)**:
   - Traditional LoRA implementation with rank decomposition
   - Efficient fine-tuning with minimal parameter overhead (~0.09% trainable parameters)
   - Model merging and deployment strategies

2. **QLoRA (Quantized LoRA)**:
   - 4-bit quantization with NF4 data type
   - Combines quantization with LoRA for maximum efficiency
   - Uses BitsAndBytesConfig for optimal memory usage

3. **DoRA (Weight-Decomposed Low-Rank Adaptation)**:
   - Advanced technique that separates directional and magnitude components
   - Enhanced performance over traditional LoRA
   - Can be combined with quantization for memory efficiency

4. **AdaLoRA (Adaptive LoRA)**:
   - Dynamic rank adaptation during training
   - Automatically adjusts importance of different modules
   - Orthogonal regularization for better parameter efficiency

5. **IA³ (Infused Adapter by Inhibiting and Amplifying Inner Activations)**:
   - Ultra-efficient method with only 0.0072% trainable parameters
   - Scales key/value projections and feed-forward networks
   - Minimal computational overhead

**Key Features:**
- Complete training pipelines for each PEFT method
- Performance comparisons and parameter efficiency analysis
- Production-ready implementations with proper evaluation
- Memory optimization strategies and best practices
- Model saving, loading, and deployment configurations

**Technical Highlights:**
- Uses Mistral-7B as the base model for demonstrations
- Stanford Alpaca dataset for instruction fine-tuning
- Comprehensive evaluation with perplexity metrics
- Support for both FP16 and quantized training
- Gradient checkpointing and memory optimization

## License
This project is open source and available under the [MIT License](LICENSE).