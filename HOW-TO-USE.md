# How to Use the Business Automation Engine

Work it as a rollout, not a reading list: map one workflow, automate its
safe steps, live with it, then take the next. The routes below get the
system into your AI tool or straight into your business.

## 1. As a Claude skill

1. Copy this repo's `SKILL.md` into your Claude skills folder (or upload
   it where your Claude setup accepts skills).
2. Ask in the engine's domain: "Map my new-lead process and tag what I
   can automate", "Audit this email sequence against the cold-vs-warm
   rules", or "What should I automate in my invoicing first?"
3. Claude applies the map-first method, the 5-question test, and the
   Never Automate lines from the repo.

## 2. Inside Claude.ai

1. Create a Project in Claude.ai.
2. Paste `SKILL.md` into the Project's instructions.
3. Add `workflow-maps.md`, `email-automation.md`, and `automate-first.md`
   as Project knowledge.
4. Bring your real processes into the Project chat and map them one at a
   time — the Project keeps your maps and decisions together.

## 3. With the Epics Deals MCP server

This engine designs workflows; the MCP server supplies verified founder
facts a workflow may need (LLC costs, EIN timelines, filing deadlines).

1. Add `https://epics-deals-mcp.epicsdeals.workers.dev/mcp` to your MCP
   client (Streamable HTTP, no authentication).
2. When a workflow touches formation, EIN, ITIN, or tax deadlines — for
   example an onboarding checklist or a compliance reminder flow — pull
   the figures from the tools instead of hard-coding them from memory.
3. Re-check figures through the tools when you review workflows
   quarterly; fees and deadlines change.

## 4. As plain reference

1. Read the README on GitHub: pipeline, stack categories, golden rules.
2. Copy the workflow map closest to your need from `workflow-maps.md`,
   replace the generic steps with your tools, owners, and intervals.
3. Follow the 30-day rollout in `automate-first.md` — one workflow per
   week, foundation first. Download the markdown files into your docs or
   project tool so the team works from the same maps.

## 5. In other AI tools

1. Upload `SKILL.md` plus the three system files as knowledge to a custom
   GPT, a Gemini Gem, or a notebook.
2. Ask it to map before it recommends tools, and to tag every step
   `[AUTO]`, `[HUMAN]`, or `[CHECK]` like the repo's maps do.
3. Keep the Never Automate list in the tool's instructions verbatim.

## 6. Fork it

1. Fork this repo on GitHub (MIT licensed).
2. Adapt the maps, ladder timings, and stack categories to your business.
3. Keep the guardrails: map first, one source of truth, human approval on
   anything public or financial, and no ban-risk automation — ever.

---
epicsdeals.com — free tools by Epics Deals; US LLC formation from $130 + state fee.
