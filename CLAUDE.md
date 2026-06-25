# Task Board Project

## Project Overview

A task board application for managing tasks visually (Kanban-style or similar).

## Tech Stack

- (Update this section as the stack is decided)

## Project Structure

- (Update this section as directories are created)

## Development Guidelines

- Write clean, minimal code without unnecessary comments or abstractions.
- Do not add error handling or validation beyond what is explicitly required.
- Prefer editing existing files over creating new ones.
- Do not create documentation files unless explicitly requested.

## Git Operation Rules

**Every time code is changed, commit and push to GitHub immediately.**

### Workflow

1. Make the code change.
2. Stage only the relevant files (never `git add -A` blindly — exclude `.env`, secrets, and large binaries).
3. Write a concise commit message focused on *why*, not *what*.
4. Push to the remote branch.

```bash
git add <specific-files>
git commit -m "short description of why this change was made"
git push
```

### Commit Message Style

- Use the imperative mood: "Add login page", "Fix task drag bug", "Remove unused dependency"
- Keep the subject line under 72 characters.
- No period at the end of the subject line.

### Branch Strategy

- `main` — always deployable; never force-push.
- Feature work goes on a topic branch; open a PR to merge into `main`.

### What NOT to commit

- `.env` files or any file containing secrets or credentials.
- Large binary files or build artifacts (`node_modules/`, `dist/`, `.next/`, etc.).
- Editor-specific files unless already in `.gitignore`.
