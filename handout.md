# Vibecoding with Claude Code — Handout

> **Think first, prompt second, verify always.**

## The Vibecoding Workflow

### 1. Start with a Clear Idea

Before touching Claude, write down:

- **What problem** are you solving?
- **For whom?**
- **What should the end result look like?** (Describe screens, features, data)

Write this in 3–5 sentences — this becomes your first prompt.

### 2. Break It Down

- Do **not** ask for the entire app in one prompt
- Start with the **skeleton / structure**, then add features one by one
- Each prompt should be **one clear task**

### 3. Iterate and Verify

After each Claude response:

1. **Read** what it did (at least skim the changes)
2. **Test** it — does it work?
3. **If something is wrong:** describe the problem specifically

"The button should be blue but it is red" **beats** "fix it".

### 4. Use Claude as a Collaborator

- Ask it to **explain** decisions: *"Why did you choose this approach?"*
- Ask for **alternatives**: *"What are other ways to implement this?"*
- Ask for **improvements**: *"Look at this project and suggest improvements"*

Claude is at its best when you treat it as a **thinking partner**, not just a code generator.

---

## Tips & Tricks

### Choosing the Right Model

| Model | Speed | Best for |
| ---------- | ------- | ---------------------------------------- |
| **Sonnet** | Fast | Straightforward tasks, quick edits |
| **Opus** | Slower | Complex reasoning, architecture decisions |
| **Haiku** | Fastest | Tiny tasks — formatting, renaming |

**Rule of thumb:** Start with Sonnet. Escalate to Opus when stuck or planning something complex.

### Plan Mode

Toggle with **Shift+Tab** in Claude Code.

- Claude **thinks and plans** but does not write code yet
- Use it at the **start of a new feature** or when unsure about the approach
- Example: *"Plan how you would add user authentication to this app"*

> Plan first, code second. This is the single most underused feature.

### Make Claude Ask Questions First

Before starting a new feature, try:

- `Before you start, ask me any clarifying questions you need.`
- `What information do you need from me to do this well?`

This prevents Claude from making wrong assumptions.

### Ask for Improvements

When you have something working:

- `Look at this project and suggest some improvements.`
- `Review this code for potential bugs or issues.`
- `How could I make this more user-friendly?`

### Debugging with Claude

1. **Copy-paste the exact error message**
2. **Describe what you expected** vs. what happened
3. Use a prompt like: `I see this error: [paste error]. It happens when I [describe action]. Fix it.`

### Creating Documentation

- `Create a README.md for this project explaining what it does and how to run it.`
- `Add comments to explain the key parts of this code.`

### More Useful Prompts

- *"Explain this code to me like I am a beginner"*
- *"Refactor this to be simpler"*
- *"Add error handling for edge cases"*
- *"Create a CLAUDE.md file with project conventions"* — helps Claude help you
- Use `/clear` to reset context when switching tasks

---

## Going Further

### Git as your safety net

- Start on GitHub: create the repo with a generated README, then `git clone` locally. `git init` works offline.
- Commit every working step — your undo button.
- Ask Claude to write the commit message: `Stage the relevant files and commit with a clear message explaining why.`
- Push regularly. Cloud > laptop.

### CLAUDE.md — keep it alive

- Run `/init` to bootstrap.
- Edit it with Claude as the project changes: `Update CLAUDE.md to reflect the new build script.`
- Belongs in CLAUDE.md: tech stack, conventions, commands, gotchas.
- Doesn't belong: transient state, secrets, long prose.

### Testing prompts

- `Add tests for this function covering the happy path and one edge case.`
- `Write a failing test for X, then make it pass.`
- `Add a regression test so this bug can't come back.`

### Code review before commit

- `Review this diff for bugs, edge cases, and security issues. What would a senior engineer change?`
- `What else in this codebase does this change affect? Are there places I should also update?`
- `Find any duplicated logic in this file and propose a refactor.`

### Skills

- Invoke with `/<skill-name>` in Claude Code.
- Built-in: `/review`, `/security-review`, `/init`.
- Example custom skill (atomic commits): [resources/skills/atomic-commits.md](resources/skills/atomic-commits.md).

### Permissions & settings.json

- `~/.claude/settings.json` (user-wide), `.claude/settings.json` (project), `.claude/settings.local.json` (personal per-project).
- Annotated example: [resources/settings-example.jsonc](resources/settings-example.jsonc).
- Never blanket-allow `Bash(*)`.

### Memory: three layers

- **Session** — current conversation. `/compact` to summarise, `/clear` to reset, `claude --resume` to bring one back.
- **Project** — `CLAUDE.md` in the repo root. Shared with the team via git.
- **User** — `~/.claude/CLAUDE.md` + memory tool. Your personal preferences, everywhere.

### MCP, subagents, hooks, cost, diff review

- **MCP servers** — connect Claude to external tools (GitHub, Linear, databases). [docs](https://code.claude.com/docs/en/mcp)
- **Subagents** — delegate research/exploration. Built-ins: Explore, Plan, general-purpose. [docs](https://code.claude.com/docs/en/sub-agents)
- **Hooks** — shell commands triggered by harness events; great for auto-format or blocking risky writes. [docs](https://code.claude.com/docs/en/hooks)
- **Cost & limits** — `/cost` shows session usage. Use Haiku for mechanical work to save your budget. [pricing](https://www.claude.com/pricing)
- **Reading diffs critically** — before every commit ask: `Explain this diff line by line.` then `What else does this change touch?`
