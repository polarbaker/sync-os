# Sync AI OS

> Turn social intention into real-world connection -- the AI backbone for Sync's growth engine.

**Built by [Gold Star AI](https://goldstarai.com) for Anouk Frieden | HBS Strategy for Entrepreneurs (1257)**

---

## What Is This?

Sync AI OS is a 3-agent AI operating system built for **Sync**, a mobile-first AI platform that maps your social network, surfaces who to spend time with, and curates activities aligned with your goals.

These agents are designed for Sync's current stage: **pre-seed, post-MVP validation**. They target the three things that matter most right now.

## The 3 Agents

| Agent | Command | What It Does |
|-------|---------|--------------|
| **@experiment-lab** | `/experiment` | Design and track lean startup experiments with clear hypotheses, budgets, and theory-of-value updates |
| **@growth-hacker** | `/growth` | Model viral loops, optimize CAC, design referral experiments, plan city launches |
| **@user-voice** | `/research` | Prep user interviews, capture feedback, track NPS, synthesize feature priorities |

## Quick Start

### Prerequisites
- [Claude Code](https://claude.ai/code) installed
- Google Workspace MCP connected

### Run Your First Command

```bash
# Open this directory in Claude Code
cd sync-os

# Design your next experiment
/experiment design "Friend-invite onboarding flow achieves k > 0.5 in pilot cohort"

# Analyze your growth funnel
/growth analyze

# Prep for user interviews
/research prep "churned users"
```

## Project Structure

```
sync-os/
├── CLAUDE.md                          # System instructions (agents, workflows, context)
├── README.md                          # This file
├── .mcp.json                          # MCP server configuration
├── .claude/
│   ├── settings.local.json            # Tool permissions
│   └── commands/
│       ├── experiment.md              # /experiment command definition
│       ├── growth.md                  # /growth command definition
│       └── research.md               # /research command definition
└── agents/
    ├── AGENTS-INDEX.md                # Agent registry and rationale
    ├── experiment-lab/AGENT.md        # @experiment-lab full spec
    ├── growth-hacker/AGENT.md         # @growth-hacker full spec
    └── user-voice/AGENT.md            # @user-voice full spec
```

## Why These 3 Agents?

Based on Sync's SFE memo:

1. **@experiment-lab** -- The SFE methodology is hypothesis-driven. Every product and growth decision should flow through a structured experiment cycle. This agent makes that process repeatable.

2. **@growth-hacker** -- Experiment 2 proved paid acquisition doesn't work at $16.60 CAC on a $4.99/month product. Cracking organic/viral growth is existential. This agent models the math and designs the tests.

3. **@user-voice** -- The best product insights so far (override feature, network effects priority) came from 10 user interviews. Scaling that research rigor is how Sync avoids building the wrong thing next.

---

Built by [Gold Star AI](https://goldstarai.com)
