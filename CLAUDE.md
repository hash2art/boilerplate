# CLAUDE.md — APP_NAME

## Project Overview

---

## Session Continuity

This project uses `docs/PROGRESS.md` as the session handoff file. Claude's context resets each session — PROGRESS.md is the single source of truth for build state.

- **Start every session:** run `/catchup` — Claude reads PROGRESS.md and confirms where to continue
- **End every session:** run `/checkpoint` — Claude updates PROGRESS.md with completed items, in-progress state, and the next session's start instruction
- Never leave a session with failing tests or uncommitted code
- One session = one completable PROGRESS.md item; split larger tasks across sessions

PROGRESS.md sections: Current Status (phase + next session start line), Completed ✅, In Progress 🔄, Up Next 📋, Key Decisions Made, Known Issues/Blockers.

Slash commands live in `.claude/commands/`. The `checkpoint.md` command instructs Claude to update all PROGRESS.md sections and confirm with "Checkpoint saved. Next session: [task]". The `catchup.md` command instructs Claude to read both CLAUDE.md and PROGRESS.md, summarise the current state, and ask whether to continue with the next listed task.

---

## Git Conventions
- Always use Conventional Commits format (e.g., feat:, fix:, docs:, refactor:, style:, test:).
- Automatically stage and commit changes after completing a task.
- Keep the subject line under 72 characters.
- Use lowercase for the scope and subject.

---

## Tech Stack

---

## Repository Structure


---

## Environment Variables
