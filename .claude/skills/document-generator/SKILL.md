---
title: Document Generator
aliases: [document generator, draft generator, draft this document, first draft]
status: active
created: 2026-05-05
name: document-generator
description: Produce a first-draft document (proposal cover letter, quote summary, renewal letter, follow-up email, summary letter, etc.) from meeting notes plus a stated document type. Use when the operator pastes meeting notes and names a document type ("proposal cover letter," "renewal letter," "summary email"), or says "draft this," "document generator," "first draft of [doc]," "I need a draft proposal." Produces a copy-and-edit-ready draft, plus a list of blanks to fill in and places to double-check.
---

# Document Generator

Run this when you owe a client a document and you do not want to start from a blank page.

## When this skill fires

The operator pastes meeting notes (or references existing notes in `Active/` or `People/[Name].md`) and names a document type. Trigger phrases include "draft this," "document generator," "first draft of [document]," "I need a [proposal / cover letter / renewal letter / summary email] for [client]," or any clear signal that meeting context is being handed over with a specific output document requested.

## What this skill produces

```
[The draft document, ready to copy and edit.]

---

## Blanks to fill in
- [Each placeholder you left, with context: "[exact premium amount]," "[client's effective date]"]

## Double-check before sending
- [Each place where the language might need to change based on something the operator said but did not write]
```

## Rules for this skill

- Match the tone of the meeting notes. If the operator's notes are formal, the draft is formal. If conversational, conversational.
- Use the client's real name and the specific products, services, or addresses discussed.
- No jargon unless the client used it first. "AD&D rider" stays only if the operator's notes contain "AD&D rider" or the client used it.
- Include only what was discussed. Do not invent product details, dollar amounts, dates, or commitments the operator did not make.
- End with a single clear next step: a date, a meeting, or a decision the client owes the operator. Not "let me know if you have any questions."
- The "Blanks to fill in" list should be honest. If a number or date was not in the input, it goes in this list. If everything is filled in from the input, the list says "None."

## Example flavor (insurance advisor)

Input: meeting notes from a group benefits renewal call with HealthFirst plus the document type "proposal cover letter."

Output: a one-page cover letter referencing HealthFirst by name, the August 15 renewal, the 18 employees, the Sun Life vs Canada Life comparison the operator promised, and a closing line "I will send the comparison spreadsheet Friday afternoon. Let us schedule a 30-minute review the following Tuesday." Blanks list: "[exact Sun Life premium quote], [exact Canada Life premium quote]." Double-check list: "the call notes mention 'they want EHC paramedical raised' but do not specify the new cap; confirm before drafting the comparison."

## Example flavor (mortgage broker)

Input: discovery call notes for a refinance plus the document type "summary email."

Output: a short email recapping the goal (consolidate $40K credit-card debt into the mortgage), the property value, the current rate, the lenders being approached, and the next step ("I will have rate options to you by Wednesday"). Blanks list: "[exact appraised value], [exact existing balance]." Double-check list: "the client mentioned a co-signer might be available; confirm whether to include co-signer scenarios in the rate options."

## Example flavor (real estate agent)

Input: listing intake notes plus the document type "listing presentation summary."

Output: a structured one-pager covering the recommended list price, the comparables used, the marketing plan, the commission structure, and the timeline. Blanks list: "[final list price recommendation, awaiting CMA finalization]." Double-check list: "the seller mentioned wanting a 60-day closing; verify the marketing timeline still works at that pace."

## What good output looks like

A draft that uses the client's name, the real product or property, and a real next step (a date or a decision). The blanks list is honest about what got skipped. If the draft hallucinates a number the operator did not say, the input was thin: ask for fuller notes and run again.
