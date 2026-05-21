# Agentic Engineering Scorecard

An evidence-based skill for assessing how well a software team uses AI coding agents.

Most AI maturity models ask people how mature they think they are. This one asks the agent to inspect the working system first: repo instructions, skills, specs, tests, CI, tickets, PRs, git history, automations, and team workflow evidence.

This is mostly targeted at solo practitioners, founders, and small engineering teams. It intentionally stays away from heavyweight enterprise concerns such as procurement, centralized governance, legal policy, vendor management, and organization-wide change programs so it can stay focused on practical engineering workflow.

## Use The Skill

The canonical artifact is:

[skills/ai-engineering-maturity-assessment/SKILL.md](skills/ai-engineering-maturity-assessment/SKILL.md)

If your coding agent supports skills, import or copy that folder into your project’s skill location and adapt the setup section to your repo.

When adapting it, point the skill at:

- the repo or repos in scope
- ticketing and PR systems
- CI, docs, runbooks, and automations
- the AI tools your team actually uses
- local verification commands
- branch, worktree, port, environment, database/schema, review, and release conventions

Then ask your agent:

```text
Use the AI Engineering Maturity Assessment skill to assess this repo. Start with the setup/access phase, inspect evidence before asking me questions, and translate every miss into concrete next steps.
```

## If Your Tool Does Not Support Skills

Paste the skill file into the agent and say:

```text
Here is a skill I am considering for this project. Use it to assess our AI engineering maturity. Adapt it to this repo as needed, ask only the setup questions required to access evidence, and then produce the scorecard.
```

## What It Assesses

The scorecard asks whether the team has a practical operating model for agentic engineering:

- Can a fresh agent understand the project?
- Is there a deliberate single-tool or multi-tool strategy?
- Can one developer supervise multiple concurrent feature streams?
- Can an agent implement from a spec and verify its work?
- Are human-in-the-loop judgment gates explicit?
- Does review catch AI-specific failure modes?
- Can long-horizon work survive multiple sessions?
- Are recurring AI checks maintaining the engineering system?
- Do recurring threads, goals, queues, and automations keep work moving safely?
- Does the team maintain its AI instructions, skills, prompts, and rules?
- Is durable memory explicit and reviewable rather than trapped in chat transcripts?
- Is AI usage shared across the team rather than trapped in one person’s habits?

## Recommended Cadence

- **Weekly:** solo founder or team actively changing AI workflows.
- **Biweekly:** early-stage team shipping regularly.
- **Monthly:** stable team institutionalizing practices.
- **Quarterly:** executive-level reassessment, not prompt/skill hygiene.

Ask your agent to set this up as a recurring task where your tool supports scheduled automations or recurring workflows. For example:

```text
Set up the AI Engineering Maturity Assessment skill as a recurring task for this repo. Run it monthly, save each report, compare the results to the previous run, and recommend any changes for human review before editing shared instructions, skills, rules, or workflow docs.
```

Each run should produce a saved report so trend lines can be compared over time. A human should review proposed changes before applying them to shared instructions, skills, rules, or workflow docs.

## Status

This is an early v0.1 artifact. Expect the scorecard to evolve as the practice evolves.
