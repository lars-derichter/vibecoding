---
layout: section
transition: slide-left
---

# Installation

Follow along on your laptop — I will keep talking while you install.

---
layout: two-cols-header
layoutClass: gap-8
---

## Step 1: Install VS Code

Download from **[code.visualstudio.com](https://code.visualstudio.com/)**

::left::

### Windows

- Run the installer
- Default settings are fine
- Check "Add to PATH" if prompted

::right::

### Mac

- Open the `.dmg` file
- Drag VS Code to Applications
- Open it from Applications

<!--
Ask: "Raise your hand if you already have VS Code installed." — those people can skip ahead.
-->

---
layout: two-cols-header
layoutClass: gap-8
---

## Step 2: Install Node.js

Download from **[nodejs.org](https://nodejs.org/)** (LTS version)

::left::

### Windows

- Run the installer
- **Check "Add to PATH"**
- Restart your terminal after install

::right::

### Mac

- Run the `.pkg` installer
- Follow the prompts

<v-click>

> You will not need to write any JavaScript — Node.js is useful for the web projects you'll build today.

</v-click>

---
layout: two-cols-header
layoutClass: gap-8
---

## Step 3: Install Claude Code CLI

Open the built-in terminal in VS Code.

::left::

### Mac

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

::right::

### Windows (PowerShell)

```powershell
irm https://claude.ai/install.ps1 | iex
```

::content::

<v-click>

Then start Claude Code: `claude` — this opens your browser to authenticate.

Install URL: **[claude.ai/install.sh](https://claude.ai/install.sh)**

</v-click>

<v-click>

> You need an **Anthropic account** with a Pro plan ($20/month) to use Claude Code. New users can start a **30-day free trial** at [claude.ai](https://claude.ai).

</v-click>

<!--
Walk around and help students who get stuck.
The native installer auto-updates in the background.
Students need a paid plan — help them sign up for the free trial if needed.
-->

---

## Step 4: Install the VS Code Extension

1. Open the Extensions panel: `[Ctrl]+[Shift]+[X]` (Windows) / `[Cmd]+[Shift]+[X]` (Mac)
2. Search for **"Claude Code"** by Anthropic
3. Click **Install**

<v-click>

You should now see the Claude Code panel in your sidebar.

**Raise your hand when you see it!**

</v-click>

<!--
Wait until ~80% of students have the extension installed before moving on.
Help stragglers during the next section.
-->
