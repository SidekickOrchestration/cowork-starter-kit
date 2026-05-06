---
title: Contributing
aliases: [contributing, dev contributions, kit contributions]
status: active
created: 2026-05-05
---

# Contributing to the Cowork Starter Kit

Issues and PRs welcome. The kit is intentionally minimal. New skills, vertical-specific examples, and improved defaults are the highest-value additions. Anything that bloats the first-run experience will probably be declined or moved to a separate `examples/` branch.

Open an issue first if you are proposing a structural change to the folder scaffold or the CLAUDE.md template.

## Setup

```bash
cd ~/Repos
git clone https://github.com/SidekickOrchestration/cowork-starter-kit.git
cd cowork-starter-kit
```

Open the folder in Cowork to test changes locally. The five kit skills auto-load from `.claude/skills/` the moment you open the folder, so any edit to a `SKILL.md` is testable in the same session.

## What lands

- New skills that solve a recurring vertical-specific friction (with at least two named verticals where the friction shows up the same way)
- Bug fixes to existing skills (typo, broken format, incorrect frontmatter)
- README clarifications, especially anything that helps a non-technical first-time user
- New `.example` template files for `Reference/` or `People/` that demonstrate a useful pattern

## What does not land (or moves to a branch)

- Skills that target a single highly specialized vertical (better as a fork or as an `examples/` branch)
- Vertical-specific data files in `Reference/` (this is a generic kit; vertical content lives in vertical playbooks at sidekickorchestration.ai)
- Anything that adds setup steps to the five-minute quickstart
- Large code dependencies, build tools, or tooling that requires the user to install anything beyond Cowork

## Style

- Brand voice rules apply to anything Sidekick-attributed: no em dashes, no double dashes, no hype language. See the existing files for the tone.
- All `.md` and `.example` files require Karpathy frontmatter (`title`, `aliases`, `status`, `created`).
- Prefer short, specific examples over abstract framing.
- Active voice. No "is being processed" or "has been generated."

## Reporting issues

Open an issue at [github.com/SidekickOrchestration/cowork-starter-kit/issues](https://github.com/SidekickOrchestration/cowork-starter-kit/issues). Include:

- What you tried (the exact prompt or step)
- What happened
- What you expected
- Your Cowork version if you know it

## Maintainer

The kit is maintained by Sidekick Orchestration Ltd. (Vancouver, BC). Questions: [chase@sidekickorchestration.ai](mailto:chase@sidekickorchestration.ai).
