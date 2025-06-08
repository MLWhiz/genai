# Advanced PEFT Techniques

<div align="center">
  <h3>🎯 Parameter-Efficient Fine-Tuning for Large Language Models</h3>
  
  <p>
    <img src="https://img.shields.io/badge/PEFT-LoRA-blue" alt="LoRA"/>
    <img src="https://img.shields.io/badge/PEFT-QLoRA-orange" alt="QLoRA"/>
    <img src="https://img.shields.io/badge/PEFT-DoRA-green" alt="DoRA"/>
    <img src="https://img.shields.io/badge/PEFT-AdaLoRA-purple" alt="AdaLoRA"/>
    <img src="https://img.shields.io/badge/PEFT-IA³-red" alt="IA³"/>
  </p>
</div>

This directory contains comprehensive implementations and comparisons of state-of-the-art Parameter-Efficient Fine-Tuning (PEFT) techniques for large language models. The content is part of the GenAI series published on [MLWhiz](https://www.mlwhiz.com/). The particular blog is [here](https://open.substack.com/pub/mlwhiz/p/fine-tuning-llms-your-guide-to-peft?r=9kivc&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true)

## 📚 Overview

Parameter-Efficient Fine-Tuning has revolutionized how we adapt large language models for specific tasks. Instead of fine-tuning all parameters (which requires massive computational resources), PEFT methods enable effective adaptation by training only a small subset of parameters while keeping the pre-trained model frozen.

## 🚀 Techniques Covered

### 1. LoRA (Low-Rank Adaptation)
- **Method**: Decomposes weight updates into low-rank matrices
- **Best for**: General fine-tuning tasks with good performance-efficiency balance

### 2. QLoRA (Quantized LoRA)
- **Method**: Combines 4-bit quantization with LoRA for maximum memory efficiency
- **Best for**: Resource-constrained environments and very large models

### 3. DoRA (Weight-Decomposed Low-Rank Adaptation)
- **Method**: Separates weight updates into directional and magnitude components
- **Best for**: Tasks requiring enhanced performance over traditional LoRA

### 4. AdaLoRA (Adaptive LoRA)
- **Method**: Dynamically adjusts rank during training based on importance
- **Best for**: Complex tasks where different modules need different adaptation levels

### 5. IA³ (Infused Adapter by Inhibiting and Amplifying Inner Activations)
- **Method**: Scales key/value projections and feed-forward activations
- **Best for**: Tasks requiring minimal parameter overhead

## 📁 Contents

```
6_Advanced_PEFT/
├── README.md                           # This file
├── Advanced PEFT Techniques.ipynb      # Complete implementation notebook
└── requirements.txt                    # Python dependencies
```

## 🛠️ Implementation Details

### Base Configuration
- **Model**: Mistral-7B-Instruct-v0.1
- **Dataset**: Stanford Alpaca (instruction-following dataset)
- **Training**: 1 epoch with evaluation every 50 steps
- **Hardware**: GPU with mixed precision (FP16)

### Key Features
- Complete training pipelines for each PEFT method
- Comprehensive parameter efficiency analysis
- Performance comparisons via perplexity metrics
- Memory optimization strategies
- Production-ready model saving and loading
- Gradient checkpointing for memory efficiency

## 🏃‍♂️ Quick Start

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

3. **Run Sections**: Each PEFT technique is implemented in its own section with clear markdown explanations.

## 💡 Key Insights

### When to Use Each Method:

- **LoRA**: Your go-to choice for most fine-tuning tasks with good balance of efficiency and performance
- **QLoRA**: When working with very large models or limited GPU memory
- **DoRA**: When you need better performance than LoRA and can afford slightly more parameters
- **AdaLoRA**: For complex tasks where different parts of the model need different levels of adaptation
- **IA³**: When you need ultra-minimal parameter overhead and the task suits activation scaling

### Best Practices:
- Start with LoRA for baseline performance
- Use QLoRA for memory-constrained scenarios
- Experiment with DoRA for performance improvements
- Consider AdaLoRA for complex, multi-faceted tasks
- Try IA³ for lightweight deployment scenarios

## 🔗 Related Resources

- **Blog Series**: [MLWhiz GenAI Series](https://www.mlwhiz.com/)
- **PEFT Library**: [Hugging Face PEFT](https://github.com/huggingface/peft)
- **Transformers**: [Hugging Face Transformers](https://github.com/huggingface/transformers)

## 📄 Research Papers

- **LoRA**: [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)
- **QLoRA**: [QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314)
- **DoRA**: [DoRA: Weight-Decomposed Low-Rank Adaptation](https://arxiv.org/abs/2402.09353)
- **AdaLoRA**: [Adaptive Budget Allocation for Parameter-Efficient Fine-Tuning](https://arxiv.org/abs/2303.10512)
- **IA³**: [Few-Shot Parameter-Efficient Fine-Tuning is Better and Cheaper than In-Context Learning](https://arxiv.org/abs/2205.05638)

## 🤝 Contributing

Feel free to open issues or submit pull requests to improve the implementations or add new PEFT techniques!

## 📜 License

This project is open source and available under the MIT License.

---

<div align="center">
  <p>
    🚀 <strong>Part of the <a href="https://www.mlwhiz.com/">MLWhiz</a> GenAI Series</strong> 🚀
  </p>
</div> 