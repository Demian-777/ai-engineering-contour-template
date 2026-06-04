# AI Engineering Contour

## Project overview

This repository is a lightweight, stack-neutral template for AI-assisted engineering work. It is not an application, framework, runtime, or platform.

Use it to start projects with a simple contour:

Idea -> Reuse Gate -> Build-vs-Reuse Decision -> brief.md -> plan before code -> small implementation -> local checks -> fresh AI review -> PR -> CI -> human merge.

## Source of truth

`AGENTS.md` is the single source of truth for repository workflow and AI agent behavior.

Other files may provide prompts, templates, or shims, but they must not redefine these rules.

## Standard workflow

1. Capture the change in a brief.
2. Check for reuse before building.
3. Decide build vs reuse before implementation.
4. Plan before writing code.
5. Implement one small approved step.
6. Run configured local checks.
7. Request a fresh AI review when useful.
8. Open a PR with scope, risk, and validation notes.
9. Let CI run real configured checks.
10. Merge only after human review.

## Commands with TODO placeholders

Downstream projects must replace these placeholders with real commands:

```sh
# TODO: run formatting check
# TODO: run lint/static analysis
# TODO: run tests
# TODO: run build/type checks, if applicable
# TODO: run security checks, if applicable
```

Do not treat placeholder commands as validation.

## Engineering rules

- Keep changes small, explicit, and reversible.
- Prefer clear existing patterns over new abstractions.
- Avoid accidental complexity, hidden coupling, ad-hoc workarounds, speculative abstractions, duplicated sources of truth, and spaghetti architecture.
- Do not introduce an application stack in this template.
- Document meaningful tradeoffs in the brief or PR.

## Dependency policy

- Reuse existing code, platform features, and proven dependencies before building.
- Add new dependencies only when approved in the brief or PR.
- Avoid dependencies for convenience alone.
- This template must not include package manager files.

## Skills policy

- Do not add a skills catalog to this template.
- Use project-specific skills only when a downstream project explicitly adopts them.
- Any skill usage must respect the brief, allowed files, and source-of-truth rules.

## UI / UX policy

- UI / UX requirements apply only when the downstream project has a user interface.
- Keep user workflows clear, accessible, and consistent with the project context.
- Do not add UI frameworks or design systems in this template.

## LLM product policy

- LLM features must define user value, failure modes, privacy implications, and validation approach.
- Do not add LLM infrastructure, providers, agents, evals, MCP, or subagents in this template.
- Downstream projects must document LLM-specific choices in their briefs.

## Logging policy

- Add logging or observability only where it helps diagnose real behavior.
- Do not log secrets, credentials, private user data, or unnecessary payloads.
- Downstream projects must define their own observability tools.

## Post-launch policy

- For deployed changes, define post-launch validation before merge.
- Include rollback notes for risky or user-facing changes.
- Keep monitoring proportional to impact.

## Definition of done

- A brief exists for the change.
- Reuse and dependency decisions are documented.
- The implementation matches the approved scope.
- Configured checks were run and results are recorded.
- Risks, rollback, and security/privacy impact were considered.
- The PR is ready for human review.

## Forbidden behavior for AI agents

- Do not edit files outside the approved scope.
- Do not add application code to this template.
- Do not add package managers, frameworks, Docker, databases, auth, deployment, MCP, subagents, evals, mutation testing, OpenHands, or skills catalogs.
- Do not invent successful checks when real checks are not configured.
- Do not duplicate `AGENTS.md` as competing instructions.
- Do not make broad rewrites without an approved brief and plan.
