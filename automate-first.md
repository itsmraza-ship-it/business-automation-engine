# Automate First

You cannot automate everything, and you should not try. Sequence matters: automate the boring, repetitive, low-risk work first, prove it, and expand from there — while keeping a clear list of things that never get automated at all.

## Automate First

These are high-frequency, rule-based, and forgiving of imperfection because a human still sees the outcome.

### 1. Data entry and record creation
- Form submission → CRM record created with source, date, and owner
- Booking → calendar event + CRM activity logged
- Payment → invoice marked paid, receipt filed, record updated
- The rule: a human should never copy information from one of your systems into another one by hand.

### 2. Reminders
- Follow-up tasks when a lead, proposal, or ticket goes quiet
- Invoice due-date and past-due reminders (the ladder in `workflow-maps.md`)
- Contract / renewal / deadline reminders for the team and, where appropriate, the client
- Intake-form reminders during onboarding
- Reminders are the safest automation there is: worst case, a human gets nudged unnecessarily.

### 3. Status notifications
- "We received your enquiry / application / ticket" acknowledgements
- Order / project / delivery status updates at defined milestones
- "Your document / invoice / proposal is ready" notices with the link
- Notifications state facts from your system of record — they do not make promises a human has not approved.

### 4. Internal alerts
- New lead, new payment, new ticket, failed payment, urgent-keyword ticket → alert to the right person in the channel the team actually watches
- Automation failure alerts: when a workflow errors or stops, a human hears about it the same day, not at the quarterly review
- Daily / weekly digest of pipeline movement, overdue items, and open loops

### Also early wins
- Template generation: proposals, invoices, and onboarding task lists pre-filled from CRM data for a human to check and send
- File organisation: client documents saved to the right folder with a consistent naming pattern
- Meeting plumbing: booking links, confirmation emails, calendar holds, and a pre-call intake summary

## Never Automate

Some actions carry judgement, money, reputation, or account risk. Automation may *draft* or *queue* them. A human performs or approves them, every time.

### Final client answers on sensitive matters
- Advice on legal, tax, medical, financial, immigration, or compliance situations specific to a client's facts
- Answers to complaints, disputes, or distressed customers
- Anything where being wrong has consequences for the client — a human who is accountable must own the answer

### Refunds and approvals
- Refunds, credits, write-offs, and goodwill payments
- Discounts, price exceptions, and changed payment terms
- Approving contracts, proposals with non-standard terms, hiring, and vendor commitments
- Automation can route the request and assemble the information. The decision is a person's.

### Public posts without review
- Social posts, blog publishes, ads, press, and partner-facing announcements
- Automation may draft, schedule a *review task*, and log the result — it never publishes on its own
- This includes "harmless" automated replies and comments: public words in your name require your eyes first

### Anything that can spam or ban-risk an account
- Bulk posting, bulk messaging, mass DMs, automated engagement (likes / follows / comments) on social platforms
- Cold-blasting purchased or scraped lists, or mailing a warm list with cold tactics (see `email-automation.md`)
- Exceeding a platform's, provider's, or mailbox's rate and volume limits to move faster
- If the shortcut could get an account warned, restricted, or banned, it is not a shortcut. It is a liability with a timer on it.

### Also never
- Deleting records, lists, or files without a human confirming what is being deleted
- Changing prices, terms, or policies in customer-facing systems
- Closing a complaint or dispute as "resolved" without the customer confirming it

## How to Judge a Candidate Automation

Ask five questions. Automate only if all five pass:

1. **Is it repetitive?** Happens the same way, many times, with the same inputs.
2. **Is it rule-based?** The decision logic can be written down without "use your judgement".
3. **Is the cost of an error low — and reversible?** A wrong reminder is trivial; a wrong refund is not.
4. **Is it logged?** You can see what it did, when, and to which record.
5. **Does it stay inside every platform / provider limit?** With margin, not at the edge.

If a candidate fails question 2, 3, or 5, it belongs on the Never Automate side (or stays human with automation only drafting / routing).

## 30-Day Rollout Order

A realistic first month. One workflow at a time — finish, test, and live with each one before building the next.

### Week 1 — Foundation (no sending, no publishing)
- [ ] Pick your system of record (CRM) and clean it: stages, owners, source tags
- [ ] Map your first workflow on paper using `workflow-maps.md` — start with **New Lead**
- [ ] Connect the automation platform to the CRM and forms; set up logging
- [ ] Build: form → CRM record + owner assignment + internal alert
- [ ] Test it yourself end-to-end before any real lead touches it

### Week 2 — Lead and Follow-Up Discipline
- [ ] Add the automated acknowledgement email (human-written copy, approved)
- [ ] Build follow-up task reminders for quiet leads and open proposals
- [ ] Set up the master suppression list and dedupe rules (see `email-automation.md`)
- [ ] Run the New Lead workflow live; review the log daily this week and fix friction

### Week 3 — Money Plumbing
- [ ] Map and build the **Invoice + Payment Reminder Ladder** (`workflow-maps.md`)
- [ ] First invoice per client stays human-verified; repeats can generate automatically
- [ ] Add payment-received alerts + automatic receipts
- [ ] Build the **New Client Onboarding** workflow: welcome email, intake form, task list, milestones

### Week 4 — Support, Content, and Review
- [ ] Build **Support Ticket Triage**: acknowledgement, categorisation, urgent-flag routing
- [ ] Build the **Content Publishing Pipeline** tracker flow — drafting, review, publish log, repurposing and follow-up-check tasks (publishing itself stays human)
- [ ] Set up the weekly automation review: check logs, failures, and volumes; pause or fix anything behaving oddly
- [ ] Write down what is *not* automated in your business, using the Never Automate list above — and make sure the whole team knows it

### After Day 30
- Expand only from a proven base: the next workflow gets mapped, built, tested, and reviewed the same way.
- Revisit each automation quarterly. Business processes change; an automation faithfully running last quarter's process is a bug, not a feature.
- Track the payoff honestly: hours saved, follow-ups that no longer slip, invoices paid faster, reviews actually collected. Automate more of what measurably works.

## The Principle

Automate the plumbing — data, reminders, notifications, alerts — so humans have more time for the work that actually needs a human: judgement, relationships, and trust.
