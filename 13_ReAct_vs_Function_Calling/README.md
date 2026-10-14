# What Production Deployments Taught Me About ReAct vs Function Calling

Read the post: [What Production Deployments Taught Me About ReAct vs Function Calling](https://www.mlwhiz.com/p/what-production-deployments-taught)

Date: 2025-09-21

Subtitle: From Prototype to Production: Hard-Won Lessons for AI Agent Development

## Summary

The post starts from the gap between an agent that works in a demo and one that works for real users. Base LLMs can't check live data, query your database, run code or search the web, so agents add tools.

ReAct is a loop of Thought, Action and Observation. The post walks through a Paris weather query: the agent checks the current temperature (18°C), searches for the seasonal average (about 9°C) and answers. ReAct is transparent, adapts when a tool fails, and works with models that lack function calling. Function calling has the model return structured JSON naming the function and its arguments. It is faster, uses fewer tokens and is less error-prone to parse.

Rule of thumb: ReAct for multi-step reasoning, choosing tools on the fly and debugging transparency (a research assistant that parses papers). Function calling for predictable workflows (a support bot with get_order_status, initiate_refund and update_shipping_address).

The post shows both patterns from scratch, then with LlamaIndex (ReActAgent and FunctionAgent, with a Gemini LLM integration in the install step).

The production lessons are the core:

1. Customize the default ReAct prompt, which has {tool_desc} and {tool_names} placeholders.
2. Use type annotations (Annotated) on tool parameters to improve tool selection.
3. Pre-call tools needed on almost every request instead of letting the agent call them, which saves an LLM round trip.
4. Cut generated tokens, since generation drives latency more than reasoning does.
5. Log every action and observation with trace ID, timestamps, token counts and cost.
6. Add fallbacks: max steps (10-15), timeouts, retries with backoff, error feedback as an observation, and a safe final answer.

## Key takeaways

- ReAct fits complex, adaptive tasks. Function calling fits simple, predictable ones.
- Hybrid approaches often work best, and the post advises starting simple.
- Tool descriptions and type annotations strongly affect agent behavior.
- Token generation, not reasoning depth, is the main latency cost.
- Structured logs of every thought, action and observation are required for debugging production agents.
- Plan for loops and failures with step limits, timeouts and a safe default reply.

## Code

The code blocks from the post are in [code-snippets.md](code-snippets.md). They are fragments, not a runnable notebook.
