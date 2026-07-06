# Agentic Engineering Scorecard

An evidence-based skill for assessing how well a software team uses AI coding agents.

Most AI maturity models ask people how mature they think they are. This one asks the agent to inspect the working system first: repo instructions, skills, specs, tests, CI, tickets, PRs, git history, automations, and team workflow evidence.

This is mostly targeted at solo practitioners, founders, and small engineering teams. It intentionally stays away from heavyweight enterprise concerns such as procurement, centralized governance, legal policy, vendor management, and organization-wide change programs so it can stay focused on practical engineering workflow.

Related blog post: https://fabrica.tech/blog/ai-engineering-maturity-scorecard/

## Current Version

Skill version: `0.3.0`

This version adds a new maturity question on keeping autonomous and recurring agent loops honest (independent evaluation, external feedback, reversible decisions, human check-in cadence), and strengthens existing questions with: generative/randomized testing as verification evidence, enforced-vs-prose guardrails matched to agent volume, false-positive discipline for agent-generated findings, variance-aware adoption of workflow changes, and treating agent-produced analyses as drafts.

Previous 0.2.0 additions: portfolio-oriented orientation, repo/package archetypes, applicability/N/A handling, explicit aggregate score calculation, and a stable report contract for teams collecting results across many repos.

## Use The Skill

The canonical artifact is:

[skills/ai-engineering-maturity-assessment/SKILL.md](skills/ai-engineering-maturity-assessment/SKILL.md)

Install it with the Skills CLI:

```bash
npx skills add wandir-tech/agentic-engineering-scorecard --skill ai-engineering-maturity-assessment
```

If your coding agent supports skills, import or copy that folder into your project’s skill location and adapt the setup section to your repo.

When adapting it, point the skill at:

- the repo or repos in scope
- ticketing and PR systems
- CI, docs, runbooks, and automations
- connected chat, support, observability, and release systems agents can inspect
- the AI tools your team actually uses
- local verification commands
- branch, worktree, port, environment, database/schema, review, and release conventions

Then ask your agent:

```text
Use the AI Engineering Maturity Assessment skill to assess this repo. Start with the setup/access phase, inspect evidence before asking me questions, and translate every miss into concrete next steps.
```

## Portfolio Or Manager Workflow

For portfolio-wide use, have each team member run the same skill version and default output format against the repo or package they know best. Each report should keep the `assessment_metadata` block so results can be consolidated by repo/package archetype, applicable score count, confidence, and common action category.

When a repo contains multiple packages, apps, SDKs, test suites, libraries, or sample apps, the agent should first decide whether each unit belongs in the same assessment, needs a separate assessment, is supporting evidence, or is out of scope. If the answer is not obvious after cursory inspection, it should ask before scoring.

## If Your Tool Does Not Support Skills

Paste the skill file into the agent and say:

```text
Here is a skill I am considering for this project. Use it to assess our AI engineering maturity. Adapt it to this repo as needed, ask only the setup questions required to access evidence, and then produce the scorecard.
```

## What It Assesses

The scorecard asks whether the team has a practical operating model for agentic engineering:

- Can a fresh agent understand the project?
- Is there a deliberate single-tool or multi-tool strategy?
- Are agents connected to the actual work systems: tickets, PRs, chat, docs, CI, support, and observability?
- Can one developer supervise multiple concurrent feature streams?
- Can an agent implement from a spec and verify its work?
- Are human-in-the-loop judgment gates explicit?
- Does review catch AI-specific failure modes?
- Can long-horizon work survive multiple sessions?
- Are recurring AI checks maintaining the engineering system?
- Do recurring threads, goals, queues, and automations keep work moving safely?
- Are autonomous or recurring agent loops kept honest by independent evaluation, external feedback, and human check-ins?
- Does verification include generative or randomized testing that can constrain agent-scale code volume?
- Are workflow and instruction changes validated against run-to-run variance rather than single anecdotes?
- Does the team maintain its AI instructions, skills, prompts, and rules?
- Is durable memory explicit and reviewable rather than trapped in chat transcripts?
- Are useful tool-specific practices shared through repo artifacts rather than trapped in one contributor’s private setup?
- Is AI usage shared across the team rather than trapped in one person’s habits?

## Recommended Cadence

- **Weekly:** solo founder or team actively changing AI workflows.
- **Biweekly:** early-stage team shipping regularly.
- **Monthly:** stable team institutionalizing practices.
- **Quarterly:** executive-level reassessment, not prompt/skill hygiene.

Ask your agent to set this up as a recurring task where your tool supports scheduled automations or recurring workflows. For example:

```text
Set up the AI Engineering Maturity Assessment skill as a recurring task for this repo. Run it monthly, save each report, compare the results to the previous run, and recommend any changes for Human review before editing shared instructions, skills, rules, or workflow docs.

Scan https://github.com/wandir-tech/agentic-engineering-scorecard for updates and check in with a Human if changes to the scorecard are needed before running the next assessment.
```

Each run should produce a saved report so trend lines can be compared over time. A human should review proposed changes before applying them to shared instructions, skills, rules, or workflow docs.

## Distribution

This repo is structured so the skill can be copied manually or installed by tools that understand `SKILL.md` directories.

The root `skills.sh.json` groups the skill for the repo page on skills.sh. It only affects skills.sh display; the CLI discovers the skill from the `SKILL.md` frontmatter.

Review any installed skill before using it, especially if installing through a public directory or marketplace.

## Status

This is an early v0.2 artifact. Expect the scorecard to evolve as the practice evolves.
