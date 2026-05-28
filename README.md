# Awesome AI Agent Context [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Multi-tool installable context for AI agents — Claude Code, Cursor, Codex, Aider, Windsurf, MCP, and the rest, organised by what each repo does.

This directory lists public GitHub repositories that ship **installable context for AI agents** — skills, rules, MCP servers, methodology, behaviour-modification, prompt libraries, and adjacent shapes. We organise by **shape** (what the repo ships) rather than by tool. Each entry carries inline tags for tool ecosystem, install mechanism, and licence. Criteria for inclusion are applied at compile time; we do not commit to ongoing editorial curation.

By context-as-code. Maintained as a small open catalogue.

## Contents

- [Skill collections](#skill-collections)
- [Slash commands & subagents](#slash-commands--subagents)
- [Rules collections](#rules-collections)
- [Hooks](#hooks)
- [MCP servers](#mcp-servers)
- [Methodology & spec-driven frameworks](#methodology--spec-driven-frameworks)
- [Memory & context substrates](#memory--context-substrates)
- [Behaviour-modification skills](#behaviour-modification-skills)
- [Prompt & system-prompt libraries](#prompt--system-prompt-libraries)
- [Orchestration frameworks with bundled context](#orchestration-frameworks-with-bundled-context)
- [Other](#other)
- [Other discovery resources](#other-discovery-resources)
- [Validity criteria summary](#validity-criteria-summary)
- [About](#about)

## Skill collections

Repos shipping one or more agent skills — typically `SKILL.md` files or equivalent — intended to be copied into `.claude/skills/` or installed via marketplace or package. Includes both single-author small sets and large multi-harness libraries.

- [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills#readme) - 338 skills, 51 agents, and 87 commands across thirteen agent platforms. `Multi-tool` `Marketplace` `MIT`.
- [anthropics/skills](https://github.com/anthropics/skills#readme) - Anthropic's official skill collection across creative, technical, enterprise, and documentation domains. `Claude Code` `Marketplace` `Apache-2.0`.
- [github/awesome-copilot](https://github.com/github/awesome-copilot#readme) - GitHub's curated Copilot agents, skills, instructions, plugins, workflows, and hooks. `Copilot` `Marketplace` `MIT`.
- [google/skills](https://github.com/google/skills#readme) - Compact agent-first Markdown skills for Google Cloud — BigQuery, Cloud Run, GKE, Gemini APIs, and recipes. `Generic` `Package` `Apache-2.0`.
- [obra/superpowers](https://github.com/obra/superpowers#readme) - Engineering-process skills framework with TDD, debugging, and brainstorming primitives across eight agent harnesses. `Multi-tool` `Marketplace` `MIT`.
- [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills#readme) - More than 1,400 SKILL.md playbooks installable across many agents via an npm-based installer. `Multi-tool` `Package` `MIT`.
- [wshobson/agents](https://github.com/wshobson/agents#readme) - 83 plugins, 191 agents, 155 skills, and 102 commands across five agent harnesses. `Multi-tool` `Marketplace` `MIT`.

## Slash commands & subagents

Repos shipping slash-command definitions or subagent specifications. Distinct from skills in that they invoke specific actions or spawn delegated agents.

- [0xfurai/claude-code-subagents](https://github.com/0xfurai/claude-code-subagents#readme) - More than 100 production-ready development subagents for Claude Code. `Claude Code` `Copy` `MIT`.
- [qdhenry/Claude-Command-Suite](https://github.com/qdhenry/Claude-Command-Suite#readme) - 216 commands, 12 skills, and 54 agents bundled as installable workflows for Claude Code. `Claude Code` `Script` `MIT`.
- [vijaythecoder/awesome-claude-agents](https://github.com/vijaythecoder/awesome-claude-agents#readme) - Tech-lead orchestrator with a development team of specialised subagents. `Claude Code` `Copy` `MIT`.
- [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents#readme) - 154+ subagents organised across ten categories with an installer. `Claude Code` `Marketplace` `MIT`.
- [wshobson/commands](https://github.com/wshobson/commands#readme) - 57 production slash commands — 15 workflows and 42 utility tools. `Claude Code` `Marketplace` `MIT`.

## Rules collections

Repos shipping editor-embedded rule files (`.cursor/rules/`, `.windsurf/rules/`, etc.) — free-form behavioural guidance an agent loads as project context.

- [blefnk/awesome-cursor-rules](https://github.com/blefnk/awesome-cursor-rules#readme) - Composed Cursor, Windsurf, and Copilot rules tuned for a modern frontend stack. `Multi-tool` `Copy` `MIT`.
- [botingw/rulebook-ai](https://github.com/botingw/rulebook-ai#readme) - Universal rule template covering Copilot, Cursor, Roo, Cline, Windsurf, Claude, Gemini, Codex, Kilo, and Warp. `Multi-tool` `Copy` `MIT`.
- [continuedev/awesome-rules](https://github.com/continuedev/awesome-rules#readme) - Markdown and YAML rules for Cursor and Continue.dev following the amplified.dev standard. `Multi-tool` `Copy` `Apache-2.0`.
- [instructa/ai-prompts](https://github.com/instructa/ai-prompts#readme) - Curated rules for Cursor, Cline, Windsurf, and Copilot. `Multi-tool` `Copy` `MIT`.
- [sanjeed5/awesome-cursor-rules-mdc](https://github.com/sanjeed5/awesome-cursor-rules-mdc#readme) - CLI generator plus curated .mdc rule files for Cursor. `Cursor` `Script` `MIT`.

## Hooks

Lifecycle hook scripts (e.g. `UserPromptSubmit`, `Stop`, pre-commit equivalents). Copy-paste shell scripts plus `settings.json` snippets.

- [CodyLunders/claude-code-hooks-library](https://github.com/CodyLunders/claude-code-hooks-library#readme) - 60+ plug-and-play hooks covering security, quality, Git, and observability for Claude Code. `Claude Code` `Copy` `MIT`.
- [disler/claude-code-hooks-mastery](https://github.com/disler/claude-code-hooks-mastery#readme) - All 13 Claude Code hook events implemented and validated. `Claude Code` `Copy` `MIT`.
- [karanb192/claude-code-hooks](https://github.com/karanb192/claude-code-hooks#readme) - Curated copy-paste hooks for Claude Code. `Claude Code` `Copy` `MIT`.

## MCP servers

Model Context Protocol servers. Each server gives an agent new tool capabilities via standardised tool-calling.

- [github/github-mcp-server](https://github.com/github/github-mcp-server#readme) - GitHub's official MCP server providing repo, issue, and pull-request access to AI agents. `MCP` `Package` `MIT`.
- [hashicorp/terraform-mcp-server](https://github.com/hashicorp/terraform-mcp-server#readme) - HashiCorp's official Terraform MCP server. `MCP` `Package` `MPL-2.0`.
- [makenotion/claude-code-notion-plugin](https://github.com/makenotion/claude-code-notion-plugin#readme) - Notion skills, slash commands, and MCP integration for Claude Code. `Claude Code` `Marketplace` `MIT`.
- [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp#readme) - Microsoft's official Playwright MCP for browser automation. `MCP` `Package` `Apache-2.0`.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers#readme) - Reference MCP servers — Everything, Fetch, Filesystem, Git, Memory, Sequential Thinking, and Time. `MCP` `Package` `MIT`.
- [upstash/context7](https://github.com/upstash/context7#readme) - MCP server providing up-to-date version-specific documentation for hundreds of libraries. `MCP` `Package` `MIT`.

## Methodology & spec-driven frameworks

Repos codifying a methodology an agent follows — TDD-first, plan-first, spec-then-implement, ADR-driven. Installable as commands plus templates plus workflow definitions.

- [bmad-code-org/BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD#readme) - Breakthrough Method for Agile AI Development with 12 domain expert agents and 34 workflows across the agile lifecycle. `Multi-tool` `Package` `MIT`.
- [buildermethods/agent-os](https://github.com/buildermethods/agent-os#readme) - Agent OS for injecting codebase standards and spec-driven development workflow into AI coding agents. `Multi-tool` `Script` `MIT`.
- [github/spec-kit](https://github.com/github/spec-kit#readme) - Specify CLI installing slash commands and templates for spec-driven development into 30+ AI coding agents. `Multi-tool` `Package` `MIT`.
- [humanlayer/advanced-context-engineering-for-coding-agents](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents#readme) - Practices and patterns for context engineering with AI coding agents. `Generic` `Copy` `MIT`.
- [IBM/iac-spec-kit](https://github.com/IBM/iac-spec-kit#readme) - Spec-driven development applied to infrastructure-as-code workflows. `Multi-tool` `Copy` `Apache-2.0`.

## Memory & context substrates

Repos establishing a persistence layer under agent sessions — memory banks, session-context captures, cross-session knowledge stores.

- [GreatScottyMac/roo-code-memory-bank](https://github.com/GreatScottyMac/roo-code-memory-bank#readme) - Structured memory bank for Roo Code, persisting context across sessions. `Roo Code` `Copy` `MIT`.
- [rohitg00/agentmemory](https://github.com/rohitg00/agentmemory#readme) - Persistent memory across Claude, Cursor, Gemini, Codex, Hermes, and other MCP clients. `Multi-tool` `Package` `Apache-2.0`.
- [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem#readme) - Captures, compresses, and injects context across agent sessions for multiple tools. `Multi-tool` `Package` `MIT`.
- [volcengine/OpenViking](https://github.com/volcengine/OpenViking#readme) - Filesystem-based context database unifying agent memories, resources, and skills with tiered loading. `Multi-tool` `Package` `AGPL-3.0`.

## Behaviour-modification skills

Repos that modify *how* the agent operates rather than *what it knows*.

### Output-discipline

Terser, compressed, or voice-rewritten output.

- [Aboudjem/humanizer-skill](https://github.com/Aboudjem/humanizer-skill#readme) - Detects AI writing patterns and rewrites with five voice profiles. `Multi-tool` `Copy` `MIT`.
- [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman#readme) - Token-compression skill that makes the agent itself terser, plus companion slash commands. `Multi-tool` `Script` `MIT`.
- [Redclawww/savethetokens](https://github.com/Redclawww/savethetokens#readme) - Proactive context compaction, pruning, and session hygiene for Claude Code and 30 other agents. `Multi-tool` `Package` `MIT`.

### Workflow-discipline

Plan-first, TDD-first, ask-first.

- [6missedcalls/ultraplan](https://github.com/6missedcalls/ultraplan#readme) - Structured pre-code planning session with requirements interview and parallel codebase exploration. `Claude Code` `Copy` `MIT`.
- [nizos/tdd-guard](https://github.com/nizos/tdd-guard#readme) - Blocks implementation without a failing test and enforces minimal-implementation discipline across nine test frameworks. `Claude Code` `Plugin` `MIT`.
- [OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files#readme) - Manus-style persistent markdown planning workflow that forces plan files before coding. `Claude Code` `Copy` `MIT`.

### Persona & posture

Skeptic, devil's advocate, Socratic.

- [aaddrick/contrarian](https://github.com/aaddrick/contrarian#readme) - Devil's-advocate subagent that steel-mans proposals with severity-rated findings. `Claude Code` `Copy` `Unlicense`.
- [brandonsimpson/devils-advocate](https://github.com/brandonsimpson/devils-advocate#readme) - Adversarial self-critique with an independent subagent review and binary pass/fail across 20 code and 22 plan criteria. `Claude Code` `Marketplace` `MIT`.
- [dpaola2/rubber-duck](https://github.com/dpaola2/rubber-duck#readme) - Socratic debugging partner that asks questions instead of answering, through a five-phase walk-through. `Claude Code` `Copy` `MIT`.

### Constraint enforcement

Commit format, ADR conventions, format rules.

- [inprojectspl/conventional-commits](https://github.com/inprojectspl/conventional-commits#readme) - Enforces Conventional Commits v1.0.0 with types, scopes, and 72-character first lines. `Claude Code` `Copy` `MIT`.
- [microsoft/AI-Engineering-Coach](https://github.com/microsoft/AI-Engineering-Coach#readme) - VS Code extension analysing local AI coding sessions against 44 markdown anti-pattern rules. `Multi-tool` `Extension` `MIT`.

### Anti-sycophancy

Honest-feedback posture and anti-hallucination discipline.

- [0xcjl/anti-sycophancy](https://github.com/0xcjl/anti-sycophancy#readme) - Three-layer defence with a prompt-rewriting hook, skill, and memory rules to keep the agent critical. `Multi-tool` `Package` `MIT`.

### Self-correction & reflection

Memory-as-discipline and continual-learning from corrections.

- [BayramAnnakov/claude-reflect](https://github.com/BayramAnnakov/claude-reflect#readme) - Captures corrections and syncs them to CLAUDE.md and AGENTS.md so the agent stops repeating mistakes. `Multi-tool` `Marketplace` `MIT`.

## Prompt & system-prompt libraries

Curated prompt collections with a clear install posture (CLI, package, structured folder to vendor).

- [0xeb/TheBigPromptLibrary](https://github.com/0xeb/TheBigPromptLibrary#readme) - Multi-LLM prompts, system-prompts, and instructions library. `Generic` `Copy` `MIT`.
- [harish-garg/gemini-cli-prompt-library](https://github.com/harish-garg/gemini-cli-prompt-library#readme) - Curated prompts installable as a Gemini CLI Extension. `Gemini` `Extension` `MIT`.
- [thibaultyou/prompt-library](https://github.com/thibaultyou/prompt-library#readme) - Prompts with metadata and a CLI for CI and local workflows. `Generic` `Package` `MIT`.

## Orchestration frameworks with bundled context

Multi-agent orchestration runtimes that install their own agent definitions, skills, or commands alongside the framework.

- [HKUDS/CLI-Anything](https://github.com/HKUDS/CLI-Anything#readme) - Plugin with 40+ generated CLI harnesses and a Hub package manager turning GUI software into agent-callable CLIs. `Multi-tool` `Script` `Apache-2.0`.
- [Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything#readme) - Cross-CLI plugin with five `/understand*` skills that build and query a code knowledge graph. `Multi-tool` `Script` `MIT`.
- [ruvnet/ruflo](https://github.com/ruvnet/ruflo#readme) - Claude-Flow multi-agent swarm orchestration platform with RAG and Claude / Codex integration. `Multi-tool` `Package` `MIT`.
- [SuperClaude-Org/SuperClaude_Framework](https://github.com/SuperClaude-Org/SuperClaude_Framework#readme) - 30 commands, 20 agents, 7 modes, and 8 MCP integrations for Claude Code. `Claude Code` `Package` `MIT`.

## Other

Hubs that aggregate skills, agents, commands, hooks, and plugins; and adjacent surfaces shipping installable content that doesn't fit cleanly into the categories above.

- [Aider-AI/conventions](https://github.com/Aider-AI/conventions#readme) - Community-contributed CONVENTIONS.md files for the aider AI coding assistant. `Aider` `Copy` `Apache-2.0`.
- [davepoon/buildwithclaude](https://github.com/davepoon/buildwithclaude#readme) - Hub aggregating skills, agents, commands, hooks, plugins, and marketplaces for Claude Code. `Claude Code` `Marketplace` `MIT`.

## Other discovery resources

Adjacent inventory resources outside this directory's scope. We mine them for discovery and link to them as the next-best places to look for things we don't list. We don't list awesome-lists themselves as entries here — they are linked below instead.

### Awesome-lists by tool

- [Code-and-Sorts/awesome-copilot-agents](https://github.com/Code-and-Sorts/awesome-copilot-agents#readme) - Curated agent.md, instruction, prompt, skill, and MCP files for GitHub Copilot.
- [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code#readme) - Curated list of Claude Code resources.
- [ichoosetoaccept/awesome-windsurf](https://github.com/ichoosetoaccept/awesome-windsurf#readme) - Curated list of Windsurf rules and resources.
- [Ischca/awesome-agents-md](https://github.com/Ischca/awesome-agents-md#readme) - Curated list of AGENTS.md example files and references.
- [Meirtz/Awesome-Context-Engineering](https://github.com/Meirtz/Awesome-Context-Engineering#readme) - Curated list of context-engineering resources and patterns.
- [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules#readme) - Curated list of Cursor rules.
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers#readme) - Curated list of Model Context Protocol servers.
- [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills#readme) - Curated list of Claude skills.

### Marketplaces and vendor / official registries

- [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official#readme) - Anthropic-managed plugin directory and marketplace.
- [modelcontextprotocol/registry](https://github.com/modelcontextprotocol/registry#readme) - Community MCP server registry service.

## Validity criteria summary

In short: each entry ships installable context that becomes part of the consumer's AI-agent workflow; is publicly licensed; has a clear install or consume path; and isn't itself a product that uses AI to deliver an unrelated value. See [CRITERIA.md](CRITERIA.md) for the full criteria, edge-case rulings, and worked boundary examples.

We apply criteria **at compile time** — when an entry is admitted. We do not commit to ongoing editorial curation. Entries reflect their state at admission and during periodic sweeps.

## About

This directory is part of the context-as-code initiative — codifying expertise so it compounds. The directory itself is independent of any other context-as-code product; it stands on its own as a public catalogue.

- Operated by: Zebra Labs Ltd.
- Brand: context-as-code.
- Licence: [CC0-1.0](LICENSE) — public domain, no rights reserved on the catalogue content. Listed projects keep their own licences.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose entries, report stale entries, or request changes. We accept submissions via GitHub Pull Request; issue templates exist for non-PR-shaped requests.

By participating, you agree to the [Code of Conduct](code-of-conduct.md).
