---
name: github-project-publisher
description: Package a local project into a clean GitHub-ready repository with README, supporting docs, organized deliverables, git initialization, remote setup guidance, and push troubleshooting. Use when a user wants to turn a local project, OpenClaw workflow, skill collection, contest entry, or chat-grown output into a public GitHub repository from zero to first push.
---

# GitHub Project Publisher

Use this skill when a user has something real on disk but not yet something presentable on GitHub.

The purpose is not just to run `git push`.
The purpose is to convert a messy local output into a **publishable repository asset**.

## Core goal

Help the assistant take a project from:
- scattered files
- half-written docs
- no repo structure
- no README
- no publish flow

to:
- a clean repository folder
- a clear README
- support docs for submission or sharing
- initialized git history
- remote linkage
- successful first push

## Workflow

### 1. Define the publishing unit
First decide what the repository actually is.

Identify:
- the project name
- the project scope
- which files belong in the repo
- which files do **not** belong in the repo
- whether the project is product-like, skill-like, research-like, or contest-like

Do not publish from a noisy parent workspace if a smaller focused repo should exist.

### 2. Create a clean repo structure
Prefer a focused project directory.

Typical structure:
- `README.md`
- `docs/`
- `skills/` or `src/` or `assets/` depending on project type
- packaged outputs if they are useful to end users

Do not dump unrelated workspace state into the repo.

### 3. Write the minimum publishable docs
At minimum, create:
- `README.md`

Common helpful additions:
- `docs/project-description.md`
- `docs/repo-description.md`
- `docs/submission-copy.md`
- `docs/usage-example.md`
- a simple cover image or SVG

### 4. Explain the project clearly
The README should answer:
- what this project is
- why it exists
- what problem it solves
- what the main modules are
- how someone can use it

Avoid vague “AI project” wording. Use a concrete framing.

### 5. Initialize git cleanly
Typical sequence:
- `git init`
- `git add .`
- `git commit -m "Initial commit: ..."`
- `git branch -M main`
- `git remote add origin <repo-url>`
- `git push -u origin main`

### 6. Handle GitHub auth friction
Expect common issues:
- user tries GitHub account password instead of PAT
- wrong token type or wrong repo scope
- 403 permission errors
- HTTP2 transport errors
- no GitHub CLI login state

Guide the user through the smallest viable fix.

### 7. Finish the repository as a shareable artifact
Before calling it done, confirm:
- files are actually on GitHub
- README renders clearly
- docs are present
- the repo looks intentional, not accidental

## Common failure modes

### Failure mode 1 — Publishing the wrong directory
The user tries to publish a giant mixed workspace instead of a focused project folder.

Fix:
Create a dedicated repo folder and copy only the intended files.

### Failure mode 2 — Missing narrative
The files exist, but the repository does not explain itself.

Fix:
Write README + short docs before pushing.

### Failure mode 3 — GitHub auth confusion
The user enters a GitHub password instead of a PAT.

Fix:
Explain that modern Git operations over HTTPS use PAT, not account password.

### Failure mode 4 — Wrong token scope
The token exists, but lacks repository write permission.

Fix:
Use a token with repository contents write access.

### Failure mode 5 — The repo is technically uploaded but still looks weak
The code is online, but the repo does not look like a project.

Fix:
Add README, docs, examples, and cover assets.

## Output expectations

A good result should leave the user with:
- a real repo URL
- a readable README
- a coherent project structure
- docs they can paste into forms or competitions
- confidence that the project now exists outside the chat thread

## References

Read as needed:
- `references/repo-checklist.md` — final publish checklist
- `references/auth-troubleshooting.md` — GitHub token and push error troubleshooting
- `references/repo-structure-patterns.md` — common repo organization patterns
