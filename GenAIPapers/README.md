# GenAI Papers Collection

<div align="center">
  <h3>📚 Influential Generative AI Research Papers</h3>
  
  <p>
    <img src="https://img.shields.io/badge/Papers-36-blue" alt="36 Papers"/>
    <img src="https://img.shields.io/badge/Categories-8-orange" alt="8 Categories"/>
    <img src="https://img.shields.io/badge/Status-Updated-green" alt="Updated Collection"/>
  </p>
</div>

## 📋 Papers in This Collection

| **Paper Title** | **Year** | **Category** | **Key Innovation** | **Impact on the Field** |
|---|---|---|---|---|
| **AlphaCode: Competition-level code generation with AlphaCode** | 2022 | Code Generation | Large-scale Transformer trained on competitive programming datasets with sampling-based generation and filtering mechanisms | Achieved human-level performance on competitive programming contests, demonstrating AI's capability for complex algorithmic problem-solving and inspiring new benchmarks |
| **CLIP: Learning Transferable Visual Representations from Natural Language Supervision** | 2021 | Multimodal AI | Contrastive learning between image and text embeddings using 400M image-text pairs, enabling zero-shot image classification | Revolutionized computer vision by eliminating need for labeled datasets, became foundation for DALL-E, GPT-4V, and countless multimodal applications |
| **Chain-of-Thought Prompting Elicits Reasoning in Large Language Models** | 2022 | Reasoning | Simple prompting technique that encourages step-by-step reasoning by including intermediate steps in few-shot examples | Unlocked emergent reasoning capabilities in LLMs, spawned entire field of prompt engineering and reasoning research, improved performance on complex tasks by 10-50% |
| **Code Llama: Open Foundation Models for Code** | 2023 | Code Generation | Open-source code generation model fine-tuned from Llama 2 with specialized training on code datasets and infilling objectives | Democratized access to high-quality code generation, enabling widespread development of coding assistants and accelerating open-source AI development |
| **Codex: Evaluating Large Language Models Trained on Code** | 2021 | Code Generation | GPT-3 fine-tuned on GitHub repositories, introducing novel evaluation metrics and techniques for code generation tasks | Powers GitHub Copilot, transformed software development workflow for millions of developers, established code generation as major AI application area |
| **DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning** | 2024 | Reasoning | Reinforcement learning framework specifically designed to enhance reasoning capabilities in large language models through reward-based training | Demonstrated significant improvements in mathematical and logical reasoning tasks, influenced development of reasoning-focused training methodologies |
| **Direct Preference Optimization: Your Language Model is Secretly a Reward Model** | 2023 | Alignment | Eliminates separate reward model training by directly optimizing LLM policy using human preferences via classification loss | Simplified RLHF pipeline by 50% computational cost, made alignment training more accessible, adopted by major AI labs for model alignment |
| **DoRA: Weight-Decomposed Low-Rank Adaptation** | 2024 | Fine-tuning | Decomposes pre-trained weights into magnitude and direction components, applying LoRA only to direction for better fine-tuning | Outperformed standard LoRA across multiple tasks, offering more effective parameter-efficient fine-tuning with similar computational overhead |
| **Flamingo: a Visual Language Model for Few-Shot Learning** | 2022 | Multimodal AI | Cross-attention layers between frozen vision encoder and language model, enabling few-shot learning on vision-language tasks | Demonstrated powerful few-shot multimodal capabilities, influenced architectures of GPT-4V and Gemini, established new paradigm for multimodal learning |
| **GLaM: Efficient Scaling of Language Models with Mixture-of-Experts** | 2021 | Architecture | Sparsely activated MoE architecture with learned routing, achieving better performance than dense models with fewer active parameters | Paved way for efficient scaling beyond trillion parameters, influenced PaLM, Switch Transformer, and modern efficient LLM architectures |
| **GPT-4V(ision) System Card** | 2023 | Multimodal AI | Integration of vision capabilities into GPT-4 with comprehensive safety analysis and capability assessment across multimodal tasks | Established new standard for multimodal AI evaluation, demonstrated commercial viability of vision-language models, influenced safety practices industry-wide |
| **Gemini: A Family of Highly Capable Multimodal Models** | 2023 | Multimodal AI | Native multimodal training from scratch with unified architecture processing text, images, audio, and video simultaneously | First model to match GPT-4 performance while being multimodal from ground up, advanced state-of-the-art in multimodal reasoning and understanding |
| **Gemini 1.5: Unlocking Multimodal Understanding** | 2024 | Multimodal AI | Extended context length to 1M+ tokens with enhanced multimodal reasoning capabilities across text, images, audio, and video | Breakthrough in long-context multimodal understanding, enabled new applications in document analysis and multimedia processing |
| **In-Context Retrieval-Augmented Generation with Pre-trained Language Models** | 2023 | RAG | Combines retrieval with in-context learning, using retrieved documents as context for generation without fine-tuning | Enhanced RAG systems with better context utilization, improved factual accuracy in LLM responses, influenced design of modern knowledge-augmented systems |
| **Is DPO Superior to PPO for LLM Alignment? A Comprehensive Study** | 2024 | Alignment | Comprehensive empirical comparison of Direct Preference Optimization vs Proximal Policy Optimization for language model alignment | Provided crucial insights into alignment method effectiveness, influenced industry adoption of DPO over traditional RLHF approaches |
| **LLaMA 2: Open Foundation and Fine-Tuned Chat Models** | 2023 | Foundation Models | Improved open-source foundation models with commercial license, enhanced safety training, and chat-optimized variants | Democratized access to high-quality LLMs, enabled widespread commercial adoption of open-source models, accelerated AI research globally |
| **Learning to Reason via Mixture-of-Thought for Logical Reasoning** | 2024 | Reasoning | Combines multiple reasoning approaches (chain-of-thought, tree-of-thought, etc.) in a unified framework for enhanced logical reasoning | Improved performance on complex reasoning benchmarks by 15-30%, demonstrated benefits of reasoning method ensemble approaches |
| **LoRA: Low-Rank Adaptation of Large Language Models** | 2021 | Fine-tuning | Decomposes weight updates into low-rank matrices, reducing trainable parameters by 99% while maintaining performance | Revolutionized LLM fine-tuning by making it accessible on consumer hardware, enabled rapid model customization, became standard for efficient adaptation |
| **LoRA Learns Less and Forgets Less** | 2024 | Fine-tuning | Empirical analysis showing LoRA's learning dynamics and catastrophic forgetting properties compared to full fine-tuning | Provided theoretical understanding of LoRA's effectiveness, influenced development of improved parameter-efficient fine-tuning methods |
| **Mamba: Linear-Time Sequence Modeling with Selective State Spaces** | 2023 | Architecture | Selective state space model with linear scaling in sequence length, addressing Transformer's quadratic complexity limitation | Potential transformer alternative for long sequences, achieved competitive performance with much better efficiency, sparked renewed interest in non-attention architectures |
| **Mixtral 8x7B: A Mixture of Experts Language Model** | 2024 | Architecture | Open-source sparse MoE with 8 experts, matching dense model performance while using only 12B active parameters | Demonstrated feasibility of open-source MoE models, achieved GPT-3.5 level performance with 5x efficiency, accelerated open-source AI development |
| **Mixture-of-Depths: Dynamically Allocating Compute** | 2024 | Architecture | Dynamic computation allocation across sequence positions, allowing models to skip unnecessary computations for certain tokens | Reduced computational cost by 50% while maintaining performance, introduced new paradigm for efficient inference in large language models |
| **PaLM-2 Technical Report** | 2023 | Foundation Models | Improved data quality, multilingual training, and reasoning capabilities with enhanced mathematical and coding performance | Powers Google's AI products (Bard, etc.), demonstrated importance of high-quality training data, advanced multilingual and reasoning capabilities |
| **Parameter-Efficient Transfer Learning for NLP** | 2019 | Fine-tuning | Adapter modules inserted between transformer layers, enabling task-specific adaptation with minimal parameter overhead | Founded parameter-efficient fine-tuning field, influenced LoRA and subsequent methods, made transfer learning more practical for resource-constrained settings |
| **Phi-4 Technical Report** | 2024 | Foundation Models | 14B parameter model achieving state-of-the-art performance through high-quality training data and curriculum learning | Demonstrated that smaller models can compete with larger ones through superior training, influenced focus on data quality over model size |
| **QLoRA: Efficient Finetuning of Quantized LLMs** | 2023 | Fine-tuning | 4-bit quantization combined with LoRA and paged optimizers, enabling fine-tuning of 65B models on single GPU | Democratized LLM fine-tuning by reducing memory requirements by 4x, enabled widespread experimentation with large models on consumer hardware |
| **RLHF: Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback** | 2022 | Alignment | Three-stage training process: supervised fine-tuning, reward modeling, and PPO reinforcement learning from human preferences | Established foundation for modern AI alignment, powers ChatGPT and similar systems, created new field of human preference learning in AI |
| **ReAct: Synergizing Reasoning and Acting in Language Models** | 2022 | Agents | Interleaves reasoning traces and actions, enabling LLMs to interact with environments while maintaining interpretable thought processes | Created new paradigm for AI agents, improved reasoning accuracy by 20-40%, influenced development of autonomous agents and tool-using AI systems |
| **ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models** | 2023 | Agents | Separates reasoning from tool execution, generating complete reasoning plan before tool calls for more efficient and robust agent behavior | Improved agent reliability and reduced token costs by 50%, influenced modular agent architectures, enhanced planning capabilities in AI systems |
| **Reasoning Language Models: A Blueprint** | 2024 | Reasoning | Comprehensive framework for developing reasoning capabilities in language models through systematic training and evaluation | Provided roadmap for reasoning-focused LLM development, influenced industry approaches to building more capable reasoning systems |
| **Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks** | 2020 | RAG | Combines parametric and non-parametric knowledge by retrieving relevant documents and conditioning generation on retrieved context | Founded RAG paradigm used in ChatGPT, Copilot, and most modern AI systems, solved knowledge cutoff problem, enabled factual accuracy in LLM responses |
| **Switch Transformer: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity** | 2021 | Architecture | Simplified MoE with single expert selection and improved training stability, achieving 7x speedup while maintaining quality | Enabled practical training of trillion-parameter models, influenced Google's PaLM and modern efficient architectures, democratized large-scale model training |
| **Toolformer: Language Models Can Teach Themselves to Use Tools** | 2023 | Tool Use | Self-supervised learning of tool use through filtered sampling, enabling LLMs to decide when and how to use external tools | Established foundation for autonomous tool use in AI, influenced development of modern AI agents, demonstrated self-improvement capabilities in LLMs |
| **Towards Large Reasoning Models: A Survey of Reinforced Reasoning** | 2024 | Reasoning | Comprehensive survey of reinforcement learning approaches for enhancing reasoning capabilities in large language models | Provided systematic overview of reasoning enhancement techniques, influenced research directions in reasoning-focused AI development |
| **Towards System 2 Reasoning in LLMs: Learning How to Think With Meta Chain-of-Thought** | 2024 | Reasoning | Meta-cognitive approach to reasoning that teaches models to think about their own thinking processes, inspired by dual-process theory | Advanced reasoning beyond simple chain-of-thought, demonstrated improvements in complex problem-solving and self-reflection capabilities |
| **Tree of Thoughts: Deliberate Problem Solving with Large Language Models** | 2023 | Reasoning | Tree search over language model reasoning steps, enabling exploration of multiple reasoning paths and backtracking | Improved complex problem-solving by 50-70%, inspired new reasoning frameworks, demonstrated importance of search in AI reasoning systems |

