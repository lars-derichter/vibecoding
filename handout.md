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
