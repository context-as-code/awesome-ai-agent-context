# Contributing

Thanks for considering a contribution. This directory is a list of public GitHub repositories that ship installable context for AI agents. Contributions take three forms: **suggesting a new entry**, **reporting a stale entry**, and **requesting removal of your own repo**.

## Quick reference

| You want to | Use |
|---|---|
| Suggest a new entry | Open a Pull Request, or open the `suggest-entry` issue if you can't open a PR |
| Report a dead link / archived repo | Open the `report-stale` issue |
| Ask for your repo to be updated or removed | Open the `remove-my-entry` issue |
| Propose a category change, split, or merge | Open a plain issue |
| Anything else | Open a plain issue or discussion |

## Before you submit an entry

Check it against the validity criteria in [CRITERIA.md](./CRITERIA.md). The four core criteria are:

1. **Intent** — primary deliverable is installable context (skills / rules / prompts / MCP servers / methodology / behaviour-modification / etc.). Not an AI product that uses AI internally.
2. **Installable / consumable posture** — clear path for the repo's content to become part of the consumer's AI-agent workflow.
3. **AI-agent-consumable shape** — structured for agent consumption.
4. **Public + usable** — public repo with some licence.

Plus the edge-case rulings in [CRITERIA.md](./CRITERIA.md) — please read these before submitting.

## How to submit an entry (Pull Request path)

1. Fork the repo.
2. Identify the right shape category for the entry — see [CATEGORIES.md](./CATEGORIES.md).
3. Add a new line to the appropriate section of [README.md](./README.md) using the canonical format:

   ```
   - [Name](https://github.com/owner/repo#readme) - One-line description ending with a period. `Tool-Tag` `Install-Mechanism` `Licence`
   ```

   Format rules (enforced by `awesome-lint`):
   - Use a regular hyphen with spaces (` - `) as the separator. Not em-dash, not en-dash.
   - Description starts with an uppercase letter and ends with a period (or `!?…)` / emoji).
   - URL ends with `#readme` so the link opens at the README anchor.
   - Description is about the project, not about this list.
   - No marketing-tone language ("blazing fast", "next-generation", "the best").
   - Inline tags in backticks at the end, ordered: tool tag(s) → install mechanism → licence.

4. Keep entries sorted alphabetically within their section (case-insensitive on the name).
5. Open a Pull Request. The PR template will prompt for required metadata + a criteria self-check.
6. `awesome-lint` runs automatically; if it fails, fix and push again.
7. Wait for review. See cadence note below.

## How to submit an entry (issue path, if you can't open a PR)

Use the `suggest-entry` issue template. Fill in the same metadata the PR template would prompt for. We'll open a PR on your behalf if the submission qualifies.

## Cadence — review and merge

**Best-effort, not guaranteed.** This directory is maintained by a small team without committed review SLA. We aim to triage submissions within a reasonable timeframe but make no promise on turnaround. If your PR has been open for more than a few weeks without response, feel free to comment to nudge.

The validity check is operator-decided. We reject submissions that don't meet criteria and explain why; you're welcome to revise and resubmit.

## Categorisation governance

The shape categories in [CATEGORIES.md](./CATEGORIES.md) emerged from a discovery pass and may evolve. Propose category changes via plain issue. The operator decides; rationale is recorded in the issue thread.

## What we explicitly don't accept

- AI products that use AI internally to deliver value (review bots, customer-support AI, voice-AI frameworks, etc.). These are out of scope per criterion 1.
- Awesome-lists themselves. They are discovery sources we mine; we link to the best of them, but we don't list them as entries.
- Demo / tutorial / sample repos paired with blog posts. If the referenced repo is a substantive installable artefact, the *repo* may qualify on its own merits — but the post isn't the entry.
- Leaked system-prompt collections. These are reference / study material, not installable agent context.
- Repos with marketing-tone descriptions. Plain, factual one-liners only.
- AI-generated entry content for the list itself. (Different from "we list AI tooling" — that's fine.) The list is curated by humans.

## Code of Conduct

By participating, you agree to abide by the [Contributor Covenant](./code-of-conduct.md). Be respectful; assume good faith.

## Licence

By contributing, you agree your contributions are licensed under [CC0-1.0](./LICENSE), the same as the rest of the directory content.