## � Paper Categories

### 🏗️ **Architecture & Foundation Models** (8 papers)
- Mamba: Linear-Time Sequence Modeling
- Mixtral 8x7B: Mixture of Experts Language Model
- Mixture-of-Depths: Dynamically Allocating Compute
- Switch Transformer: Scaling to Trillion Parameter Models
- GLaM: Efficient Scaling of Language Models
- PaLM-2 Technical Report
- LLaMA 2: Open Foundation and Fine-Tuned Chat Models
- Phi-4 Technical Report

### 🎯 **Alignment & Safety** (3 papers)
- RLHF: Training a Helpful and Harmless Assistant
- Direct Preference Optimization: Your Language Model is Secretly a Reward Model
- Is DPO Superior to PPO for LLM Alignment? A Comprehensive Study

### 🔧 **Fine-tuning & Efficiency** (5 papers)
- LoRA: Low-Rank Adaptation of Large Language Models
- QLoRA: Efficient Finetuning of Quantized LLMs
- Parameter-Efficient Transfer Learning for NLP
- DoRA: Weight-Decomposed Low-Rank Adaptation
- LoRA Learns Less and Forgets Less

### 🤖 **Code Generation** (3 papers)
- Codex: Evaluating Large Language Models Trained on Code
- Code Llama: Open Foundation Models for Code
- AlphaCode: Competition-level code generation

