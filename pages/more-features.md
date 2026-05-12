---
layout: section
transition: slide-left
---

# More to Explore

Quick tour — one slide each, with pointers.

---

## MCP Servers

**Model Context Protocol** lets Claude talk to external tools and services through a standard interface.

<v-clicks>

- Examples: GitHub MCP (issues, PRs), Linear MCP (tickets), database MCPs, Slack MCP
- Configure once, use everywhere — Claude picks them up automatically
- The "USB-C of AI integrations"

</v-clicks>

<v-click>

Docs: [code.claude.com/docs/en/mcp](https://code.claude.com/docs/en/mcp)

</v-click>

---

## Subagents

Delegate a sub-task to a specialised agent without polluting your main conversation.

<v-clicks>

- Built-in examples: **Explore** (search and read), **Plan** (design implementation), **general-purpose** (anything)
- Useful for "go find me all the places that use X" — the result comes back as a summary
- You can define your own subagents in `.claude/agents/`

</v-clicks>

<v-click>

Docs: [code.claude.com/docs/en/sub-agents](https://code.claude.com/docs/en/sub-agents)

</v-click>

---

## Hooks

Run a shell command automatically when Claude is about to do something.

<v-clicks>

- `PreToolUse`, `PostToolUse`, `UserPromptSubmit`, `Stop` — many trigger points
- Use cases: auto-format on file write, block writes to sensitive paths, log everything, run tests after edits
- Configured in `.claude/settings.json`

</v-clicks>

<v-click>

Docs: [code.claude.com/docs/en/hooks](https://code.claude.com/docs/en/hooks)

</v-click>

---

## Cost & Usage Limits

<v-clicks>

- Type **`/cost`** to see what the current session has consumed
- Claude Code plans have **rate limits** — heavy Opus use burns through faster than Sonnet
- Cheap habits: use Haiku for boring mechanical work, `/clear` between unrelated tasks, `/compact` when conversations get long

</v-clicks>

<v-click>

Pricing: [claude.com/pricing](https://www.claude.com/pricing)

</v-click>

---

## Reviewing Diffs Critically

Trust, but verify. Try these prompts on Claude's output **before** you commit:

<v-clicks>

```
Explain this diff line by line. What is each change for?
```

```
What else in this codebase does this change affect?
Are there places I should also update?
```

```
What could break because of this? Suggest one regression test.
```

</v-clicks>

<v-click>

> The diff is the work. Reading it is the job.

</v-click>
