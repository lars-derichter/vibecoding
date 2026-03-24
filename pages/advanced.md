---
layout: section
transition: slide-left
---

# Going Further with Claude Code

---

## CLAUDE.md — Project Memory

- A **markdown file** in your project root that Claude reads automatically
- Put coding conventions, tech stack, and project-specific instructions here
- Like a **briefing document** for your AI collaborator
- Run **`/init`** to let Claude generate a CLAUDE.md by analysing your project

```markdown
# CLAUDE.md
## Tech Stack
- React + TypeScript
- Use Tailwind CSS for styling

## Conventions
- Use functional components
- All API calls go through src/api/
```

---

## Compacting and Context Management

Claude has a **context window** — long sessions can lose early context.

<v-clicks>

- Use **`/compact`** to summarize the conversation and free up space
- Use **`/clear`** to start fresh within the same project
- Start **new conversations** for new features

</v-clicks>

<v-click>

> Think of it like clearing your desk before starting a new task.

</v-click>

---

## More to Explore on Your Own

<v-clicks>

- **Custom slash commands** — create reusable prompt templates
- **MCP (Model Context Protocol)** — connect Claude to external tools
- **Git integration** — Claude can create commits and branches
- **Multi-file editing** — refactor across your entire project

</v-clicks>

<v-click>

Docs: **[docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)**

</v-click>
