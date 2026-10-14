# 5 Things Meta Muse Actually Does, and the Engineering Behind Each One

Read the post: [5 Things Meta Muse Actually Does, and the Engineering Behind Each One](https://www.mlwhiz.com/p/6-things-meta-muse-actually-does)

Date: 2026-10-03

Subtitle: A personal AI agent that runs in its own VM, keeps working after you close the app, and asks permission before it spends. A look at the machinery.

## Summary

The author tried Muse, Meta's personal AI agent, by asking it to find what he owed people in his Gmail. It returned a list and then asked whether it should draft the replies. That shift from advising to acting is why he wrote about the engineering underneath.

Per the post, Muse launched on 8 September 2026, runs on Muse Spark 1.3 (1 million token context, released 2 September), and connects to Gmail, Google Calendar, Outlook, Plaid, OpenTable, Spotify and others. The author used it from the UK through a VPN for setup and mostly talks to it in WhatsApp.

Five pieces of machinery do the work:

- The Muse Secure VM: a dedicated, isolated cloud VM per user. Credentials live there, not in the model's context.
- Sentinel: a separate gatekeeper agent that controls outbound requests and escalates sensitive actions for approval. The planner doesn't authorize its own actions, which matters if it gets prompt-injected.
- Background execution: tasks keep running after you close the app.
- Persistent memory: preferences are picked up from conversation and can be forgotten on request.
- Muse Spark 1.3: Meta claims about 20% fewer tool calls and 25% fewer tokens on agentic tasks (the author says he can't verify this).

The use cases are email triage, calendar plus morning briefings plus price tracking, booking and buying (with one-time cards from Link by Stripe), open-web form filling, and LinkedIn triage. The author treats connector-backed tasks as dependable and browser-driven ones as best effort. Pricing is Free (100M tokens a week), Power ($20/month, 500M) and Maximum ($100/month, 3B).

## Key takeaways

- The notable change is that the agent acts on your accounts instead of only advising.
- Separating the planner from the authorizer (Sentinel) is the main safety design.
- One-time card numbers and per-user VMs assume that something will eventually go wrong.
- Connector-backed tasks are reliable. Browser-driven ones break quietly when pages change.
- Approval fatigue is a human limit that no architecture fixes.
- All three tiers run the same agent, so you are paying for compute.

## Code

This post is conceptual, no code.
