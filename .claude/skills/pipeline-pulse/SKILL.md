---
title: Pipeline Pulse
aliases: [pipeline pulse, pipeline review, who needs attention, pipeline check]
status: active
created: 2026-05-05
name: pipeline-pulse
description: Surface which clients and prospects need attention this week, given a list of active conversations with last-contact dates and current stage. Use when the operator says "pipeline pulse," "who needs attention," "pipeline review," "who is going cold," "Monday pipeline check," or pastes a client list with stages and last-touch dates. Produces four buckets (going cold, at decision, recently active, surprise list) with a specific suggested next move for each name in the first two.
---

# Pipeline Pulse

Run this Monday morning, or whenever the "I am missing someone" twinge hits.

## When this skill fires

The operator pastes a client list, prospect list, or HubSpot export with last-contact dates and current stage. Trigger phrases include "pipeline pulse," "who needs attention," "pipeline review," "who is going cold," "Monday check," or any clear signal that the operator wants the active book scanned for what is moving, what is stuck, and what they might be missing.

## What this skill produces

```
## Going cold
Clients and prospects with no contact in 3+ weeks who were active. One line per client with the suggested next move.
- [Client name] - [Last contact date] - [What stage]. Suggested message: [specific suggested message, not "follow up"].
- [Repeat]

## At decision
Clients with a quote, proposal, application, or pending choice in front of them. One line per client.
- [Client name] - [What decision is owed] - [How long it has been pending]. Suggested next move: [specific].
- [Repeat]

## Recently active, no action needed
One line per client just to confirm.

## Surprise list
Anything in the data that is worth surfacing: clients you might have forgotten, gaps in the notes, patterns across the list.
- [Pattern or client]: [why it matters]
- [Repeat]
```

## Rules for this skill

- "Going cold": specific suggested message per client, not generic "send a check-in." If the operator has not contacted Linda in 6 weeks and the last note said "waiting on her benefits enrollment date," the suggested message should be "Hi Linda, circling back on the enrollment date - any movement?" Not "follow up."
- "At decision": name the actual decision the client owes, not a generic "follow up on quote." If the client has a Sun Life vs Canada Life proposal in front of them, write "Owes a carrier choice on the Aug 15 renewal."
- "Surprise list": at least one entry, even if it is a pattern observation. Look across the list for things the operator would not see staring at the same data themselves: three clients in the same industry, two clients in the same building, four clients with the same renewal month, anything.
- Do not invent contact history. If the input does not show a stage or a last-contact date for a client, list the client under "Surprise list" with note "incomplete data, worth verifying."
- Read every `People/[Name].md` referenced in the input list if the file exists. The People file usually has context the bare list does not.

## Example flavor (insurance advisor)

Input: 22 active prospects and clients, mix of group benefits and life, last-contact dates ranging from yesterday to 9 weeks ago.

Output:
- Going cold: 3 clients with 4-6 week gaps. For each, a specific suggested message based on the last topic of conversation.
- At decision: 2 clients with proposals out, both 10 days past the verbal "I will get back to you by Tuesday" mark. Suggested next move for each: a specific question that respects the time without re-pitching.
- Recently active: 11 clients confirmed.
- Surprise list: "Three group benefits clients all have an Aug 15 renewal. Worth a single calendar block on Aug 1 to do all three quote refreshes at once."

## Example flavor (mortgage broker)

Input: 14 active files, mix of approvals, awaiting documents, and post-funding follow-ups.

Output:
- Going cold: 2 files where conditional approval is pending and the client has not sent T4s in 3 weeks.
- At decision: 1 client comparing a 3-year and 5-year fixed, has the comparison in hand for 8 days.
- Recently active: 9 files moving normally.
- Surprise list: "Four files all have closings in the same week of June. Worth checking lender funding capacity early."

## What good output looks like

"Going cold" lists three to five names with a specific suggested message for each, not a generic "send a check-in." "At decision" names the actual decision the client owes. The "Surprise list" catches at least one pattern the operator would have missed staring at the same data.
