# New Project Handoff Prompt

We are starting a concrete downstream project from `ai-engineering-contour-template`.

Read `AGENTS.md` first. `AGENTS.md` is the single source of truth for workflow and AI agent behavior. Other files may provide prompts or templates, but they must not redefine or override `AGENTS.md`.

Core workflow:

Idea -> Reuse Gate -> Build-vs-Reuse Decision -> brief.md -> plan before code -> one small approved implementation step -> local checks -> fresh AI review -> PR -> CI -> human merge.

Concrete project/task description:

TODO: Insert the project context, goal, constraints, and first task here.

Before coding, help determine the missing information:

- Goal and non-goals.
- Reuse candidates and build-vs-reuse decision.
- Stack-specific commands.
- Brief contents.
- Files allowed and forbidden to change.
- Tests and checks.
- Whether UI / UX, LLM infrastructure, logging / observability, security / privacy, or post-launch validation are relevant.

Do not write code yet.

Do not add dependencies, config, schema, API, environment variables, auth, routing, architecture, deployment, MCP, subagents, evals, mutation testing, or skills unless justified and approved.

Anti-overengineering rules:

- Do not overengineer.
- Avoid accidental complexity, hidden coupling, ad-hoc workarounds, speculative abstractions, duplicated sources of truth, and spaghetti architecture.
- If scope expands, stop and reassess.
- If checks are not configured or not run, say so.
- Do not weaken tests just to make code pass.

Expected return:

1. Missing information / questions.
2. Reuse Gate plan.
3. Suggested brief.md outline.
4. Required project-specific setup before implementation.
5. Minimal safe next step.

Stop before implementation.
