---
layout: section
transition: slide-left
---

# The Vibecoding Workflow

---

## The Golden Rule

<div class="text-3xl text-center py-8">

**Think first, prompt second, verify always.**

</div>

Vibecoding is not "type random stuff and hope" — it is a **structured collaboration**.

---

## Step 1: Start with a Clear Idea

Before touching Claude, write down:

<v-clicks>

- **What problem** are you solving?
- **For whom?**
- **What should the end result look like?** (Describe screens, features, data)

</v-clicks>

<v-click>

Write this in **3-5 sentences** — this becomes your first prompt.

</v-click>

<!--
Analogy: you would not walk into a meeting and say "make me a thing".
The clearer your brief, the better the result.
-->

---

## Step 2: Plan Before You Code

Toggle **plan mode** with <kbd>Shift</kbd>+<kbd>Tab</kbd>. Claude thinks and writes a plan — but does not touch files yet.

<v-clicks>

- Use it whenever the change touches **more than one file** or the approach is unclear
- **Read the plan critically.** Push back: _"Why this approach? What are the alternatives?"_
- Only approve the plan when you understand it

</v-clicks>

<v-click>

> You would not ask a contractor to "build me a house" without a plan. Same here.

</v-click>

<!--
Plan mode is the single most underused feature. For technical students: emphasize that approving a bad plan
costs you 10x more than rejecting it. Reading the plan is the actual work.
-->

---

## Step 3: Break It Down

<v-clicks>

- Do **not** ask for the entire app in one prompt
- Start with the **skeleton / structure**, then add features one by one
- Each prompt should be **one clear task**

</v-clicks>

---

## Step 4: Iterate and Verify

After each Claude response:

<v-clicks>

1. **Read** what it did (at least skim the changes)
2. **Test** it — does it work?
3. **If something is wrong:** describe the problem specifically

</v-clicks>

<v-click>

"The button should be blue but it is red" **beats** "fix it"

</v-click>

---

## Step 5: Use Claude as a Collaborator

<v-clicks>

- Ask it to **explain** decisions: _"Why did you choose this approach?"_
- Ask for **alternatives**: _"What are other ways to implement this?"_
- Ask for **improvements**: _"Look at this project and suggest improvements"_

</v-clicks>

<v-click>

Claude is at its best when you treat it as a **thinking partner**, not just a code generator.

</v-click>
