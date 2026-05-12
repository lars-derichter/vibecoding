---
layout: section
transition: slide-left
---

# Going Pro

Habits that turn vibecoding into real software work.

---

## Git as Your Safety Net

<v-clicks>

- **Start on GitHub.** Create the repo with a generated README, then `git clone` locally. _(`git init` works too, for offline starts.)_
- Every working state deserves a **commit** — your undo button when Claude takes a wrong turn
- Ask Claude to **write the commit message** for you: _"Stage the relevant files and commit with a clear message."_
- **Push regularly.** Cloud > your laptop.

</v-clicks>

<v-click>

> A commit is cheap. A lost afternoon of changes is not.

</v-click>

---

## CLAUDE.md — A Living Document

A markdown file in your project root. Claude reads it automatically and uses it as standing instructions.

<div grid="~ cols-2 gap-4">

<div>

**What belongs in it**

- Tech stack and conventions
- Build / test / dev commands
- Project-specific gotchas
- Folder structure

</div>

<div>

**What doesn't**

- Transient state ("currently working on X")
- Secrets, API keys
- Long prose — keep it scannable

</div>

</div>

<v-click>

Run **`/init`** to bootstrap one. Then **edit it with Claude** as the project changes: _"Update CLAUDE.md to reflect the new build script."_ See [this repo's CLAUDE.md](https://github.com/lars-derichter/vibecoding/blob/main/CLAUDE.md) as an example.

</v-click>

---

## Testing with Claude

Tests give Claude a way to verify its own work — and catch hallucinations.

<v-clicks>

- Ask Claude to **write tests alongside the feature**: _"Add tests for this function covering the happy path and one edge case."_
- **Test-driven prompting:** _"Write a failing test for X, then make it pass."_
- After a fix: _"Add a regression test so this doesn't break again."_

</v-clicks>

<v-click>

> If Claude can't write a test for it, you probably can't trust it either.

</v-click>

---

## Code Quality & Review

Ask Claude to be **harsh on its own work**.

```
Review this diff for bugs, edge cases, and security issues.
Be specific. What would a senior engineer change?
```

```
What else does this change touch? Are there places I should
also update?
```

```
Find any duplicated logic in this file and propose a refactor.
```

<v-click>

Use this **before every commit**, not just at the end of the project.

</v-click>

---

## Skills — Reusable Workflows

A **skill** is a packaged prompt + procedure Claude can invoke by name. Think "saved playbook".

<v-clicks>

- Invoke with `/<skill-name>` in Claude Code
- Built-in examples: `/review`, `/security-review`, `/init`
- You can write your own — a markdown file with frontmatter and instructions

</v-clicks>

<v-click>

**Example:** an [atomic-commits skill](https://github.com/lars-derichter/vibecoding/blob/main/resources/skills/atomic-commits.md) that splits your work-in-progress into small, well-messaged commits.

</v-click>

---

## Permissions & settings.json

Claude Code asks for permission before running commands. **You decide what to trust.**

<v-clicks>

- Permissions live in `~/.claude/settings.json` (user-wide) and `.claude/settings.json` (per-project)
- Allowlist common safe commands (`npm test`, `git status`) — fewer prompts, same safety
- **Never** blanket-allow `Bash(*)` on shared machines

</v-clicks>

<v-click>

See an annotated example: [resources/settings-example.jsonc](https://github.com/lars-derichter/vibecoding/blob/main/resources/settings-example.jsonc).

</v-click>
