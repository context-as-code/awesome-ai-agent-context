# Shape Categories

This directory organises entries by **shape** — what kind of installable artefact the repo ships — rather than by tool or area. Categories below define the top-level structure of the README. They emerged from a discovery pass across ~158 candidate repos; expect them to evolve over time. Propose changes via an issue.

## Top-level categories

1. **Skill collections (single & multi-harness)** — Repos that ship one or more agent skills, typically as `SKILL.md` files or equivalent, intended to be copied into `.claude/skills/` or installed via marketplace / package. Includes both single-author small sets and large multi-harness libraries that generate per-tool artefacts.
2. **Slash commands & subagents** — Repos that ship slash-command definitions (`/foo`-style) or subagent specifications (delegatable agent personas). Distinct from skills in that they invoke specific actions or spawn sub-agents.
3. **Rules collections (Cursor / Windsurf / Cline)** — Repos that ship editor-embedded rule files (`.cursor/rules/`, `.windsurf/rules/`, etc.) — free-form behavioural guidance an agent loads as project context.
4. **Hooks** — Repos that ship lifecycle hook scripts (e.g. `UserPromptSubmit`, `Stop`, pre-commit equivalents). Copy-paste shell scripts + `settings.json` snippets.
5. **MCP servers** — Repos shipping Model Context Protocol servers. Each server gives an agent new tool capabilities via standardised tool-calling.
6. **Methodology / spec-driven frameworks** — Repos that codify a methodology an agent follows (TDD-first, plan-first, spec-then-implement, ADR-driven, etc.). Installable as commands + templates + workflow definitions.
7. **Memory / context substrates** — Repos that establish a persistence layer under agent sessions (memory banks, session-context captures, cross-session knowledge stores). Installed once; the agent reads / writes through it.
8. **Behaviour-modification skills** — Repos that modify *how* the agent operates rather than *what it knows*. Sub-clusters:
   - 8a. **Output-discipline** — terser / compressed / voice-rewritten output.
   - 8b. **Workflow-discipline** — plan-first / TDD / ask-first.
   - 8c. **Persona / posture** — skeptic / devil's advocate / Socratic.
   - 8d. **Constraint enforcement** — commit format / ADR conventions / format rules.
   - 8e. **Anti-sycophancy** — honest-feedback posture, anti-hallucination discipline.
   - 8f. **Self-correction / reflection** — memory-as-discipline, continual-learning from corrections.
9. **Prompt / system-prompt libraries** — Repos shipping curated prompt collections with a clear install posture (CLI, package, structured folder to vendor). Excludes "study only" leaked-prompt archives.
10. **Orchestration frameworks with bundled context** — Multi-agent orchestration runtimes that install their own agent definitions, skills, or commands alongside the framework.
11. **Other / aggregator hubs / format anchors** — Hubs that aggregate skills/agents/commands/hooks/plugins; format-spec repos shipping copyable templates (distinct from pure RFC-style format docs which are out of scope).

## Sub-cluster review

The sub-clusters under category 8 (Behaviour-modification) are the only deep nesting at V0.1.0. If sub-clusters emerge elsewhere with enough entries to warrant grouping, we'll introduce them — propose via issue.

## How to add or change categories

- Propose a new category, split an existing one, or move an entry between categories by opening an issue.
- The operator decides; rationale recorded in the issue thread and in this file's revision history.
- Reviewed annually OR ad-hoc when a new shape emerges that doesn't fit cleanly.
