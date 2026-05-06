---
title: Product Comparison
aliases: [product comparison, carrier comparison, side-by-side, options comparison]
status: active
created: 2026-05-05
name: product-comparison
description: Build a side-by-side comparison of two or three products, carriers, lenders, or providers from raw product information. Use when the operator pastes brochure text, PDF excerpts, or scratch notes about multiple options and says "compare these," "side-by-side," "product comparison," "carrier comparison," "which one fits this client," or shares two or more sources of product information. Produces a one-sentence summary, a comparison table, three short paragraphs on operational reality, a recommendation framed by client priority, and a "Watch out for" line catching one specific gap.
---

# Product Comparison

Run this when a client is choosing between two or three options and you need a side-by-side without spending 90 minutes building it.

## When this skill fires

The operator pastes product information from two or more sources and asks for a comparison. Trigger phrases include "compare these," "side-by-side," "product comparison," "carrier comparison" (insurance), "lender comparison" (mortgage), "brokerage comparison" (real estate), "fund comparison" (financial advisory), or "which one fits [client]." The skill works for any vertical where the operator is choosing between two or three providers for a client.

## What this skill produces

```
## Summary
[One sentence: which option fits which client profile]

## Side-by-side comparison
| Field | Option A | Option B | Option C (if applicable) |
|-------|----------|----------|---------------------------|
| [columns the client cares about: premium / rate / fee, coverage / amount / term, exclusions / conditions, riders / features, claims / service, anything material]

## Operational reality
**Option A:** [Two or three sentences on what using this product is actually like: claims experience, support quality, renewal patterns, friction points.]
**Option B:** [Same.]
**Option C:** [Same, if applicable.]

## Recommendation
If the client's priority is [X], go with [Option]. If the client's priority is [Y], go with [Option].

## Watch out for
[One specific exclusion, fee, condition, or fine-print item that the brochure copy buries. Name it in plain language.]
```

## Rules for this skill

- Plain English, not industry jargon. Assume the client knows their own business but does not know provider internals.
- Do not invent numbers. If a premium, rate, or fee is not in the input, write "[not stated in input]" in that cell and ask the operator before publishing.
- The recommendation must name an option, not hedge. "Either could work" is not a recommendation.
- The "Watch out for" line should catch something real. If you cannot find a meaningful gap, write "Nothing material flagged in the inputs" and stop. Do not invent fine-print risk.
- Keep the operational-reality paragraphs to two or three sentences each. Long paragraphs lose the client.

## Example flavor (insurance advisor)

Input: pasted brochure text from Sun Life, Canada Life, and Manulife for an 18-employee group dental and EHC plan.

Output: comparison table covering premium per employee, dental annual maximum, EHC paramedical caps, claims processing time, and renewal pattern. Operational reality paragraphs noting which carriers are stricter on rate increases, which offers easier portal claims, and which has the longest underwriting wait. Recommendation: "If priority is lowest premium year one, Manulife. If priority is claims experience and admin simplicity, Sun Life."

## Example flavor (mortgage broker)

Input: rate sheets and conditions from Scotiabank and MCAP for a first-time buyer at $720K, 5% down.

Output: comparison table covering 5-year fixed rate, prepayment privileges, portability, penalty calculation, and approval timeline. Operational reality paragraphs noting which lender is stricter on conditional approvals, which has faster funding, and which is more flexible on side-business income. Recommendation: "If priority is the lowest rate, MCAP. If priority is fastest unconditional approval before Sunday's open house, Scotiabank."

## Example flavor (real estate agent)

Input: comparable listings or two competing offers on a property.

Output: comparison table covering price, conditions, deposit, closing date, and contingencies. Operational reality paragraphs on each buyer's financing strength and history of closing. Recommendation: "If priority is highest net to seller, Offer A. If priority is certainty of closing on time, Offer B."

## What good output looks like

A table the client can read in 90 seconds. The recommendation paragraph names which option fits which priority, not a hedge. The "Watch out for" line catches one specific exclusion or condition the brochure buries.
