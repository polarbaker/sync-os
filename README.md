# Sync AI OS

> Your AI-powered operations toolkit -- built specifically for where Sync is right now.

**Built by [Gold Star AI](https://goldstarai.com) for Anouk Frieden | HBS Strategy for Entrepreneurs (1257)**

---

## What Is This?

This is an **AI Operating System** custom-built for Sync. It gives you 5 AI agents that work as specialized assistants, each focused on a specific challenge Sync faces right now. They're informed by your SFE memo -- your experiment results, your pricing data, your growth challenges, and the specific feedback from your pilot users.

You talk to them in plain language. They think, then do the work -- creating spreadsheets, documents, and analyses in Google Workspace. Think of them as five very focused interns who've read everything about Sync and never forget anything.

---

## Your 5 Agents

### 1. @experiment-lab -- Your Experiment Partner

**The problem it solves:** The SFE methodology requires rigorous experiments, but structuring hypotheses, defining success criteria, and tracking results across multiple experiments gets messy fast.

**What it does:** You tell it what you want to test, and it builds you a complete experiment brief -- hypothesis, success criteria, budget, timeline, and what to measure. After you run the experiment, you feed it results, and it updates your Theory of Value, tells you whether P and V went up or down, and recommends whether to develop, pivot, or kill. It keeps a running log of all your experiments so the learning compounds.

**Example:** "Design an experiment to test whether a referral bonus reduces CAC below $3" -- and it builds the full brief with measurable criteria and a budget cap.

---

### 2. @growth-hacker -- Your Acquisition Strategist

**The problem it solves:** Paid ads didn't work ($16.60 per user on a $4.99/month product). You need to figure out organic and viral growth, but the math is complex -- viral coefficients, referral loops, city-level density -- and guessing wrong is expensive.

**What it does:** It models the viral loop math for you. How many invites does each user send? What percentage accept? What percentage actually activate? It projects growth curves, tracks your cost per user across different channels, and designs city-specific launch plans. It also calls out when something won't work before you spend money on it.

**Example:** "Model what growth looks like if we launch in Zurich with 50 seed users and achieve a 0.6 viral coefficient" -- and it projects the curve and tells you when (or if) you'd hit self-sustaining growth.

---

### 3. @match-quality -- Your Recommendation Tuner

**The problem it solves:** Your pilot users said "I'd rather go to a piano bar, not a violin concert." The override feature was a quick fix, but the deeper issue remains: how does Sync learn what someone actually wants? If the suggestions don't land, people stop opening the app. The recommendation engine is the product.

**What it does:** It tracks whether your suggestions are actually working -- not just whether someone taps "accept," but whether they show up to the event. It categorizes WHY suggestions miss: was it the wrong activity type? Wrong friend pairing? Wrong time? Wrong vibe? It spots the difference between what users say they want (their goals during onboarding) and what they actually choose (their real behavior). Over time, it shows you exactly where your recommendation engine is improving and where it's still broken.

**Example:** "Show me the override analysis for the last 30 days" -- and it tells you that 40% of overrides are "right idea, wrong venue" (meaning your logic is close but your event data needs work), which is a very different fix than if they were saying "wrong activity type entirely."

---

### 4. @network-bootstrapper -- Your Cold Start Strategist

**The problem it solves:** Your users told you the hard truth: "friends need to already be on Sync." But someone has to be first. This is the chicken-and-egg problem that kills most social products. Sync is most useful when your friends are on it, but your friends won't join until it's useful.

**What it does:** It models the math of network density. How many users do you need in one city before new signups already have friends on the platform? (That's the tipping point.) It designs what the experience should feel like at every stage -- when someone has zero friends on Sync (survival mode), when they have 2-3 friends (starting to click), and when they have 10+ (full value). It identifies "connector nodes" -- people with large, overlapping social networks who should be your very first users. And it evaluates every way to import contacts (phone, calendar, Instagram) ranked by how easy it is for the user and how privacy-safe it is.

**Example:** "Design the Day 1 experience for someone who joins Sync before any of their friends" -- and it maps out what features still deliver value, what the "aha moment" is for a solo user, and what action they need to take to pull in their first friend.

---

### 5. @user-voice -- Your Research Partner

**The problem it solves:** Your two best product insights (the override feature and the network effects priority) came from talking to just 10 people. But as you do more interviews, keeping track of what everyone said, spotting patterns, and turning raw notes into product decisions gets overwhelming.

**What it does:** It prepares interview guides tailored to specific user segments (power users, people who churned, waitlist signups). After each interview, you feed it your notes and it extracts the structured data -- pain points, feature requests, NPS score, willingness to pay, key quotes. When you've done several interviews, it synthesizes everything: top themes ranked by frequency, NPS trend, feature priorities, and the questions you still haven't answered. It also flags when what people say they want doesn't match what they actually do.

**Example:** "I just interviewed 5 waitlist signups, here are my notes" -- and it pulls out the patterns, updates your NPS, and tells you the top 3 things these users want that you don't have yet.

---

## How the Agents Work Together

The agents aren't isolated -- they feed into each other:

- **@user-voice** uncovers insights from interviews, which become hypotheses for **@experiment-lab**
- **@experiment-lab** runs tests on growth ideas from **@growth-hacker** and recommendation changes from **@match-quality**
- **@network-bootstrapper** builds the density that **@growth-hacker** needs for viral math to work
- **@match-quality** gets better as **@network-bootstrapper** increases density (more friends = more data = better suggestions)

The backbone is **@experiment-lab** -- every hypothesis from the other four agents flows through it for structured testing.

---

## Getting Started

### What You Need
1. **Claude Code** -- download it at [claude.ai/code](https://claude.ai/code) (available as a CLI, desktop app, or web app)
2. **Google account** -- the agents create real documents and spreadsheets in Google Workspace

### Your First Session

Once Claude Code is open in this project folder, just type a command:

```
/experiment design "Referral onboarding flow achieves k > 0.5 in first cohort"
```

That's it. The agent reads the command, understands the context (your pricing, your experiment history, your CAC data), and produces a complete experiment brief as a Google Doc.

Other things to try:

| What You Want | What to Type |
|---------------|-------------|
| Design your next experiment | `/experiment design "your hypothesis here"` |
| See your growth funnel | `/growth analyze` |
| Check if suggestions are landing | `/match audit` |
| Plan a city launch | `/bootstrap density-model zurich` |
| Prep for user interviews | `/research prep "churned users"` |
| Log interview notes | `/research log` (then paste your notes) |
| See what users want most | `/research synthesize` |
| Model the viral math | `/growth referral-model` |
| Understand the cold start gap | `/bootstrap day-one solo` |

---

## What's in This Repo

| File | What It Is |
|------|-----------|
| `CLAUDE.md` | The "brain" -- all the context about Sync, your experiments, metrics, and workflows that the agents use |
| `README.md` | This guide |
| `.claude/commands/` | The 5 command definitions (one per agent) |
| `agents/` | Detailed specs for each agent -- their purpose, rules, metrics, and how they connect |

Everything is customized from your SFE memo: your pricing ($4.99 free/premium), your experiment results (10 pilot users, $16.60 CAC from Meta ads), your strategic decisions (geographic densification, organic over paid), and even the specific user feedback ("piano bar not violin concert").

---

## Questions?

This was built by Thomas Baker at Gold Star AI. Reach out if you want to customize anything, add more agents, or talk about how AI operating systems work at the product level.

---

Built by [Gold Star AI](https://goldstarai.com)
