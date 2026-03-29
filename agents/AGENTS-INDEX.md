# Sync AI OS - Agent Registry

> 3 agents purpose-built for Sync's current stage: pre-seed, post-MVP validation.

---

## Agent Roster

| Agent | Tier | Score | Purpose | Command |
|-------|------|-------|---------|---------|
| **@experiment-lab** | 1A | 10.0 | Design and track lean startup experiments with SFE methodology | `/experiment` |
| **@growth-hacker** | 1A | 9.5 | Viral loop modeling, CAC optimization, referral experiment design | `/growth` |
| **@user-voice** | 1A | 9.0 | User interview prep, feedback synthesis, NPS tracking, feature prioritization | `/research` |

---

## Why These 3

Sync is in the **validation phase**. The product works (users attend events they schedule), but the business model needs proof:

1. **@experiment-lab** because the SFE methodology demands rigorous experiments. Every product and growth decision should flow through a structured hypothesis-test-learn cycle.

2. **@growth-hacker** because CAC = $16.60 via paid social is the existential threat. Sync needs to crack organic/viral growth or the unit economics will never work at $4.99/month.

3. **@user-voice** because the best product insights so far (the override feature, the network effects requirement) came directly from talking to users. Scaling this research rigor is how Sync avoids building the wrong thing.

---

## Agent Details

See individual agent files:
- `agents/experiment-lab/AGENT.md`
- `agents/growth-hacker/AGENT.md`
- `agents/user-voice/AGENT.md`

Command definitions (for Claude Code):
- `.claude/commands/experiment.md`
- `.claude/commands/growth.md`
- `.claude/commands/research.md`
