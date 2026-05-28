# Validity Criteria

This document defines what qualifies for inclusion in the directory. Criteria are applied **at compile time** — when an entry is added or reviewed. We do not claim ongoing editorial curation; entries reflect their state at admission and during periodic sweeps. Propose changes to these criteria via issue.

## Core criteria — all four must hold

A public GitHub repository qualifies if:

1. **Intent: ships installable context as the primary deliverable.** The repo's main asset is content meant to be pulled into another repo to shape AI-agent behaviour. Acceptable: skills, commands, agents, rules, prompts, system-prompt collections, knowledge files / methodology playbooks, agent.md / AGENTS.md collections, MCP server configurations, prompt-library bundles. Not acceptable: a product that *uses* AI internally (e.g. a code-review bot, a customer-support AI, a voice-AI framework); a tutorial repo whose primary output is a blog post or video.

2. **Installable / consumable posture.** A clear delivery mechanism exists that brings what the repo ships into the consumer's AI-agent workflow. Acceptable mechanisms include: install script, "copy these files to `.claude/` / `.cursor/` / `.agent/`" instructions, npm / pip / cargo / cargo-install package, CLI, plugin marketplace entry, clone-and-symlink guidance, MCP server, IDE / editor extension whose value is its bundled content (e.g. a VS Code extension shipping rules / skills / instructions), binary that intercepts or extends agent operation, or a coherent folder structure the consumer vendors.

   The consumption pathway can be agent-direct OR mediated through a tool / binary / extension the human runs alongside their agent. The validity test is: **does the repo ship something that becomes part of the consumer's AI-agent workflow** — content the agent reads, a tool the agent uses, an extension delivering content, a binary intercepting agent operation, or a package extending agent capabilities.

3. **AI-agent-consumable shape.** The content is structured for agent consumption (markdown with frontmatter, rule files, prompt files, structured directories) rather than free-form human-only documentation. Mixed repos qualify if the agent-consumable portion is the primary asset.

4. **Public + usable.** Public repo with some licence (no-licence is a red flag worth tagging, not necessarily an exclusion).

## Edge-case rulings

| Case | Ruling |
|---|---|
| Awesome-* / curated link lists | **Exclude from this directory.** We mine awesome-lists for discovery; we link to the best of them as adjacent inventory resources. We don't list them as entries — that would make us an aggregator of aggregators. |
| MCP server repos | **Include**, tagged distinctly (`MCP` tool tag). Different install model from skills/rules/prompts but still "pull capability into a repo for an AI agent." |
| Single-skill / single-prompt / single-agent repos | **Include** if criteria 1–4 hold. Likely the largest population. |
| Tool-specific collections (Cursor / Claude Code / Codex / etc.) | **Include all.** Directory stays tool-agnostic; entries carry tool tags per-entry. |
| Template / boilerplate repos | **Include** if the context portion is meaningful. Exclude if the template is mostly framework boilerplate with a token AGENTS.md. |
| Personal opinionated prompt libraries / system-prompt dumps | **Include** if criteria 1–4 hold. Install posture may just be "copy this folder" — still qualifies. |
| Sample / demo / tutorial repos | **Exclude.** Demos paired with tutorial posts are not directory entries. But if a post *references* a separate substantive repo, evaluate that referenced repo on its own merits. |
| Knowledge / methodology repos (referenced-by-agent rather than installed-as-context) | **Include.** Methodology playbooks, architectural decision libraries, codified expertise. |
| Template / starter repos (a copyable file or set of files that a consumer adapts into their own repo) | **Include** if the template is itself the primary deliverable and meets criteria 1, 3, 4. The copying-and-adapting is a valid install model. Counter-example: a repo whose primary deliverable is a specification document describing the format (e.g. `agentsmd/agents.md`) — these are RFC-shaped, not template-shaped, and remain excluded. |
| Leaked system-prompt collections | **Exclude.** They're markdown files for humans to study — no install script, no agent-consumable structure, the consumer is reading not installing. They are culturally significant but don't fit the directory's intent. |

## Worked boundary examples

These document where the line has been drawn for borderline cases, supporting future decision consistency.

| Pair | Distinction | Outcome |
|---|---|---|
| `JuliusBrussee/caveman` and `yves-gugger/lean-ctx` (both about token reduction) | Both become part of the consumer's AI-agent workflow — one as a skill the agent installs, the other as a binary that intercepts agent output. Different install mechanisms, same validity. | **Both INCLUDE.** Tagged differently by install mechanism. |
| `Workflowsio/company-os-starter-kit` (template + setup interview) vs `agentsmd/agents.md` (spec + reference website) | Both reference a "format." The starter kit ships an actual usable template a consumer adapts. The spec repo ships a specification document; the example file is illustrative — consumers are expected to write their own following the spec. | Starter kit INCLUDE; spec repo EXCLUDE. |
| `rohitg00/agentmemory` (MCP + plugins) vs `superlinked/sie` (RAG infrastructure server) | Both are servers. `agentmemory` ships as installable agent-context — an MCP server an agent talks to via standardised tool-calling, plus native plugins. `sie` is back-end inference infrastructure a product is built on. | agentmemory INCLUDE; sie EXCLUDE. |
| `microsoft/AI-Engineering-Coach` (VS Code extension shipping 44 rules) vs `Kirill89/reviewcerberus` (AI-powered code-review bot) | AI-Engineering-Coach ships a VS Code extension whose value is the rules + dashboard shaping how the developer uses their AI agents — the extension becomes part of the consumer's AI-coding workflow. reviewcerberus is a separate code-review bot triggered on PRs; it uses AI internally but doesn't extend the consumer's existing Claude Code / Cursor / Codex workflow. | AI-Engineering-Coach INCLUDE; reviewcerberus EXCLUDE. |
| `pipecat-ai/pipecat` (framework for building voice-AI products) vs MCP servers (e.g. `upstash/context7`) | pipecat is a Python framework for *building new AI products*. MCP servers become part of the consumer's AI-agent workflow — the agent talks to them via standardised tool-calling. | pipecat EXCLUDE; MCP servers INCLUDE. |

## What we mean by "criteria applied at compile time, not ongoing curation"

- **At admission:** every entry was checked against criteria 1–4 and the edge-case rulings.
- **In sweeps:** quarterly manual review checks for dead links, archived repos, renamed repos. We do not re-test every entry against criteria each sweep.
- **What we do NOT promise:** that every listed repo will still meet criteria a year from now, that descriptions stay current to the day, or that we will proactively remove repos that drift.
- **What you can do:** if an entry has drifted, open an issue (using the `report-stale` template) and we'll triage.

## Criteria changes

Material changes to criteria require a version bump in this file and an audit of existing entries. Minor wording clarifications can be applied without version bump. History is in the repo's git log.
