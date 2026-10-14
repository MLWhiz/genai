# Did Apple Just Burst the AI Reasoning Bubble? I don't think so

Read the post: [Did Apple Just Burst the AI Reasoning Bubble? I don't think so](https://www.mlwhiz.com/p/the-hard-truth-about-ai-reasoning)

Date: 2025-06-10

Subtitle: A shallow dive into Apple's latest research that challenges everything we think we know about reasoning models

## Summary

The post covers Apple's paper "The Illusion of Thinking" and the author's reaction as someone bullish on reasoning models. Instead of another math benchmark, Apple built controllable puzzle environments such as Tower of Hanoi. Puzzles let you control complexity (add more disks), avoid data contamination, expose the reasoning trace and give an objective check on correctness.

The paper found three regimes. At low complexity, regular LLMs beat reasoning models, which overthink and loop. At medium complexity, reasoning models do well. At high complexity, both types collapse.

The odd finding: as problems get harder, reasoning models think less, not more. They reduce reasoning effort even with token budget left.

The author stays bullish. The tested models (o1, o3-mini, DeepSeek-R1, Claude 3.7 Sonnet) are first-generation, the medium-complexity sweet spot is real, and the paper shows what to fix: overthinking on easy tasks and effort that doesn't scale with difficulty.

For practitioners, the post suggests knowing your complexity zone (skip the reasoning toggle on simple tasks), not expecting more tokens alone to solve hard problems, testing beyond final accuracy, and building controlled benchmarks. It ends with a speculative take that human reasoning has complexity limits too, and a list of what the next generation might add: thinking effort that scales with difficulty, better calibration, new architectures and hybrid approaches.

## Key takeaways

- Reasoning models help most at medium complexity and can hurt on simple tasks.
- At high complexity both reasoning and regular models collapse.
- Reasoning effort drops as problems get harder, which is the surprising result.
- Evaluate intermediate reasoning steps and use controlled benchmarks, not only final accuracy.
- The author reads the paper as a roadmap for the next generation, not as proof the approach fails.

## Code

This post is conceptual, no code.
