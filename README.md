# Multi-Track Development Planning

A reusable skill that produces **agent-proof project architecture** for long-horizon, multi-track (frontend/backend/integration) development. It produces a documentation system + execution protocol that lets any zero-context LLM Agent pick up a long-running project and continue development correctly, even when multiple parallel agents work simultaneously across multiple tracks.

## What It Does

Drop this skill into any brainstorming or planning session. It produces:

- **7 live documents** (PLAN / PROGRESS / DECISIONS / AGENT_PROTOCOL / RECOVERY / BLOCKERS / MERGE_QUEUE)
- **A task graph** for the current phase with full specs (ID, deps, acceptance, steps, resume_hint)
- **Milestone-level outlines** for future phases
- **A trigger-word protocol** for auto-continuing any track (e.g. `前端 开始开发`)
- **A recovery protocol** for any amnesiac agent
- **An 8-mechanism parallel-execution safety system**
- **A task lifecycle state machine** (pending → in_progress → done/blocked/failed/stale) with retry + stale detection
- **A constitution change protocol** preventing silent edits to STRATEGY/SPEC/ARCHITECTURE
- **A zero-memory agent relay simulation test** as the ultimate acceptance check

## When to Use

Invoke this skill whenever the user asks to plan, design, or set up architecture for a project that matches any of:

- A long-running project (>1 session / days / weeks)
- A project that LLM AI Agents will execute
- A project with two or more parallel tracks (frontend + backend, etc.)
- A project where context compression or session switching is expected
- A project where the user wants parallel multi-agent / multi-session execution

## Install

Copy the `SKILL.md` file into your project's skill folder (e.g. `.trae/skills/multi-track-development-planning/SKILL.md` or the equivalent location for your agent runtime).

## Usage

After install, any agent in the project can invoke the skill by name. During brainstorming, the skill replaces the standard design step with a strategic architecture pack + execution protocol + task graph.

Trigger phrases (user → agent):
- `<track-name> 开始开发` — start next ready task on that track
- `集成 开始开发` — start next integration task
- `继续` — resume last session's work
- `<track> 状态` — report track status without doing work

## Documentation

The complete methodology is documented inside [SKILL.md](./SKILL.md). Read sections 0–10 for the full spec.

## Quality

The skill ships with 13 invariant checks + a zero-memory agent relay simulation test. See §8 in SKILL.md.

## Author

**NoWint** — [https://github.com/NoWint](https://github.com/NoWint)

## License

AGPL-3.0 — see [LICENSE](./LICENSE).
