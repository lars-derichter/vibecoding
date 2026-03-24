---
layout: section
transition: slide-left
---

# Tips & Tricks

A cheat-sheet for your group exercise.

---

## Choosing the Right Model

| Model | Speed | Best for |
|-------|-------|----------|
| **Sonnet** | Fast | Straightforward tasks, quick edits |
| **Opus** | Slower | Complex reasoning, architecture decisions |
| **Haiku** | Fastest | Tiny tasks — formatting, renaming |

<v-click>

**Rule of thumb:** Start with Sonnet. Escalate to Opus when stuck or when planning something complex.

</v-click>

---

## Plan Mode

Toggle with <kbd>Shift</kbd>+<kbd>Tab</kbd> in Claude Code.

<v-clicks>

- Claude **thinks and plans** but does not write code yet
- Use it at the **start of a new feature** or when you are unsure about the approach
- Great for: _"Plan how you would add user authentication to this app"_

</v-clicks>

<v-click>

> Plan first, code second. This is the single most underused feature.

</v-click>

---

## Make Claude Ask Questions First

Use these prompts before starting a new feature:

```
Before you start, ask me any clarifying questions you need.
```

```
What information do you need from me to do this well?
```

<v-click>

**Why?** Prevents Claude from making wrong assumptions — especially useful at the start of a project.

</v-click>

---

## Ask for Improvements

When you have something working, ask Claude to review it:

```
Look at this project and suggest some improvements.
Improvements can be code optimizations, usability fixes,
or extra functionalities.
```

```
Review this code for potential bugs or issues.
```

```
How could I make this more user-friendly?
```

<v-click>

This is a great way to **learn** — Claude explains _why_ something could be better.

</v-click>

---

## Debugging with Claude

When something goes wrong:

<v-clicks>

1. **Copy-paste the exact error message**
2. **Describe what you expected** vs. what happened
3. Use a prompt like:

</v-clicks>

<v-click>

```
I see this error: [paste error].
It happens when I [describe action].
Fix it.
```

</v-click>

<v-click>

Let Claude read the relevant files — it often spots the issue faster than you.

</v-click>

---

## Creating Documentation

```
Create a README.md for this project explaining what it does
and how to run it.
```

```
Add comments to explain the key parts of this code.
```

<v-click>

Useful for group projects, hand-offs, and your own future self.

</v-click>

---

## More Useful Prompts

<v-clicks>

- _"Explain this code to me like I am a beginner"_
- _"Refactor this to be simpler"_
- _"Add error handling for edge cases"_
- _"Create a CLAUDE.md file with project conventions"_ — helps Claude help you
- Use `/clear` to reset context when switching tasks

</v-clicks>
