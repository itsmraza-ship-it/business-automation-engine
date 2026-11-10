# Workflow Maps

Five core workflows, mapped step by step. Read them as the process first — the automation notes at each step only make sense once the human process is clear.

Legend:
- `[AUTO]` — safe to automate
- `[HUMAN]` — a person decides / approves / communicates
- `[CHECK]` — a decision point that routes the workflow

## 1. New Lead

```
Lead submits form / books a call / is referred
  -> [AUTO] Create CRM record (name, contact, source, date)
  -> [AUTO] Tag source + assign owner by rule (region / service / round-robin)
  -> [AUTO] Send acknowledgement email ("Got it — here's what happens next")
  -> [AUTO] Internal alert to owner (Slack / email / task)
  -> [HUMAN] Owner reviews record and any intake answers
  -> [HUMAN] First personal reply / call — a human opens the relationship
  -> [CHECK] Qualified?
       YES -> [AUTO] Move deal to "Qualified" stage
              -> [HUMAN] Discovery call -> go to Proposal workflow
       NO  -> [CHECK] Not now, or never?
                  NOT NOW -> [AUTO] Set follow-up task on agreed date
                             -> [AUTO] Add to nurture / follow-up cadence (see email-automation.md)
                  NEVER   -> [AUTO] Mark "Closed — not a fit" with reason logged
                             -> [HUMAN] Send a polite closing message (template, human-sent)
  -> [AUTO] Log every touch on the CRM record
```

Key rules:
- Speed matters for the acknowledgement (automated, instant) — and a human still makes the first real contact promptly.
- No lead sits without an owner and a next step. If either is missing, the workflow has failed, not the salesperson.
- Source tagging is non-negotiable: you cannot improve lead generation you cannot attribute.

## 2. New Client Onboarding

```
Proposal signed / payment confirmed
  -> [AUTO] Move deal to "Won — Onboarding" in CRM
  -> [AUTO] Create client folder + project / task list from the onboarding template
  -> [AUTO] Send welcome email (see email-automation.md) with the intake form link
  -> [HUMAN] Kickoff owner reviews scope, flags anything unusual in the deal
  -> Client completes intake form
  -> [AUTO] Save intake answers to the client record; alert delivery owner
  -> [CHECK] Intake complete?
       NO  -> [AUTO] Gentle reminder after a set interval
              -> [HUMAN] Personal nudge if a second reminder is needed
       YES -> [HUMAN] Internal kickoff: confirm deliverables, owner, timeline
              -> [AUTO] Create delivery milestones + status-notification schedule
              -> [HUMAN] Kickoff call / message with the client: timeline + how to reach you
  -> [AUTO] Set follow-up and review-request triggers for after delivery
  -> Delivery begins (see core pipeline in README.md)
```

Key rules:
- Onboarding starts the moment money or signature lands — not when someone "gets around to it".
- One intake form, used for every client of that type. Ad-hoc questions by email are how information gets lost.
- The client should always be able to answer three questions: what happens next, when, and who do I contact?

## 3. Invoice + Payment Reminder Ladder

```
Deliverable / milestone reached (or proposal signed, per your terms)
  -> [HUMAN] Confirm the amount, scope reference, and payment terms are correct
  -> [AUTO] Generate invoice from the CRM / accounting record
  -> [AUTO] Send invoice + payment link; log sent date and due date in CRM
  -> [CHECK] Paid by due date?
       YES -> [AUTO] Mark paid, send receipt + thank-you
              -> [AUTO] Trigger the next stage (delivery step / follow-up)
       NO  -> Reminder ladder runs (each step logged on the record):
              Day +1 past due -> [AUTO] Friendly reminder: invoice details + payment link restated
              Day +7          -> [AUTO] Firmer reminder: amount, due date, "tell us if there's an issue"
              Day +14         -> [HUMAN] Personal message from the account owner — email alone stops here
              Day +21 / +30   -> [HUMAN] Call + decision: pause work per your terms, payment plan, or escalate
  -> [CHECK] Client says there's a problem (dispute / hardship / confusion)?
       YES -> [HUMAN] Automation PAUSES. A human handles the conversation and the resolution.
       NO  -> Ladder continues as above.
```

Key rules:
- A human verifies the first invoice for every client. Automation handles the repeats.
- Reminders restate facts (invoice number, amount, due date, payment link) and always leave a door open: "if something looks wrong, reply and we'll check it".
- Tone escalates slowly and never threatens what your contract does not actually say.
- Payment problems are conversations, not sequences — the ladder exists to start the conversation, not replace it.

## 4. Content Publishing Pipeline

```
Idea captured (research / client question / analytics learning)
  -> [AUTO] Idea logged in the content tracker with topic, format, owner
  -> [HUMAN] Draft created (article / script / post)
  -> [HUMAN] Review: accuracy, claims checked, brand voice, no unapproved promises
  -> [CHECK] Approved?
       NO  -> [HUMAN] Revise -> back to Review
       YES -> [HUMAN] Packaging: title, visual, description / caption, links checked
              -> [HUMAN] Publish — manually, one item at a time, at human pace
              -> [AUTO] Log published URL + date in the tracker
              -> [AUTO] Create repurposing tasks (other formats / platforms, from the same idea)
              -> [AUTO] Schedule the post-publication check (~25 hours) as a task
              -> [HUMAN] Review performance at the check; rescue (title/visual) or double down (follow-up piece)
```

Key rules:
- **Nothing public publishes without human review and approval.** Automation drafts, organises, and logs — it does not post. (See `automate-first.md`.)
- Publishing is one item at a time at a human pace, with varied spacing — never bulk-scheduled blasts across platforms.
- Every published item gets a follow-up check, and winners get a follow-up *piece*.

## 5. Support Ticket Triage

```
Customer message arrives (inbox / form / helpdesk)
  -> [AUTO] Create ticket with customer record attached (CRM lookup)
  -> [AUTO] Acknowledge receipt instantly ("We've got it — here's your reference")
  -> [AUTO] First-pass categorisation by keyword / form field:
            billing / technical / account access / general / urgent-signal words
  -> [CHECK] Urgent or sensitive? (payment failure, legal, security, distressed customer, refund request)
       YES -> [AUTO] Flag URGENT + alert a human immediately
              -> [HUMAN] Human takes the ticket end-to-end. No automated replies beyond the acknowledgement.
       NO  -> [AUTO] Route to the right queue / owner by category
              -> [HUMAN] Owner replies — templates allowed as a starting draft, edited and sent by a human
              -> [CHECK] Resolved?
                     NO  -> [HUMAN] Escalate to senior owner; ticket stays open with a next-update time promised to the customer
                     YES -> [HUMAN] Send closing message ("closing this — reply any time to reopen")
                            -> [AUTO] Mark resolved; log category + resolution on the customer record
                            -> [AUTO] If the same category spikes, alert the team (pattern = a product/process fix waiting to happen)
```

Key rules:
- Automation triages and routes; humans resolve. The customer should never discover they were talking to a sequence.
- Sensitive categories bypass the standard queue entirely — speed and a human, in that order.
- Ticket categories are data: review them regularly and fix the upstream cause (a confusing email, a broken step, a missing FAQ), not just the individual tickets.

## Using These Maps

1. Copy the map for the workflow you are building.
2. Replace the generic steps with *your* tools, owners, and intervals — and write down why wherever you change a step.
3. Build only the `[AUTO]` steps in your automation platform.
4. Run the workflow manually alongside the automation for the first few cycles and compare — fix the map where reality disagrees with it.
5. Review each map quarterly. Processes drift; maps (and automations) must drift with them, deliberately.
