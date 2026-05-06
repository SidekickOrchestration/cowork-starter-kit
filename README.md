---
title: Cowork Starter Kit
aliases: [starter kit, cowork-starter-kit, DIY Cowork, Sidekick starter kit]
status: active
created: 2026-05-05
---

# Cowork Starter Kit

A free, opinionated setup for getting useful work out of Claude Cowork in your first session. Maintained by [Sidekick Orchestration](https://sidekickorchestration.ai).

If you finished the [Independent Advisor Playbook](https://sidekickorchestration.ai) (or any of our DIY pieces) and want the file-system version that compounds across sessions, this is the next step.

---

## What this is

Three things, packaged together so you do not have to figure out the order yourself:

1. **A `CLAUDE.md` template** that tells Claude how you work, your tone, your file safety rules, and a session-start protocol. You edit it once. Every session after that loads the same context, no setup tax.
2. **A folder scaffold** (`Reference/`, `Active/`, `People/`, `TO DELETE/`) so Claude has somewhere to put things and somewhere to look for things. The folders mean Claude can answer "what did I tell that client last September" because the context is stored, not memorized.
3. **Five installable skills** under `.claude/skills/` that fire on natural language and produce structured outputs for the recurring work most independent advisors do: after-meeting briefs, product comparisons, pipeline reviews, document drafts, and a weekly distill.

Apache-2.0 licensed. Free to use, edit, and keep.

---

## Who this is for

Independent operators who run their own book of work. Insurance, mortgage, real estate, financial advisory, fractional consulting, agency-of-one. The examples inside lean toward independent insurance advisors because that is where the kit was first tested, but the prompts and the structure work for any practice where the operator owns the client relationship and produces documents for clients.

If you are part of a captive structure where someone else owns the CRM, the carrier panel, and the client paperwork, this kit will not fit. The shape assumes you are the one running the practice.

---

## Five-minute quickstart

You need: a Claude account with Cowork access, and a folder on your Mac where you want the kit to live. No terminal, no command line, no git.

**1. Download the kit.**

Go to [github.com/SidekickOrchestration/cowork-starter-kit/releases/latest](https://github.com/SidekickOrchestration/cowork-starter-kit/releases/latest) and click the link labeled "Source code (zip)" to download. Unzip the file. You will get a folder called something like `cowork-starter-kit-v0.1.0`.

Rename the folder to whatever you want your practice folder to be called (for example, `my-practice`). Move it wherever on your Mac you want it to live (`Documents/`, `Desktop/`, anywhere).

**2. Open the folder in Cowork.**

In the Claude desktop app, switch to Cowork mode and select the folder you just renamed. Cowork now has read and write access to the kit, your `CLAUDE.md`, and your skills.

**3. Open `Getting_Started.pdf` and follow the steps inside.**

The PDF is the human entry point. It walks you through opening the folder in Cowork, copying one prompt into your first message, and answering the question Claude asks. It also has a one-page reference of the most useful phrases you will say to Claude in your first month, plus a short "what goes where" section so you do not have to second-guess your filing.

If you prefer text over PDF, the same prompt also lives in `bootstrap.md`. Either path works.

That is it. You are running.

### Where does my data live?

Everything in the kit stays on your Mac, in the folder you picked. The kit itself does not transmit any data anywhere. The only network activity is Cowork's normal behavior: when you chat with Claude, your messages and the file contents Claude needs to read travel to Anthropic. That is true of any Claude usage, not specific to the kit. No data goes to GitHub, no data goes to Sidekick.

If your practice has regulatory privacy obligations (PIPEDA, HIPAA, similar), this is the same exposure profile as using Claude.ai directly. Talk to your compliance contact if you have not already cleared Claude for client data.

---

## What is in the box

```
cowork-starter-kit/
├── Getting_Started.pdf                    the human entry point, open this first
├── README.md                              this file
├── LICENSE                                Apache 2.0
├── .gitignore                             standard ignores plus TO DELETE/*
├── CLAUDE.md                              the practice template, edit once
├── INDEX.md                               concept-to-file lookup
├── bootstrap.md                           paste-into-Cowork first prompt (text version)
├── example-starter-session.md             what a first session looks like
├── CONTRIBUTING.md                        for developers and contributors only
├── Reference/                             stable docs you write once and refer to often
│   └── Example_ICP.md.example             template for your own ICP file
├── Active/                                in-progress work, drafts, build trackers
├── People/                                one file per client or contact
│   └── Example_Client.md.example          template for your own client files
├── TO DELETE/                             instead of deleting, you move here
└── .claude/
    └── skills/
        ├── after-meeting-brief/           voice notes in, structured follow-up out
        ├── product-comparison/            two or three product PDFs in, side-by-side comparison out
        ├── pipeline-pulse/                client list in, who needs attention this week out
        ├── document-generator/            meeting notes in, first-draft document out
        └── weekly-capture/                week's notes in, Friday distill out
```

Example files end in `.example` so you can see the format without Claude treating them as your real ICP or your real client. Copy them, rename, edit, then delete the `.example` version.

The folders are the part that compounds. You can add `Meetings/`, `Operations/`, or whatever your practice needs as you go. The starter set is deliberately minimal so you do not spend day one rearranging folders.

---

## How the skills work

Cowork auto-loads any skill in `.claude/skills/` the moment you open the folder. You do not have to install or activate them. To verify, ask Claude "what skills do you have loaded" and the five kit skills should be in the list.

Each skill is a `SKILL.md` file with a description that fires on natural-language phrases. You do not have to remember a command. You say:

> "Here are my notes from the call with Jen. Run an after-meeting brief."

Claude detects the trigger, loads the skill, and produces the structured output. The prompts inside the skills are the same prompts you have in the [Independent Advisor Playbook](https://sidekickorchestration.ai) PDF, but installed once instead of pasted every time. When you close the chat and come back tomorrow, the skill is still there.

To customize a skill, open its `SKILL.md` and edit the body. Change the example vertical, change the output format, change the fields you want surfaced. The frontmatter at the top stays as-is so the trigger still fires.

---

## The CLAUDE.md template

`CLAUDE.md` at the repo root is the file Claude reads first every session. It tells Claude how you work: your tone, your output rules, your file safety rules, and what to do at session start.

The template ships with sensible defaults. The sections marked `# CUSTOMIZE` are the ones you should edit on day one. The rest you can leave alone until you have a reason to change them.

Examples of what to customize:
- Your name and your role (top of the file)
- Your output rules (what tone do you want Claude to use, what to avoid)
- Your file safety rules (the defaults are conservative; loosen them only if you understand the trade)
- Your session-start protocol (which files Claude should always read at the top of a session)

The defaults work. Change them when something bothers you, not preemptively.

---

## When the DIY version runs out of road

The kit is the methodology. If you want a setup that fits exactly how your practice runs, with skills tuned to your specific clients, products, and workflows, that is what [Sidekick Solo](https://sidekickorchestration.ai) is. We do the setup, you keep the implementation. One engagement, one fixed price, no monthly tax.

If you are happy with the DIY path, ignore the offer. The kit is free to use, edit, and keep.

---

## For developers and contributors

If you want to fork the kit, customize it for your team, or contribute changes back, the git workflow is the right path:

```bash
cd ~/Documents
git clone https://github.com/SidekickOrchestration/cowork-starter-kit.git my-practice
cd my-practice
```

Open the folder in Cowork the same way as the .zip path. See [CONTRIBUTING.md](CONTRIBUTING.md) for the contribution model and the kinds of changes most likely to land.

---

## License and attribution

Apache License 2.0. See [LICENSE](LICENSE) for the full text.

You are free to use this kit commercially, modify it, distribute it, and run it without giving anything back. Attribution is appreciated but not required. If you build something on top of the kit and want to credit Sidekick, link to [sidekickorchestration.ai](https://sidekickorchestration.ai).

The kit is maintained by Sidekick Orchestration Ltd. (Vancouver, BC). Questions, feedback, or "this broke and I cannot figure out why" go to [chase@sidekickorchestration.ai](mailto:chase@sidekickorchestration.ai).
