# Security Review Prompt

Read `AGENTS.md`, the relevant brief, and the proposed diff.

Review for security and privacy impact without assuming any stack.

Check:

- Secret handling.
- Authentication or authorization impact, if applicable.
- Data exposure or sensitive logging.
- Input validation and trust boundaries.
- Dependency or supply-chain risk.
- LLM-specific privacy or prompt-injection risk, if applicable.
- Rollback or incident response concerns.

Return concrete findings first, ordered by severity. If no issues are found, say so clearly and note any residual risk.
