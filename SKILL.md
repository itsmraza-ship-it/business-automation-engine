---
name: business-automation-engine
description: A map-first system for automating a startup's core pipeline — lead capture, CRM, proposals, invoicing, delivery, follow-up, and email — without automating away trust or control. Use when designing, auditing, or rolling out a business workflow or email automation.
---

# Business Automation Engine — Skill

Automation does not fix a broken process; it runs the broken process
faster. This skill enforces the repo's order: map the process on one page
first, then automate only the steps that are safe to automate.

## What it covers

- The core pipeline: Lead Capture → CRM → Proposal → Invoicing →
  Delivery → Follow-up → Review / Referral — breaks happen *between*
  stages, and closing those gaps is automation's real job
- `workflow-maps.md` — five step-by-step maps (New Lead, Client
  Onboarding, Invoice + Reminder Ladder, Content Publishing, Support
  Triage) tagged `[AUTO]` / `[HUMAN]` / `[CHECK]`
- `email-automation.md` — cold-vs-warm separation, welcome sequence,
  follow-up cadence, per-mailbox volume discipline, suppression lists,
  human sign-off before campaigns
- `automate-first.md` — what to automate first, what to never automate,
  a 5-question test for any candidate, and a 30-day rollout order
- Tool stack by category (automation platform, CRM, forms, scheduling,
  invoicing, email, documents, tasks, support) — category first, brand
  second; fewer tools fully used beats many half-configured

## How to apply it — the method

1. **Map before you automate.** Write the process as it actually happens:
   steps, owner, input, output, and the points where a human must decide,
   approve, or speak to a customer. If it does not fit on one page, it is
   not understood well enough to automate.
2. **Run the 5-question test** on every candidate step: repetitive?
   rule-based (no "use your judgement")? low-cost and reversible if wrong?
   logged? inside every platform/provider limit with margin? Fail on
   questions 2, 3, or 5 → it stays human (automation may draft or route).
3. **Automate the plumbing first.** Data entry and record creation,
   reminders, status notifications, internal alerts, template generation,
   file organisation, meeting plumbing. Prove each one before expanding.
4. **Keep one source of truth.** Every contact, deal, and invoice lives in
   one CRM/system of record; automations read from it and write back to
   it. Every automation has an owner, an off-switch, and a log.
5. **Roll out in the 30-day order.** Week 1: CRM foundation + New Lead
   map. Week 2: acknowledgement + follow-up discipline + suppression list.
   Week 3: invoice ladder + onboarding. Week 4: support triage + content
   pipeline tracker + weekly automation review. One workflow at a time.

## Never automate — hard lines

- Final client answers on sensitive matters (legal, tax, financial,
  compliance, complaints, disputes)
- Refunds, credits, discounts, price/term changes, contract approvals
- Public posts, ads, or announcements without human review — automation
  drafts and queues; humans publish
- Anything that can spam or ban-risk an account: bulk posting/messaging,
  automated engagement, cold-blasting purchased lists, exceeding limits
- Deleting records or closing a complaint as "resolved" unconfirmed

## Email rules — apply exactly

- Warm (clients, opted-in leads, subscribers, community) and cold
  (never-heard-of-you) **never mix**: separate lists, separate sending
  streams/domains, so an outreach problem cannot take down client mail.
  A person becomes warm only by opting in.
- Welcome sequence: deliver the promise immediately, then story, best
  content, reframed problem, soft offer — one idea and one CTA per email,
  and the sequence ends.
- Follow-ups stop the moment a human replies, books, buys, or
  unsubscribes. Payment problems pause the ladder and become a
  conversation.
- Volume: warm up gradually, respect hard per-mailbox daily/hourly caps,
  keep sending consistent, authenticate SPF/DKIM/DMARC, seed-test every
  new template (spam verdict = fix and retest, never send anyway).
- One master suppression list, checked at import and before every send.
  A human signs off every campaign against the repo's checklist.

## How to apply this when helping a user

- Start from their actual workflow, not a tool recommendation. Ask what
  happens today, step by step, then map it with `[AUTO]`/`[HUMAN]` tags.
- Recommend categories before brands, and name the source of truth for
  contacts, money, and tasks explicitly.
- Flag any plan that crosses the Never Automate lines and redesign it as
  draft-and-approve instead.

---
epicsdeals.com — free tools by Epics Deals; US LLC formation from $130 + state fee.
