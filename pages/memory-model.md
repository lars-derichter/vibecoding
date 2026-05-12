---
layout: section
transition: slide-left
---

# Memory: Three Layers

---

## Where Claude Remembers Things

<div grid="~ cols-3 gap-6">

<div>

### Session

The current conversation.

- Lives until `/clear` or you close the session
- `/compact` summarises it to free space
- `claude --resume` brings one back

</div>

<div>

### Project

`CLAUDE.md` in the repo root.

- Read automatically every session
- Shared with your team via git
- Edit it as the project evolves

</div>

<div>

### User

`~/.claude/CLAUDE.md` + memory tool.

- Your personal preferences, across all projects
- Examples: "always use Flemish Dutch", "I prefer terse responses"
- Loaded everywhere

</div>

</div>

<v-click>

> Session is volatile, project is shared, user is personal. Put each fact where it belongs.

</v-click>
