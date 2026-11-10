# Email Automation

Email is the highest-leverage — and highest-risk — automation in a small business. Done well, it makes a small team feel responsive and organised. Done badly, it lands in spam, annoys the people you most want to keep, and damages the domain every other email depends on.

These rules keep email working for you.

## The First Distinction: Cold vs. Warm

Everything else in this file follows from one separation:

- **Warm email** — people who know you: clients, opted-in leads, subscribers, giveaway entrants, community members, partners. They gave you their address for this.
- **Cold email** — people who have never heard of you, contacted because they fit a profile.

### The separation rules

1. **Never cold-blast a warm list.** Your warm list is an asset built on permission. Using it for cold-style blasts burns trust and deliverability at the same time.
2. **Separate sending streams.** Warm/transactional email and cold outreach run on separate domains / subdomains and separate sending setups, so a deliverability problem in outreach can never take down your client invoices, onboarding mail, and subscriber email with it.
3. **Separate lists, separate tools where it helps.** Keep warm-list platforms (newsletters, sequences) distinct from cold-outreach tooling. If one database contains both, tagging and suppression discipline must be airtight — and separate is simpler.
4. **A person moves from cold to warm only by opting in** — replying with genuine interest, booking a call, signing up, or becoming a client. Scraping or buying a "warm-looking" list does not make it warm.

## Welcome Sequence Outline

For new subscribers / opted-in leads / new clients (adapt the emphasis to the audience — the structure holds):

| Email | Timing | Job |
|---|---|---|
| 1 — Welcome + deliver the promise | Immediately | Thank them, deliver exactly what they signed up for (resource, confirmation, next step), set expectations: what you'll send and roughly how often |
| 2 — Your story / credibility | Shortly after | Why you exist, who you help, one piece of proof or a short story. Human tone, signed by a real person or team |
| 3 — Best useful content | Next in sequence | Your single most helpful resource on their core problem. Pure value, no pitch |
| 4 — The problem, reframed | Next | The common mistake / myth in your niche, and the better way — positions your thinking, still no hard sell |
| 5 — Soft offer + reply prompt | Next | What working with you looks like, one clear next step, and an easy question they can reply to ("What are you working on right now?") |

Rules:
- Every sequence email must be worth opening on its own. If an email only exists to "warm them up for the pitch", cut it.
- One idea per email, one call to action per email.
- Plain, personal formatting beats heavy design for sequence mail — it should read like mail from a person.
- The sequence ends. After it, subscribers move to your regular cadence — they do not sit in sequences forever.

## Follow-Up Cadence

For leads and conversations (separate from the welcome sequence):

- **After an enquiry / form submission:** instant automated acknowledgement, then a human's personal follow-up promptly (see `workflow-maps.md`, New Lead).
- **After a proposal:** check in on a human timescale — a short, specific message referencing *their* situation, not a generic "just bumping this". A small number of follow-ups, spaced days apart, each adding something (an answer, a resource, a deadline that is real).
- **After delivery:** a check-in once the client has had time to use the work, then the review / referral request at the moment of evident satisfaction — not on a blind timer.
- **Long-term nurture:** occasional genuinely useful content for not-now leads, at a modest cadence, with an easy unsubscribe. When a lead replies, automation stops and a human takes over — always.
- **Stop conditions are part of the cadence.** A reply, a booking, a purchase, or an unsubscribe ends the sequence immediately. Sequences that keep emailing people who already answered are the fastest way to look like a robot.

## Per-Mailbox Volume Discipline and Warm-Up

Deliverability is a reputation you build slowly and lose quickly.

- **Warm up new mailboxes and domains gradually.** Start with low daily volume to engaged recipients and increase in steps over weeks. A brand-new mailbox sending at full volume on day one is the classic spam-folder pattern.
- **Respect hard per-mailbox daily and hourly caps** — set them in your tooling, below your provider's limits, and do not raise them to "get a batch out". Volume you cannot sustain safely is volume you should not send.
- **Keep volume consistent.** Steady, predictable sending looks like a business. Spikes look like a campaign blast — because they are one.
- **Engagement is the metric that matters.** Opens, replies, and clicks from real people protect your reputation; raw send counts do not. Prune chronically unengaged addresses instead of mailing them forever.
- **Authenticate every sending domain** (SPF, DKIM, DMARC) and verify it before the first send, not after the first spam complaint.
- **Test before you scale.** Send any new template or sequence to seed / test inboxes first and check placement (inbox vs. spam) before it goes to a real list. If the seeds say spam, you fix and retest — you do not send anyway and hope.

## Suppression Lists

A suppression list is the memory of your email system. Honour it absolutely.

Suppress (never email again via automation):
- Anyone who unsubscribed
- Hard bounces (address does not exist)
- Anyone who marked you as spam
- People who asked to be removed in a reply, in any wording
- Existing clients / active conversations, from any outreach sequence they should not be in
- Colleagues, partners, and competitors, from prospecting sequences

Rules:
- **One master suppression list**, checked by every tool and every sequence before sending — not a separate list per campaign that drifts out of sync.
- Suppression is permanent by default. Removing a suppression requires a human decision and a clear reason (for example, the person re-subscribed), logged.
- Check new lists *against* the suppression list at import time, not at send time.
- Duplicates are a suppression problem too: dedupe every import, so nobody gets the same sequence twice from two list copies.

## Human Sign-Off Before Campaigns

Automation sends sequences you approved. Campaigns — one-off sends to a list — get approved fresh, every time.

Before any campaign sends, a human confirms:

- [ ] **Audience:** exactly who is receiving this, and why they are warm for it (or, for outreach, which separate cold stream it belongs on)
- [ ] **List hygiene:** deduped, checked against the master suppression list, bounces removed
- [ ] **Content:** read in full — claims verified, links clicked, names/pronunciation checked, sign-off correct, no placeholder text anywhere
- [ ] **Offer honesty:** prices, dates, deadlines, and availability in the email are real and current
- [ ] **Volume plan:** send volume fits the per-mailbox caps and the warm-up state of the sending mailboxes
- [ ] **Seed test passed:** the final version was tested and landed in the inbox
- [ ] **Timing:** not colliding with another campaign or sequence peak to the same audience
- [ ] **Off-switch:** someone is available to pause the campaign and handle replies when it lands

No campaign sends on "it looked fine last time". Templates change, lists change, and reputations are lost in a single careless send.

## The Short Version

Warm and cold never mix. Sequences serve, follow-ups are human the moment a human replies. Volume grows gradually, caps are hard, suppression is permanent, and a person signs off before anything goes to a list.
