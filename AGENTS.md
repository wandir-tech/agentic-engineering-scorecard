# Agentic Engineering Scorecard Instructions

This repo contains a reusable scorecard prompt and skill for assessing agentic engineering maturity.

## Source Of Truth

- Canonical skill: `skills/ai-engineering-maturity-assessment/SKILL.md`

Keep the full assessment logic in the canonical skill. The README is for humans and should not duplicate the full scorecard.

## Editing Guidance

- Preserve the evidence-first structure: inspect repo/tool evidence before asking humans.
- Keep the scorecard tool-neutral across Codex, Claude Code, Cursor, Copilot, and future coding agents.
- Do not turn development-environment concurrency into a vendor-feature checklist. Score whether the project can support multiple safe concurrent feature streams.
- Treat human-in-the-loop as risk-based judgment gates, not blanket approval of everything.
- When adding a new maturity question, make sure its misses translate into next steps.
