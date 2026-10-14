# Code blocks from: I Use Claude Code Every Day. Here's the Setup That Actually Matters

Code blocks copied from the post, in order. They are fragments, not a runnable notebook.

Source: https://www.mlwhiz.com/p/i-use-claude-code-every-day-heres

## 1. 2. Install and Get Logged In

```bash
npm install -g @anthropic-ai/claude-code
```

## 2. 3. CLAUDE.md — The One File You Have to Write

```
# Project: Customer Churn Model

## What this is
An XGBoost-based churn prediction pipeline. Trained on
~2M rows from Redshift.

## Commands you should know
- `make test` - runs pytest
- `make lint` - ruff + mypy
- `make train` - full training, takes ~20 min, do NOT
  do this unless asked
- `dvc pull` - pulls data artifacts

## Conventions
- All new features go in `src/features/`, one file per
  feature group
- Use `loguru`, not `logging`
- Pandas is fine but prefer Polars for anything over 
  100k rows
- NEVER commit `data/raw/` - gitignored for a reason

## Gotchas
- The `user_id` column in `events.parquet` is a string,
  not an int. Don't cast it.
- Redshift queries time out after 5 minutes. Always add
  LIMIT when exploring.

## Things you should not touch
- `src/legacy/` - pinned code for a deprecated model.
  Don't refactor.
- `migrations/` - manual DB migrations only.
```

## 3. 4. settings.json — The Deny Rules Nobody Talks About

```
~/.claude/settings.json              # User scope - applies everywhere
.claude/settings.json                # Project scope - committed
.claude/settings.local.json          # Local scope - gitignored
```

## 4. 4. settings.json — The Deny Rules Nobody Talks About

```
{
  "$schema": "https://json.schemastore.org/claude-code-settings.json",
  "permissions": {
    "defaultMode": "acceptEdits",
    "allow": [
      "Bash(git diff *)",
      "Bash(git log *)",
      "Bash(git status)",
      "Bash(npm run lint)",
      "Bash(npm run test *)"
    ],
    "ask": [
      "Bash(git push *)",
      "Bash(rm *)"
    ],
    "deny": [
      "Read(./.env)",
      "Read(./.env.*)",
      "Read(./secrets/**)",
      "Bash(curl * | *sh*)",
      "Bash(rm -rf /*)"
    ]
  }
}
```

## 5. 6. Sessions — Naming Is the Real Unlock

```bash
claude -c                       # continue most recent session here
claude -r                       # interactive picker of recent sessions
claude -r "auth-refactor"       # jump straight to the named one
claude -n "auth-refactor"       # start a NEW session with this name
```

## 6. 7. Skills — Your Custom Toolbox

```
---
name: commit
description: Write a conventional commit message from staged changes
---

Write a conventional commit message based on what's
currently staged.

1. Run `git diff --staged` to see what changed
2. Figure out the type (feat/fix/refactor/docs/test/chore)
3. Write a one-line summary under 72 characters
4. If there's meaningful detail, add a body separated
   by a blank line
5. Show me the message and ask before committing
```

## 7. 7. Skills — Your Custom Toolbox

```
---
name: fix-issue
description: Fix a GitHub issue end-to-end
disable-model-invocation: true
allowed-tools: Bash(gh *), Read, Edit, Write
---

Fix GitHub issue $ARGUMENTS by following these steps.

## Current issue
!`gh issue view $ARGUMENTS`

## Recent changes
!`git log --oneline -10`

## Your task
1. Read the issue and understand the problem
2. Search the codebase for relevant files
3. Write the fix
4. Add or update tests
5. Run the tests
6. Write a commit message
7. Push a branch and open a PR linking the issue
```

## 8. 8. Subagents — Preserve Your Context

```
---
name: pr-reviewer
description: Reviews PRs for code quality and security
tools: Read, Grep, Glob, Bash(gh *)
model: claude-opus-4-7
---

You are a senior engineer reviewing a pull request.
Be concrete. Flag:
- Security issues (SQL injection, XSS, auth bugs)
- Performance problems (N+1 queries, unbounded loops)
- Missing tests
- Unclear naming

Don't bikeshed. Focus on things that actually matter.
```

## 9. 9. MCP — The Integration Layer

```bash
claude mcp add github npx -- @modelcontextprotocol/server-github
```
