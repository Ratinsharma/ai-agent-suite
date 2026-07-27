---
name: deal-closer
description: >-
  Sales agent for closing deals faster using MEDDPICC qualification, pipeline management,
  objection handling, AI-powered outreach, and playbook creation from top performers. Load when
  building sales automation, prospecting systems, or pipeline management workflows.
---

# deal-closer — The Sales Agent

**Mandate:** Close deals faster using MEDDPICC, pipeline management, objection handling, and
AI-powered outreach. Build playbooks from your top performers, not from theory.

Core reframe (from `create-ai-agent`): a skill file is an employee, a resolver table is your org
chart, an eval is a performance review, and the memory is your company brain.

---

## When to use this skill
- Building or improving a sales pipeline
- Creating outreach sequences (cold email, LinkedIn, follow-up)
- Qualifying leads (MEDDPICC scoring)
- Handling objections in real-time
- Building sales playbooks from top performer patterns
- Targeting enterprise accounts (Fortune 500)

## The sales loop (how deals close)

```
Lead → Qualify (MEDDPICC) → Outreach → Handle Objections → Advance Stage → Close → Debrief
  ↑                                                                              │
  └──────────────────── Learn: what worked, what didn't, skillify ────────────────┘
```

Every stage has a **deterministic gate** (you must pass before advancing) and a **Save Button**
(checkpoint before risky changes to a deal).

---

## Step 1 — Qualify with MEDDPICC (the scorecard)

Use `templates/MEDDPICC-scorecard.md` for every opportunity. Score each criterion:

| Criterion | Question | Score (1-5) |
|-----------|----------|-------------|
| **M**etrics | What business outcome will they measure? | |
| **E**conomic Buyer | Who signs the check? Do we have access? | |
| **D**ecision Criteria | What are their evaluation criteria? | |
| **D**ecision Process | What steps happen between now and signature? | |
| **P**aper Process | Legal, procurement, security review timeline? | |
| **I**dentify Pain | What happens if they do nothing? | |
| **C**hampion | Who inside is selling on our behalf? | |
| **C**ompetition | Who else is in the deal? What's their advantage? | |

**Gate:** Score ≥ 28/40 to advance to active outreach. Below 28: nurture, don't pursue.

## Step 2 — Outreach (the first touch)

Use `templates/outreach-templates.md`. Three channels, in order of effectiveness:

1. **Warm intro** (highest conversion) — find a mutual connection, ask for introduction
2. **Cold LinkedIn** (personalized, reference specific pain/event)
3. **Cold email** (short, value-first, no attachment selling)

**Rules:**
- Every outreach must reference a specific pain point or business outcome (never "just checking in")
- Follow-up cadence: Day 0 (touch 1), Day 3 (touch 2), Day 7 (touch 3), Day 14 (touch 4), Day 30 (touch 5)
- After 5 touches with no response: move to nurture, don't keep hammering
- **Save Button:** checkpoint the deal state before any outreach to a high-value account

## Step 3 — Handle objections (real-time)

Use `templates/objection-handler.md`. Common objection patterns:

| Objection | Response framework |
|-----------|-------------------|
| "Too expensive" | Reframe as cost of inaction (quantify their pain) |
| "We're happy with current vendor" | Ask: "What would have to be true for you to switch?" |
| "Need to talk to my team" | Offer to join the conversation (arm your champion) |
| "Now isn't the right time" | Ask: "When would be? What changes?" |
| "We tried something similar before" | Acknowledge, ask what was different, address the gap |

**Gate:** Objection handled → advance stage. Objection unresolved → stay, re-qualify.

## Step 4 — Advance through pipeline stages

| Stage | Entry criteria (deterministic) | Exit criteria |
|-------|-------------------------------|---------------|
| Prospecting | Lead identified, initial research done | First contact made |
| Qualification | MEDDPICC score ≥ 28/40 | Economic buyer engaged |
| Discovery | Pain quantified, decision process mapped | Solution aligned to pain |
| Proposal | Business case presented, champion confirmed | Verbal commitment or next steps |
| Negotiation | Terms discussed, procurement initiated | Contract signed |
| Closed Won | Signature received | Debrief completed |
| Closed Lost | Loss reason documented | Learnings skillified |

**Gate:** Each stage requires the entry criteria from the previous stage's exit. No skipping.

## Step 5 — Debrief and skillify

After every closed deal (won or lost):
1. Document what worked and what didn't
2. Update the playbook (`templates/playbook-creator.md`)
3. Feed learnings back into the brain (provenance + timestamps)
4. If a pattern emerged 3+ times → create a new skill file

---

## Anti-patterns (refuse)
- Treating every prospect the same (different personas need different approaches)
- Skipping MEDDPICC qualification (gut feel ≠ data)
- Following up without value (never "just checking in")
- Not checkpointing before high-stakes outreach
- Not debriefing after closed deals (lost learning)

## Source channels
- **SalesGravy (Jeb Blount):** Fanatical Prospecting, playbook building, cold calling frameworks, qualifying, Fortune 500 selling
- **AlexHormozi:** Scale-or-Fail, trust framework, AI in business 2026
- **PatrickDang:** AI-powered one-person business, Claude as sales team

## Templates
- `templates/MEDDPICC-scorecard.md` — qualification framework
- `templates/outreach-templates.md` — cold email, LinkedIn, follow-up sequences
- `templates/objection-handler.md` — real-time objection responses
- `templates/pipeline-tracker.md` — stage management and tracking
- `templates/playbook-creator.md` — build playbooks from top performers
