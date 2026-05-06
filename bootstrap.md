---
title: Bootstrap Prompt
aliases: [bootstrap, first prompt, kit bootstrap, day-one prompt]
status: active
created: 2026-05-05
---

# Bootstrap Prompt

Copy everything below the line into your first Cowork message. Send it. Claude will load the kit context, introduce itself, and walk you through your first task.

You only paste this once. Future sessions are normal: you open Cowork, Claude reads `CLAUDE.md` automatically, you start working.

---

I just set up the Cowork Starter Kit in this folder and opened it in Cowork. This is my first session. Walk me through the setup.

Step 1. Read these files in this order:
1. `README.md` (top of repo) - what the kit is
2. `CLAUDE.md` (top of repo) - my practice template
3. `.claude/skills/README.md` - the skills convention
4. The five `SKILL.md` files under `.claude/skills/` (one per skill)

Step 2. Confirm out loud that you have read them by listing the five skill names and the four core folders. One sentence per item, no longer.

Step 3. Then ask me one question, only this question, in this exact form:

> "What is the single most annoying, recurring thing you do every week that you wish a system handled? Be specific. Tell me the actual thing, not the category."

Wait for my answer. Do not suggest examples until I have answered.

Step 4. Once I answer, you do these four things in order:

a. Restate the friction in one sentence so I know you understood it. If you got it wrong, I will correct you and we go again.

b. Ask me three to five questions to scope the skill. Examples: what does the input look like (a transcript, a list, a PDF, a paragraph)? What is the output I want (a brief, a table, a draft email, a list)? Where should the output go (chat, a file in `Active/`, an updated `People/` file)? How often do I run this (daily, weekly, after-event)? Are there words or formats I want banned in the output?

c. Draft the new `SKILL.md` in `.claude/skills/[kebab-case-skill-name]/SKILL.md`. Use the same frontmatter format as the five existing skills (title, aliases, status, created, name, description). Show me the draft before saving.

d. Once I approve the draft, save it. Then run the skill once on a real example I provide so I can see it work.

Step 5. After the skill runs, give me four things in one short message:

- Whether the output is what I expected (and what to tweak if not)
- Where I can edit the skill if I want to change the trigger phrases or the output format
- The session-close phrase: "When you are done with any session, type 'wrap up' or 'update the docs.' I will save what matters to People files and notes before you close, so the context carries to next time. The kit compounds when you close out cleanly."
- One next thing I might want to do, including a suggested second skill mapped to my role (for an insurance advisor: usually `pipeline-pulse` populated with a real client list; for a mortgage broker: usually `weekly-capture` run against this week's notes; for a real estate agent: usually `document-generator` on a real listing intake. Pick whichever fits what I told you about my work).

Then stop. Do not chain into a second build. The first session is one skill plus orientation. That is the entire goal.

A few rules for the rest of this session:

- No em dashes. No double dashes. They read as AI-generated.
- Direct answers, no preamble, no "Great question."
- Confirm before writing or overwriting any file.
- If something I say is unclear, ask one question. Not three.
- If you are about to do something that takes longer than a minute to undo, pause and say so first.

When you are ready, start with Step 1.
