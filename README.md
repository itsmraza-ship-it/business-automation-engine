# Business Automation Engine

The business automation engine for startups — a practical system for automating the repetitive work in your business without automating away trust, judgement, or control.

Automation does not fix a broken process. It just runs the broken process faster. So this engine starts somewhere unfashionable: **map the process before you automate it.**

## Map First, Automate Second

Before any tool is connected:

1. Write the process down, step by step, as it actually happens today — not as you wish it happened.
2. Name the owner of each step, the input it needs, and the output it produces.
3. Mark the steps where a human must decide, approve, or speak to a customer.
4. Only then decide what software should do — and what it must never do.

If you cannot draw the workflow on one page, you do not understand it well enough to automate it. See [workflow-maps.md](workflow-maps.md) for ready-made maps of the five core workflows.

## The Core Pipeline

Most service and product startups run on the same backbone:

```
Lead Capture -> CRM -> Proposal -> Invoicing -> Delivery -> Follow-up -> Review / Referral
```

| Stage | What happens | What automation can do |
|---|---|---|
| **Lead capture** | A prospect finds you and raises a hand — form, booking page, referral, inbox | Create the CRM record instantly, tag the source, send an acknowledgement, alert the team |
| **CRM** | Every contact, conversation, and deal in one place, with a clear stage | Move deals by trigger, assign owners, set follow-up tasks automatically — one source of truth |
| **Proposal** | The prospect gets a clear offer: scope, price, timeline, next step | Generate the proposal from a template + CRM data; notify you when it is viewed / signed |
| **Invoicing** | Invoice sent, payment tracked, reminders if it slips | Issue invoices on signature / milestone, track status, run the reminder ladder (see `workflow-maps.md`) |
| **Delivery** | The work itself — onboarding, production, service, fulfilment | Kick off onboarding tasks, collect intake information, send status notifications |
| **Follow-up** | After delivery: check in, resolve loose ends, stay present | Schedule check-ins, send delivery confirmations, trigger review requests at the right moment |
| **Review / Referral** | A happy client becomes proof and pipeline | Request the review, log the testimonial, ask for the referral — and record all of it in the CRM |

Breaks in a business usually happen *between* stages — a lead nobody followed up, an invoice nobody chased, a delivered client nobody asked for a review. Automation's real job is to close those gaps.

## Tool Stack Categories

You do not need a specific brand. You need each category covered, with tools that connect to each other. Mainstream examples are given so you know what class of tool to look for — pick the one that fits your budget, region, and existing stack.

| Category | Job | Mainstream examples |
|---|---|---|
| Automation platform | Connects your tools and moves data between them on triggers | Make, Zapier |
| CRM | One source of truth for contacts, deals, and pipeline stages | HubSpot, Pipedrive, Zoho CRM, Airtable (lightweight) |
| Forms & intake | Lead capture, client onboarding questionnaires, requests | Typeform, Tally, Google Forms |
| Scheduling | Booking calls without email ping-pong | Calendly, Cal.com |
| Invoicing & payments | Invoices, payment links, receipts, payment tracking | Stripe, QuickBooks, Xero, Wave |
| Email | Transactional messages, sequences, campaigns | Your email platform + a separate stream/domain for outreach — see `email-automation.md` |
| Documents & e-sign | Proposals, contracts, agreements | PandaDoc, Notion / Google Docs + an e-sign tool |
| Project / task management | Delivery work, owners, deadlines | Notion, Asana, ClickUp, Trello |
| Support | Ticket intake, triage, replies | Help Scout, Zendesk, Intercom — or a well-run shared inbox at small scale |
| Internal comms | Alerts and hand-offs where the team actually looks | Slack, Microsoft Teams, email |

Rules for the stack:
- **Fewer tools, fully used** beats many tools, half-configured.
- Every tool must connect to the CRM or the automation platform — isolated tools create manual copy-paste, which is the thing you are trying to eliminate.
- Document which tool is the source of truth for each kind of data (contacts, money, tasks). Two "truths" is zero truths.

## Golden Rules

1. **Human approval on anything public or financial.** Posts, campaigns, refunds, discounts, price changes, and anything a customer reads as a commitment — a human approves it first. Automation drafts and queues; humans decide.
2. **One source of truth.** Every contact, deal, and invoice lives in one system of record. Automations read from it and write back to it — they never keep private copies.
3. **Log everything.** Every automated action leaves a trace: what ran, when, on which record, and what it sent or changed. If you cannot see what the automation did, you cannot trust it or debug it.
4. **Map before you automate.** No workflow gets built until it exists on paper (see above).
5. **Start boring.** Automate data entry, reminders, notifications, and alerts first — the work that is repetitive and low-risk. See [automate-first.md](automate-first.md).
6. **Every automation has an owner and an off-switch.** Someone checks it regularly, and anyone can pause it when it behaves badly.
7. **Never automate a ban risk.** Anything that could spam a platform, blast a list, or get an account restricted does not get automated. Ever.

## Repository Contents

- `README.md` — this overview: pipeline, stack categories, golden rules
- `workflow-maps.md` — step-by-step maps for new leads, client onboarding, invoicing + reminders, content publishing, and support triage
- `email-automation.md` — welcome sequences, follow-up cadence, cold-vs-warm separation, volume discipline, and sign-off rules
- `automate-first.md` — what to automate first, what to never automate, and a 30-day rollout order
- `LICENSE` — MIT License

## License

MIT — see [LICENSE](LICENSE).

## Join the Epic Founder's Club
Building a company alone is slow. The Epic Founder's Club is Epics Deals' free Discord community for founders — live sessions, Q&As and founders helping founders go global.
Join free: https://discord.gg/RbmHw9YNYg

---
**Free tools by Epics Deals** — [epicsdeals.com](https://epicsdeals.com) · *Your Partner in Global Expansion*
US LLC formation from **$130 + state fee** · EIN · ITIN · US tax filing · compliance
Part of the [Nonresident Founder Toolkit](https://github.com/itsmraza-ship-it/nonresident-founder-toolkit)
