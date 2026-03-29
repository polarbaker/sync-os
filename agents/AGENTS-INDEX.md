# Sync AI OS - Agent Registry

> 5 agents purpose-built for Sync's current stage: pre-seed, post-MVP validation.

---

## Agent Roster

| Agent | Tier | Score | Purpose | Command |
|-------|------|-------|---------|---------|
| **@experiment-lab** | 1A | 10.0 | Design and track lean startup experiments with SFE methodology | `/experiment` |
| **@growth-hacker** | 1A | 9.5 | Viral loop modeling, CAC optimization, referral experiment design | `/growth` |
| **@match-quality** | 1A | 9.5 | Suggestion quality tracking, override analysis, preference intelligence | `/match` |
| **@network-bootstrapper** | 1A | 9.5 | Cold start strategy, network density modeling, city launch planning | `/bootstrap` |
| **@user-voice** | 1A | 9.0 | User interview prep, feedback synthesis, NPS tracking, feature prioritization | `/research` |

---

## Why These 5

Sync is in the **validation phase**. The product works (users attend events they schedule), but the business model needs proof and the product has two specific risks that need dedicated attention:

1. **@experiment-lab** because the SFE methodology demands rigorous experiments. Every product and growth decision should flow through a structured hypothesis-test-learn cycle.

2. **@growth-hacker** because CAC = $16.60 via paid social is the existential threat. Sync needs to crack organic/viral growth or the unit economics will never work at $4.99/month.

3. **@match-quality** because "I'd rather go to a piano bar, not a violin concert" is the core product risk. If suggestions don't resonate, users stop opening the app. The recommendation engine IS the product -- this agent makes sure it's getting smarter, not just busier.

4. **@network-bootstrapper** because the cold start problem kills social products. Users said "friends need to already be on Sync" -- but who goes first? This agent models the density math, designs the experience for users who arrive before their friends, and identifies the connector nodes that bootstrap network effects fastest.

5. **@user-voice** because the best product insights so far (the override feature, the network effects requirement) came directly from talking to users. Scaling this research rigor is how Sync avoids building the wrong thing.

---

## How the Agents Connect

```
@user-voice (interviews) --> insights feed --> @experiment-lab (test it)
                                                      |
                                                      v
@match-quality (what's working?) <----- @experiment-lab (A/B results)
                                                      |
                                                      v
@network-bootstrapper (density) -----> @growth-hacker (scale it)
```

- @match-quality depends on density: low-density users have worse match quality (less data)
- @growth-hacker depends on @network-bootstrapper: k-factor only works with density
- @experiment-lab is the backbone: every hypothesis from the other 4 agents flows through it
- @user-voice feeds all agents: interview insights inform match tuning, bootstrapping strategy, and growth levers

---

## Agent Details

See individual agent files:
- `agents/experiment-lab/AGENT.md`
- `agents/growth-hacker/AGENT.md`
- `agents/match-quality/AGENT.md`
- `agents/network-bootstrapper/AGENT.md`
- `agents/user-voice/AGENT.md`

Command definitions (for Claude Code):
- `.claude/commands/experiment.md`
- `.claude/commands/growth.md`
- `.claude/commands/match.md`
- `.claude/commands/bootstrap.md`
- `.claude/commands/research.md`
