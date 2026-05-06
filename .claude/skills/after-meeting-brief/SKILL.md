---
title: After-Meeting Brief
aliases: [after-meeting brief, meeting brief, post-call brief, follow-up brief]
status: active
created: 2026-05-05
name: after-meeting-brief
description: Turn raw meeting notes (voice memo transcript, scratch notes, dictation) into a structured client follow-up. Use when the operator pastes meeting notes, says "after-meeting brief," "follow-up brief from this," "structure these notes," "post-call brief," "I just got off a call with [name]," or shares a transcript and wants it processed. Produces a labeled brief with attendees, what was discussed, commitments on both sides, open questions, and a draft follow-up email in the operator's voice.
---

# After-Meeting Brief

Run this after every client call, ideally within 30 minutes of hanging up.

## When this skill fires

The operator pastes meeting notes, voice memo transcript, or dictated scratch notes from a client conversation. Trigger phrases include "after-meeting brief," "structure these notes," "follow-up brief," "post-call brief," "I just got off a call with [name]," or any clear signal that meeting content has been pasted and needs structuring. If a client name is mentioned and a `People/[Name].md` file exists, read that file first for context before producing the brief.

## What this skill produces

A structured follow-up in this exact format:

```
## Client name and meeting date
[Pull from the notes; ask if not present]

## What was discussed
- [3 bullets, each one sentence, using the operator's words]

## What I committed to
- [Each as a task, with target date if named]

## What the client committed to
- [Each as a task, with target date if named]

## Open questions
- [Anything that did not get resolved; do not guess]

## Draft follow-up email
[One paragraph in the operator's voice, conversational, no jargon. Sign off with the next concrete step.]
```

## Rules for this skill

- Use the operator's words, not generic insurance / mortgage / real-estate / financial-advisor language. If the operator said "the AD&D rider," do not generalize to "the additional coverage."
- If the operator named a carrier, product, dollar amount, or date, include it exactly as stated.
- If something is unclear, list it under Open Questions instead of guessing.
- The follow-up email should read like the operator wrote it on a Tuesday afternoon, not like a template. No "I hope this email finds you well." No "I trust this finds you in good health."
- After producing the brief, ask whether to update `People/[Name].md` with the new context. Do not auto-update.

## Example flavor (insurance advisor)

Input: "Met with Marcy at HealthFirst Group Benefits. She wants to compare Sun Life vs Canada Life for her 18-employee dental and EHC. Owner pays 80%. Renewal Aug 15. She is leaning Sun Life because of claims experience but wants to see numbers. Action: I send comparison by Friday. She sends current premium spreadsheet by Wednesday."

Output: full brief with the dates, the 80% split, the carrier names, the Aug 15 renewal, both commitments noted, and a follow-up email confirming the Friday comparison and asking for the spreadsheet.

## Example flavor (mortgage broker)

Input: "Call with Jordan Park. First-time buyer, looking at $720K range in East Vancouver, 5% down. Pre-approval needs to be in by next Tuesday for the open house Sunday. Two lenders to compare: Scotiabank, MCAP. Action: I run rate comparison by Monday morning. He sends T4s and last 90 days of bank statements."

Output: full brief noting the price range, the down payment, the deadline, both lenders, and an email confirming the rate comparison by Monday and listing what the broker needs from the client.

## What good output looks like

Specific names, exact dollar amounts the operator mentioned, dates if they said them out loud. The follow-up email reads like a real Tuesday email. If the output sounds like a template, the input was thin: ask the operator for three more minutes of context and run again.
