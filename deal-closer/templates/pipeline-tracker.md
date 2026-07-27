# Pipeline Tracker

> Track every deal through stages. No skipping stages. Checkpoint before high-stakes actions.

## Active Pipeline

| Deal | Company | Stage | MEDDPICC | Next Action | Owner | Checkpoint |
|------|---------|-------|----------|-------------|-------|------------|
| | | | /40 | | | |

## Stage definitions and gates

### Prospecting
**Entry:** Lead identified, initial research done
**Activities:** LinkedIn research, identify pain signals, find warm intro path
**Exit criteria:** First contact made
**Deterministic gate:** Research doc exists with ≥3 pain signals

### Qualification
**Entry:** First contact made
**Activities:** Discovery call, MEDDPICC scoring
**Exit criteria:** MEDDPICC score ≥ 28/40
**Deterministic gate:** Scorecard completed and scored

### Discovery
**Entry:** MEDDPICC ≥ 28
**Activities:** Deep-dive on pain, decision process, competition
**Exit criteria:** Pain quantified, decision process mapped, champion identified
**Deterministic gate:** Pain ROI documented, decision timeline mapped

### Proposal
**Entry:** Discovery complete
**Activities:** Present solution, build business case, address remaining objections
**Exit criteria:** Verbal commitment or clear next steps
**Deterministic gate:** Business case document delivered, champion confirms

### Negotiation
**Entry:** Proposal accepted
**Activities:** Terms discussion, legal review, procurement
**Exit criteria:** Contract signed
**Deterministic gate:** Redlines resolved, procurement timeline tracked

### Closed Won
**Entry:** Signature received
**Activities:** Handoff to implementation, debrief, skillify learnings
**Exit criteria:** Debrief completed, playbook updated
**Deterministic gate:** Debrief doc exists, learnings fed to brain

### Closed Lost
**Entry:** Deal lost or disqualified
**Activities:** Loss reason documented, learnings extracted, playbook updated
**Exit criteria:** Learnings skillified
**Deterministic gate:** Loss reason + learnings documented

## Weekly review checklist
- [ ] All active deals have next actions assigned
- [ ] No deal has been in the same stage for >14 days (escalate or advance)
- [ ] MEDDPICC scores updated for all deals in Qualification+
- [ ] Checkpoints exist for all high-value deals (≥$50K)
- [ ] Closed deals debriefed and learnings fed to brain
