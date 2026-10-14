# GenAI 101 - How Generative AI is Rewriting the Rules for ML Engineers (And How to Adapt and get Started)

Read the post: [GenAI 101 - How Generative AI is Rewriting the Rules for ML Engineers (And How to Adapt and get Started)](https://www.mlwhiz.com/p/genai-101-how-generative-ai-is-rewriting)

Date: 2025-03-03

Subtitle: Some Thoughts and Approaches to get started in GenAI space

## Summary

Written for ML engineers coming from BERT-and-CNN style work, the post explains the shift from discriminative to generative models and how to move between them. Discriminative models learn P(Y|X) and draw decision boundaries. Generative models learn the data distribution itself and can produce new samples. A sentiment example is shown both ways: a BERT classifier and a LLaMA prompt.

It names three strengths of generative models. Zero and few-shot learning removes the cold start problem, since you describe categories in a prompt instead of labeling data. Cross-domain generalization helps with shifts like moving a US-trained classifier to another English-speaking market (the author recalls a drop of almost 15%). And one model can handle many tasks instead of one model per task.

On speed, the author cites prototyping in days, non-technical people building tools, and API-driven development replacing GPU infrastructure. He compares three weeks building a BERT inference pipeline to a few lines of API calls, and says his team runs 2-3x more A/B tests.

The risks are cost (a generative call can take 3-4x the time and compute of a discriminative one), confident hallucinations, and hard evaluation.

His playbook has six parts: go hybrid (a cheap classifier first, an LLM fallback), use RAG against hallucination, treat prompt engineering as the new feature engineering, distill LLM knowledge into small models (the post says roughly 100x cheaper and 80% as good), fine-tune with LoRA when needed, and control cost and latency with quantization, caching and versioned prompts. It ends with a learning path and a rule: prototype with an LLM, then distill to a simple model where you can.

## Key takeaways

- Generative models fit flexibility and edge cases. Discriminative ones fit speed, cost and deterministic output.
- Zero and few-shot prompting removes the need for labeled data at the start.
- Hybrid systems, RAG and distillation are the main ways to control cost and hallucination.
- Prompts should be versioned like code and A/B tested.
- Prototype with an LLM, then distill when volume makes cost matter.

## Code

The code blocks from the post are in [code-snippets.md](code-snippets.md). They are fragments, not a runnable notebook.
