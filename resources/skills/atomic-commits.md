---
name: atomic-commits
description: Split current uncommitted work into a sequence of small, focused commits with clear messages. Use when staged or unstaged changes mix multiple concerns, or when finishing a vibecoding session that produced a pile of mixed edits.
---

# Atomic commits

Goal: turn a heap of changes into a clean commit history. One commit per logical change. Messages that explain **why**, not just **what**.

## When to use this skill

- After a vibecoding session that touched multiple files for multiple reasons
- Before opening a pull request
- When `git status` shows changes that obviously belong in different commits

Do **not** use this skill if there is genuinely only one change — just commit it directly.

## Procedure

1. **Survey the changes.** Run `git status` and `git diff` (and `git diff --staged` if anything is already staged). Note every distinct concern: a bug fix, a refactor, a new feature, a doc update, a config tweak.

2. **Group changes into atomic commits.** A commit is atomic when:
   - It does **one thing** that can be described in a single sentence without "and"
   - It compiles / passes tests on its own (reverting it leaves the tree working)
   - Its diff is small enough to review in 60 seconds

3. **Plan the sequence.** Order matters:
   - Refactors and renames first (they prepare the ground)
   - New behaviour next
   - Tests with the behaviour they cover (or just before, for test-driven order)
   - Docs and formatting last

   Write out the plan as a numbered list before staging anything. Read it back.

4. **Stage and commit one group at a time.** Use `git add -p` for hunk-level staging when a single file holds multiple concerns. After each commit, run `git status` to confirm the working tree shrank as expected.

5. **Write each message in this shape:**

   ```
   <subject: imperative, ≤72 chars, no trailing period>

   <body: why this change, not what. Reference the constraint, bug,
   or decision that motivated it. Wrap at ~72 chars. Optional.>
   ```

   Subject examples that pass:
   - `Extract pricing logic into a pure function`
   - `Fix off-by-one in date-range filter`
   - `Block writes to .env in settings.json`

   Subjects that fail (too vague, too what-y):
   - `Update files`
   - `Fixes`
   - `Refactor stuff`

6. **Sanity check.** Run `git log --oneline -n <N>` (where N is the number of new commits). Read the subjects in order. If a stranger could not tell what each commit does from the subject alone, rewrite.

## Guardrails

- **Never** force-push, reset, or rebase commits already on a shared branch unless the user explicitly asks
- **Never** add `--no-verify` to bypass pre-commit hooks
- If a hook fails, **fix the issue** and create a new commit; do not amend or skip
- Skip files that look like secrets (`.env`, `*credentials*`, key files) — warn the user instead
- Stage files by name, not `git add .` or `git add -A`

## Output

When done, report:
- The number of commits created
- Their subject lines in order
- Any files deliberately left unstaged and why
