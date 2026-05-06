---
title: Weekly Capture
aliases: [weekly capture, Friday distill, week review, end-of-week distill]
status: active
created: 2026-05-05
name: weekly-capture
description: Distill the week into a Monday-ready brief: what moved, what stalled, what got missed, Monday's first three actions, and one pattern worth filing. Use when the operator says "weekly capture," "Friday distill," "wrap up the week," "end-of-week," "what should I do Monday," or pastes the week's notes / calendar / email summaries. Produces a five-section distill that compounds across weeks when run consistently.
---

# Weekly Capture

Run this Friday afternoon. The prompt that compounds the most when you keep doing it.

## When this skill fires

The operator pastes the week's notes, calendar entries, email summaries, or a mix. Trigger phrases include "weekly capture," "Friday distill," "wrap up the week," "end-of-week," "what should I do Monday," "close out the week," or any clear signal that the operator is doing a weekly review. The skill also fires if the operator simply says "what is going on this week" on a Thursday or Friday, with the expectation that they will paste data.

## What this skill produces

```
## What moved this week
Clients or files where the conversation advanced. One line each with the specific advance.
- [Client/file name] - [What advanced]

## What stalled
Clients or files where you expected movement and did not get it. One line each with what to do next.
- [Client/file name] - [What stalled, suggested next move]

## What got missed
Things you committed to that did not happen. One line each, no judgment.
- [What was committed, who is owed]

## Monday's first three
The three highest-leverage things to start with on Monday morning, in order. Each with a one-sentence reason.
1. [Action] - [Why this is first]
2. [Action] - [Why second]
3. [Action] - [Why third]

## One pattern to notice
One thing across the week worth filing for next week. Could be a client pattern, a workflow friction, a market signal, or a content idea.
- [Pattern, in one paragraph]
```

## Rules for this skill

- Use the operator's words from the input. Do not generalize specific names, dates, or amounts into category language.
- "What stalled" must include a suggested next move per item, not just "follow up." If a renewal proposal has been out for 12 days, the suggested move might be "Call Wednesday morning - email is not landing."
- "Monday's first three" should read like a real list. Not productivity-hack language. Each one names a specific action and a specific reason. If the operator's calendar shows two meetings already booked Monday, those count as "first three" only if they are genuinely the highest-leverage start.
- "One pattern to notice" surfaces something the operator would not see by staring at the same week. Three clients raising the same coverage gap is a pattern. Two clients in the same industry asking similar questions is a pattern. A workflow that took twice as long as expected is a pattern.
- If the input is thin (less than a couple of paragraphs of notes plus calendar), say so. Ask for the calendar export or three more minutes of dictation before producing a thin distill. A thin distill is worse than no distill: it teaches the operator the skill does not work.
- After producing the distill, ask whether to save it to `Active/Weekly_Distill_[date].md`. If the operator says yes, save it there. The compounding effect comes from being able to look back at week three when running week eight.

## Example flavor (insurance advisor)

Input: notes from a 5-day week, mix of client calls, two carrier meetings, and a renewal cycle in flight.

Output:
- What moved: 4 clients advanced (proposal sent, renewal confirmed, claim resolved, intro call booked)
- What stalled: 2 clients (Marcy's spreadsheet still pending, Reza has not booked the call he asked to book)
- What got missed: one commitment to send a Sun Life rider summary by Wednesday
- Monday's first three: send Sun Life rider summary first (already overdue), prep Marcy's renewal comparison since her decision date is Aug 15, return Reza's last call before pinging again
- Pattern to notice: "Three group benefits clients this week all asked about EHC paramedical caps. Worth a quick LinkedIn post on the topic, and worth flagging in the next two carrier meetings."

## Example flavor (mortgage broker)

Input: a week of files, two closings, three discovery calls, and a renewal cycle.

Output:
- What moved: two closings funded, one pre-approval issued, one renewal locked
- What stalled: a co-signer scenario the client said he would talk to his brother about (still no answer)
- What got missed: forgot to send the Tuesday family the lender comparison
- Monday's first three: send the Tuesday family the comparison (overdue), prep for Thursday's first-time-buyer seminar, follow up on the co-signer file
- Pattern to notice: "Four discovery calls this week were all first-time buyers in the 30-35 age range with $700-$800K target prices. Worth tightening the first-time buyer intake for that profile."

## What good output looks like

"Monday's first three" reads like a real list, not a productivity hack. The "One pattern to notice" surfaces something that would not show up by staring at the same week. By week four of running this consistently, the operator is catching pipeline patterns weeks before they would have surfaced on their own.
