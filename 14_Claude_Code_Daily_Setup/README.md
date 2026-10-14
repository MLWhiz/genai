# I Use Claude Code Every Day. Here's the Setup That Actually Matters

Read the post: [I Use Claude Code Every Day. Here's the Setup That Actually Matters](https://www.mlwhiz.com/p/i-use-claude-code-every-day-heres)

Date: 2026-04-23

Subtitle: CLAUDE.md, Skills 2.0, permission modes, channels — an opinionated guide for beginners and the mildly curious

## Summary

An opinionated setup guide for Claude Code, built around "the 20% of the surface area that delivers 80% of the value." The author admits his early mistakes: clicking yes to permission prompts, running up a $200 API bill before learning the Max plan can be used to log in, and starting forty-odd sessions because he didn't know `claude -c`.

The post frames Claude Code as an agentic CLI (read, think, act, observe, repeat), not an autocomplete extension. It cites roughly 4% of public GitHub commits (about 135,000 a day) as of February 2026, and Anthropic's statement that 90% of its internal code is AI-written.

The setup, in order:

- Install with npm (Node 18+) and log in with a claude.ai account. The author says Max ($100/month for individuals) is cheaper than the API if you code a few hours a day.
- Write a CLAUDE.md of under about 200 lines: commands, conventions, gotchas, off-limits paths. An example for a churn-model project is included.
- Add a settings.json with allow, ask and deny rules, especially deny rules for .env files and secrets.
- Use plan mode for thinking and `--dangerously-skip-permissions` for doing, once deny rules are in place.
- Use `claude -c` to continue, `claude -r` to resume, and `-n` or `/rename` to name sessions.
- Write skills (SKILL.md with frontmatter such as disable-model-invocation, allowed-tools and context: fork). Skills and custom commands have merged.
- Use subagents to keep the main context clean, and MCP servers (he uses Playwright and GitHub) for integrations.
- Try /voice and Channels (Claude on Telegram, in research preview).

The post ends with a tier list: daily essentials, things worth adding later, and things to skip for now.

## Key takeaways

- CLAUDE.md is the one file to write first. If you repeat something across sessions, it belongs there.
- Deny rules in settings.json are the safety fence, so set them before loosening permissions.
- Plan mode first, then let Claude run. Reviewing a plan is faster than reviewing finished code.
- Name your sessions and resume them with `claude -r name`.
- Turn repeated prompts into skills, and add MCP servers only when you need a specific integration.

## Code

The code blocks from the post are in [code-snippets.md](code-snippets.md). They are fragments, not a runnable notebook.
