# Project templates (case-journal & troubleshooting-log)

Templates and Cursor rules so the LLM always has project context and can keep documentation updated.

## Files

| File | Use when |
|------|----------|
| **case-journal.md** | Project involves setting up new things, upgrades, or changing something in a working environment. |
| **troubleshooting-log.md** | When you're debugging – add info continuously (errors, hypotheses, experiments) so everything is in one place. |
| **.cursor/rules/context-and-journal.mdc** | Cursor rule: read these files at the start and suggest/apply updates as work progresses. |

## New project

1. **Fork this repo** (or copy the folder) into your new project.
2. **Pick the right file** for the project type:
   - Setup/upgrade/change → copy `case-journal.md` to the project root or `docs/`.
   - Troubleshooting → copy `troubleshooting-log.md` to the project root or `docs/`.
3. **Cursor rule:** Copy `.cursor/rules/context-and-journal.mdc` into the project's `.cursor/rules/`, **or** add the rule to your global Cursor config (`~/.cursor/rules/`) so it applies in any project that has these files.

## Workflow

- The LLM reads case-journal or troubleshooting-log at the start of the conversation for context.
- After completing work, the LLM suggests or applies updates to the right file (status, next steps, experiments/completed items).
- Keep the files short and free of secrets.

---

## Move to your own GitHub repo

Use this when you want a dedicated template repo (e.g. `project-templates` or `case-templates`) that you fork for each new project.

1. **Create a new repo** on GitHub (e.g. `project-templates`). Leave it empty (no README/license if you want a clean copy).

2. **Copy the template folder** into that repo:
   - Clone your new repo locally.
   - Copy everything from `project-templates/` (this folder) into the repo root, so the structure is:
   ```
   your-repo/
   ├── README.md
   ├── case-journal.md
   ├── troubleshooting-log.md
   └── .cursor/
       └── rules/
           └── context-and-journal.mdc
   ```
   - Commit and push.

3. **When starting a new project:** Fork the template repo (or use "Use this template" on GitHub), then clone the fork as your new project. Add the template file you need (case-journal or troubleshooting-log) to the project root or `docs/`, and ensure the Cursor rule is in the project’s `.cursor/rules/` or in your global rules.

4. **Recommended – global rule:** Copy `context-and-journal.mdc` to `~/.cursor/rules/`. Then in **any** project (including new folders where no templates exist yet), the LLM will: (1) check for `case-journal.md` or `troubleshooting-log.md`; (2) if neither exists, ask if you want to fork the project-templates repo before continuing; (3) if at least one exists, read it for context and suggest updates as work progresses.