### 🧠 **Reasoning & Planning** (8 papers)
- Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
- ReAct: Synergizing Reasoning and Acting in Language Models
- Tree of Thoughts: Deliberate Problem Solving with Large Language Models
- DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning
- Learning to Reason via Mixture-of-Thought for Logical Reasoning
- Reasoning Language Models: A Blueprint
- Towards Large Reasoning Models: A Survey of Reinforced Reasoning
- Towards System 2 Reasoning in LLMs: Learning How to Think With Meta Chain-of-Thought

### 🔍 **Retrieval-Augmented Generation** (2 papers)
- Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
- In-Context Retrieval-Augmented Generation with Pre-trained Language Models

### 🌟 **Multimodal AI** (5 papers)
- CLIP: Learning Transferable Visual Representations
- Flamingo: a Visual Language Model for Few-Shot Learning
- GPT-4V(ision) System Card
- Gemini: A Family of Highly Capable Multimodal Models
- Gemini 1.5: Unlocking Multimodal Understanding

### 🛠️ **Tool Use & Agents** (2 papers)
- Toolformer: Language Models Can Teach Themselves to Use Tools
- ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models

## 🎯 Recommended Reading Paths

1. Start with **CLIP** and **Chain-of-Thought** papers
2. Move to **LoRA** and **Parameter-Efficient Transfer Learning**
3. Explore **Retrieval-Augmented Generation**

## 🔄 Maintenance

This collection is updated regularly to include:
- New breakthrough papers
- Important follow-up work
- Replication studies
- Survey papers for new researchers

---

**Last Updated**: July 2025
**Maintainer**: Research Collection
**Status**: Living Document - Continuously Updated

> **Note**: This collection focuses on the most influential papers that have shaped generative AI. For a complete academic survey, consider complementing with recent survey papers and conference proceedings.

---
