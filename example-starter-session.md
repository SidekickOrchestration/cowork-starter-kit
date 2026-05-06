---
title: Example Starter Session
aliases: [example session, first session example, starter example, sample session]
status: active
created: 2026-05-05
---

# Example Starter Session

What a first session looks like, end to end. The example operator is Pat Kelly, an independent insurance advisor in Calgary AB. Pat just downloaded the kit, unzipped it, opened the folder in Cowork, and pasted `bootstrap.md`.

Pat's annoying weekly thing: chasing the right carrier underwriter contact when a quote is delayed.

This is one possible first session. Yours will look different.

---

**Pat (paste from `bootstrap.md`):**
I just set up the Cowork Starter Kit in this folder and opened it in Cowork. This is my first session. Walk me through the setup. [...full bootstrap prompt...]

**Claude:**
Reading the kit now.

I have read README, CLAUDE.md, the skills convention, and all five SKILL.md files. Here is what I have:

Skills loaded:
1. `after-meeting-brief` - voice notes or scratch in, structured client follow-up out
2. `product-comparison` - two or three carrier or product PDFs in, side-by-side comparison out
3. `pipeline-pulse` - client list with last-contact dates in, who needs attention this week out
4. `document-generator` - meeting notes plus a document type in, first-draft document out
5. `weekly-capture` - the week's notes in, Friday distill out

Folders loaded: `Reference/`, `Active/`, `People/`, `TO DELETE/`. Skills under `.claude/skills/`.

Now my question for you:

> "What is the single most annoying, recurring thing you do every week that you wish a system handled? Be specific. Tell me the actual thing, not the category."

**Pat:**
Chasing the right underwriter contact when a quote is delayed. I email the carrier broker portal, no response. I email the underwriter I think it is, no response. I look through my old email for who I worked with last time. I forget which carrier uses which contact convention. By the time I find the right person, the client has been waiting 4 days and I look slow.

**Claude:**
Got it. The friction: when a quote stalls at a carrier, you spend 30 to 60 minutes hunting for the right underwriter contact, and that hunt happens once or twice a week.

Five questions to scope the skill:

1. What is the input? A carrier name plus a vague memory ("Sun Life small group"), or do you usually have an old email thread to point me at?
2. What is the output? A name plus email plus phone, or a full contact card with last-known-good date and a recommended message to send?
3. Where should the output go? Just in chat, or saved to `Reference/Carrier_Contacts.md` so it builds up over time?
4. How often does this come up? Once a week, twice a week, more?
5. Are there words or formats you want banned in the output? Anything that drives you nuts?

**Pat:**
1. Sometimes a carrier name plus a product line ("Sun Life dental and EHC small group"). Sometimes I have an email thread but the contact is wrong.
2. Full contact card. Name, role, email, phone if I have it, last-known-good date, and a one-line recommended message I can paste into a follow-up email.
3. Save to `Reference/Carrier_Contacts.md`. I want this to compound.
4. Twice a week, sometimes three times.
5. Do not invent contacts. If the file does not have a contact for a carrier and product line, say so. I would rather know I do not have it than chase a wrong contact.

**Claude:**
Drafting the skill. Path: `.claude/skills/carrier-contact-finder/SKILL.md`. Showing the draft before saving.

```markdown
---
title: Carrier Contact Finder
aliases: [carrier contact, underwriter contact, find the underwriter, who do I email]
status: active
created: 2026-05-05
name: carrier-contact-finder
description: Surface the right carrier underwriter or service contact from Reference/Carrier_Contacts.md given a carrier name and product line. Use when the operator says "who do I email at [carrier]," "carrier contact for [carrier] [product]," "find the underwriter," or pastes a stalled email thread asking for a routing recommendation. Produces a full contact card (name, role, email, phone, last-known-good date) plus a one-line recommended follow-up message. If no contact exists in the reference file for the carrier-and-product combination, says so explicitly and offers to add a placeholder entry rather than inventing one.
---

# Carrier Contact Finder

[full skill body]
```

The skill reads `Reference/Carrier_Contacts.md` (which we will create), parses the entries, returns the matching contact, and falls back to "no contact on file" if nothing matches. Recommended message style is locked to your voice: short, direct, specific to the file in question.

Approve the draft and I will save it. Or tell me what to change first.

**Pat:**
Looks right. Save it. And start `Reference/Carrier_Contacts.md` empty so I can populate it over time.

**Claude:**
Saved `.claude/skills/carrier-contact-finder/SKILL.md`. Created `Reference/Carrier_Contacts.md` with a header and an empty template entry showing the format you should use.

Want to add your first carrier contact now? Drop the carrier name, product line, contact's name and email, and the date you last spoke. I will add the entry and run the skill once so you see the output shape.

**Pat:**
Sun Life. Group dental and EHC small group (under 25 lives). Underwriter is Marcy Tran, marcy.tran@sunlife.com, last spoke 2026-04-22.

**Claude:**
Added. Running the skill now with input "who do I email at Sun Life for small group dental and EHC."

```
## Carrier Contact

**Carrier:** Sun Life
**Product line:** Group dental and EHC, small group (under 25 lives)
**Contact:** Marcy Tran, Underwriter
**Email:** marcy.tran@sunlife.com
**Phone:** [not on file]
**Last known good:** 2026-04-22 (12 days ago)

## Recommended follow-up message
Hi Marcy, following up on the [client name] quote we were working on. Has anything come back from underwriting? Happy to resend the application if it got buried.
```

Three notes:

- The output is what you wanted. You can tweak the recommended-message style by editing `.claude/skills/carrier-contact-finder/SKILL.md` and changing the message template section. The trigger phrases are in the description field; add more if you want it to fire on different language.
- One next thing you might want to do: add 2 or 3 more carriers right now while the format is fresh, so the file is populated for next Tuesday.

That is the first session. Stopping here.

---

That session took Pat 18 minutes from download to first useful output.

The skill now fires on natural language for the rest of Pat's working life. Every time Pat adds a contact to `Reference/Carrier_Contacts.md`, the skill gets sharper. By month two, Pat has 14 carriers populated and the lookup that used to take 45 minutes takes 30 seconds.

The pattern generalizes. Look at the work that drains 30 to 60 minutes a week and is mechanical, not judgment. Build a skill for it. Run the skill. The compounding starts immediately.
