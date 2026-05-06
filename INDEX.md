---
title: Kit Index
aliases: [INDEX, kit index, file index]
status: active
created: 2026-05-05
---

# INDEX

Concept-to-file lookup for the Cowork Starter Kit. If you remember what you are looking for but not where it lives, start here.

---

## Entry points

- [Getting_Started.pdf](Getting_Started.pdf) - the human entry point, open this first
- [README.md](README.md) - what the kit is, who it is for, five-minute quickstart
- [bootstrap.md](bootstrap.md) - the same first-paste prompt as the PDF, in text form
- [CLAUDE.md](CLAUDE.md) - the practice template Claude reads at the top of every session
- [example-starter-session.md](example-starter-session.md) - what a first session actually looks like
- [CONTRIBUTING.md](CONTRIBUTING.md) - for developers and contributors only
- [LICENSE](LICENSE) - Apache License 2.0

## Folders

- [Reference/](Reference/) - stable docs you write once and refer to often
- [Active/](Active/) - in-progress work, drafts, build trackers
- [People/](People/) - one file per client or contact
- [TO DELETE/](TO%20DELETE/) - safe place to move things instead of deleting
- [.claude/skills/](.claude/skills/) - installable Cowork skills

## Skills

| Skill | Mode | What it does |
|-------|------|--------------|
| [after-meeting-brief](.claude/skills/after-meeting-brief/SKILL.md) | Capture | Voice notes or scratch in, structured client follow-up out |
| [product-comparison](.claude/skills/product-comparison/SKILL.md) | Produce | Two or three carrier or product PDFs in, side-by-side comparison out |
| [pipeline-pulse](.claude/skills/pipeline-pulse/SKILL.md) | Surface | Client list with last-contact dates in, who needs attention this week out |
| [document-generator](.claude/skills/document-generator/SKILL.md) | Produce | Meeting notes plus a document type in, first-draft document out |
| [weekly-capture](.claude/skills/weekly-capture/SKILL.md) | Surface | The week's notes, calendar, and emails in, Friday distill out |

## Common questions

**Where do I customize my name and tone?**
[CLAUDE.md](CLAUDE.md), the sections marked `# CUSTOMIZE`.

**Where do I add a new skill?**
Create a new folder under `.claude/skills/[your-skill-name]/` with a `SKILL.md` file inside. Use any existing skill as a template.

**Where do client-specific notes live?**
[People/](People/), one file per client. Naming convention: `FirstName_LastName.md`.

**Where do I put work in progress?**
[Active/](Active/). Move it out (to `Reference/` or `TO DELETE/`) when it stabilizes.

**How do I know if a skill fired correctly?**
The skill should produce its specific output format. If Claude responded conversationally without the structured output, the trigger phrase did not match. Check the `description` field in the skill's frontmatter and either rephrase your request or edit the description to fire on more phrases.

**Can I delete the example skills if they do not fit my practice?**
Yes. Move the folder to `TO DELETE/` (or remove it from the repo entirely if you forked the kit). The other skills will keep working.

## Upstream

- [Independent Advisor Playbook](https://sidekickorchestration.ai) - the PDF this kit pairs with. Page 8 references this repo.
- [Sidekick Orchestration](https://sidekickorchestration.ai) - the company that maintains the kit.
