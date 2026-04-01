---
name: icp-builder
description: Build a comprehensive, research-backed ICP and buyer persona document for a client engagement. Writes a complete icp.md to ~/Obsidian/01-Clients/<ClientName>/icp.md. Use this skill whenever the user says /icp-builder, asks to "build the ICP", "create personas", "define the ideal customer profile", "who should we target", or "build out the personas" for a client — even if they don't say /icp-builder explicitly. Also trigger when starting a new client engagement where icp.md is empty or missing.
---

# ICP Builder

Build a comprehensive, research-backed Ideal Customer Profile (ICP) and buyer persona document for a fractional client engagement. The output is a single `icp.md` file saved to the client's directory.

This document is the foundational marketing artifact for the engagement. It informs positioning, messaging, channel selection, content strategy, and outbound targeting. Every other skill that needs to know "who are we talking to?" will read this file. Treat it accordingly — do not produce generic filler. Every claim should trace back to a research source or client context.

---

## Step 1: Identify the Client and Gather Existing Context

Parse the client name from the skill argument. Locate the client directory at `~/Obsidian/01-Clients/<ClientName>/`.

Read all available files in this order:
1. `CLAUDE.md` — engagement context, known ICP hypothesis, product description, GTM challenges, PMF level
2. `context.md` — living briefing doc (may have more up-to-date notes)
3. Any meeting notes (`.md` files — scan for discovery call transcripts, strategy session notes)
4. `icp.md` — check if anything is already there to preserve or build on

While reading, extract and record:
- Product description and core value proposition
- ICP hypothesis (even rough)
- Known buyer roles and personas
- Industry / vertical focus
- ACV and deal motion (SLG, PLG, founder-led)
- PMF level
- Explicit pain points or trigger events mentioned
- Competitive alternatives named
- Any direct customer quotes from meeting notes

If the client directory doesn't exist or CLAUDE.md has minimal info, note what's missing — you'll need to rely more heavily on research in Step 2.

---

## Step 2: Research Phase

Do not skip this step, even with strong existing context. Research validates what you know, surfaces buyer language you wouldn't otherwise have, and grounds the personas in reality rather than assumption.

Run research across these areas. Use parallel web searches where possible.

### 2a. Buyer Role Research
For each buyer role identified (or hypothesized), search for authentic signals:
- What does this role actually do day-to-day? What does success look like for them?
- What are their real frustrations? (Search: `"[role title]" pain points [industry] site:reddit.com`, `"[role title]" challenges [product category] site:linkedin.com`)
- What language do they use to describe their problem? (Read actual posts and reviews — don't paraphrase into corporate-speak)
- What does their career path typically look like? What are they trying to prove?

### 2b. Buyer Reviews (G2, Capterra, Trustpilot)
Search for reviews of the client's product category:
- `[product category] reviews site:g2.com`
- `[competitor name] reviews site:g2.com`

Read the reviews carefully for:
- Exact phrases buyers use to describe pain ("I was spending 3 hours a week manually...")
- What outcomes they cared about most
- What almost stopped them from buying
- What they wish were better

These reviews are gold for the "Generated Quotes" sections — use actual buyer language.

### 2c. Trigger Event Research
What events make a company enter the buying window RIGHT NOW?
- What business changes, hiring signals, funding events, or performance failures make this pain urgent?
- Are there regulatory, competitive, or market changes driving urgency in this industry?
- Search: `[industry] [pain area] when companies decide to [buy/switch/invest]`

### 2d. Market and Firmographic Research
- What company sizes and revenue ranges are the best fit for this product?
- What verticals buy most often?
- What funding stages are most common?
- What tech stack signals predict a good fit?

### 2e. Competitive Intelligence
- Who else is selling to these buyers? What do buyers choose instead?
- What are buyers unhappy about with alternatives? (This reveals where to differentiate)

---

## Step 3: Identify the Buying Committee

Based on context + research, identify 2–4 key buyer personas. Cover the full buying committee:
- **Economic buyer** — who signs off on budget
- **Champion** — who wants this most and drives internal adoption
- **Influencer / Evaluator** — who researches and shortlists vendors
- **Blocker / Gatekeeper** — who can kill a deal (IT, Legal, Finance)

For each persona, determine:
- Role title and seniority level
- Their role in the buying process
- Their primary job-to-be-done in the context of this product
- The nature and urgency of their pain

---

## Step 4: Write the ICP Document

Write the full `icp.md` using the exact structure below. Do not abbreviate sections — every section should be substantive. Use the client's actual industry, product, and buyer roles throughout. No generic placeholders.

---

### Document Template

```markdown
# [ClientName] — ICP & Persona Map

*Last updated: [YYYY-MM-DD]*
*Status: Draft*

---

## Overview

[2–3 sentences: who the ICP is, what they're trying to accomplish, and why this product fits. Be specific — name the vertical, the role, and the core problem.]

---

## Part 1: ICP Framework

### Tier Definitions

| Tier | Label | Description | Priority |
|------|-------|-------------|----------|
| Tier 1 | Core ICP | [Specific criteria — the bullseye. The account type where you win most often and expand fastest.] | Pursue immediately |
| Tier 2 | Strong Fit | [Accounts that fit well but need more qualification — maybe slightly larger, slightly different vertical, or missing one trigger.] | Qualify first |
| Tier 3 | Opportunistic | [Accounts at the edge of fit — close if inbound, but don't invest outbound resources.] | Inbound only |

---

### Firmographic Profile — Tier 1

| Dimension | Criteria |
|-----------|----------|
| Industry / Vertical | [Specific] |
| Company Size (employees) | [Range] |
| Revenue / ARR Range | [Range] |
| Funding Stage | [Stage(s)] |
| Geography | [Regions] |
| Business Model | [B2B / B2C / Enterprise / SMB / etc.] |
| Tech Stack Signals | [Tools/platforms that signal fit] |
| Other Firmographic Signals | [Anything else predictive] |

---

### Situational / Trigger Events

These are the events that make pain urgent NOW. Tier 1 accounts will have at least one of these present. Be specific — "company is growing" is not a trigger. "Just hired their first SDR team lead" is.

| Trigger | What to Look For | Why It Creates Urgency |
|---------|-----------------|------------------------|
| [Trigger name] | [Observable signal — LinkedIn post, job posting, news, funding announcement] | [Why this event creates pain that needs solving now] |
| [Trigger name] | ... | ... |
| [Trigger name] | ... | ... |

---

### Behavioral / Psychographic Profile (Tier 1)

What separates a Tier 1 account from a Tier 2 at the behavioral level:

**How they evaluate vendors:**
- [Specific behavior]

**What they value in a solution:**
- [Specific values / priorities]

**How they prefer to buy:**
- [Process, timeline, stakeholders involved]

**What establishes credibility:**
- [Social proof types, proof of concept expectations, case study formats that matter]

**Internal signals of readiness:**
- [Org structure, hiring patterns, tech stack changes that indicate they're ready]

---

## Part 2: ICP Scoring Rubric

Use this to score and prioritize inbound leads and outbound target accounts.

| Attribute | Criteria | Points |
|-----------|----------|--------|
| Target industry / vertical | In Tier 1 vertical | 2 |
| Company size / ARR | Within Tier 1 range | 2 |
| Trigger event present | At least one confirmed trigger | 2 |
| Budget authority identified | Economic buyer is reachable / identified | 2 |
| Competitive alternative confirmed | Actively using an alternative we displace | 2 |
| **Total** | | **10** |

> Customize these five attributes to be client-specific. The defaults above are starting points — replace or add dimensions that are more predictive for this specific product and market.

**Score interpretation:**
- 8–10: Pursue immediately
- 5–7: Qualify before investing heavily
- <5: Pass or deprioritize

---

## Part 3: Buying Committee

| Role | Type | Primary Concern | Entry Point? |
|------|------|----------------|--------------|
| [Title] | Economic buyer | [What they care about most] | Yes / No |
| [Title] | Champion | [What they care about most] | Yes / No |
| [Title] | Influencer / Evaluator | [What they care about most] | Yes / No |
| [Title] | Blocker / Gatekeeper | [What they care about most] | No |

---

## Part 4: Trigger Event Map

Narrative description of the 3–5 most common scenarios that open a buying window. Each scenario describes: what just happened at the company, what pain it created, and why it makes them act now.

**Trigger 1: [Name]**
[2–3 sentences — be specific. Name the event, the pain it creates, and the urgency driver.]

**Trigger 2: [Name]**
[...]

**Trigger 3: [Name]**
[...]

---

## Part 5: Persona Documents

[One full persona section per key buyer in the buying committee. Use the structure below for each.]

---

### Persona: [Role Title]

**Name:** [Fictional name]
**Title:** [Exact title]
**Buying Role:** [Economic buyer / Champion / Influencer / Blocker]
**Company Stage Context:** [The company size/stage where this persona is most relevant]
**Experience:** [Background and years in role]
**Reporting Structure:** [Reports to / is reported to by]

#### Profile Summary

[3–5 sentences. Bring this person to life — who they are, what they're trying to accomplish this year, and the pressure they're under. This should read like a real person, not a job description.]

---

#### Jobs to Be Done (JTBD)

[3–6 jobs. For each:]

**[#]. [Job Name]**
**Functional Job:** [The specific task they're trying to accomplish]
**Outcome:** [What success looks like — specific and measurable where possible]

---

#### Main Job Responsibilities

[Key areas of responsibility as subsections. Based on research — what this person actually does, not boilerplate. 3–5 responsibility areas with 3–5 bullets each.]

---

#### Core Challenges

[4–6 specific, research-grounded challenges. For each, surface the underlying fear or worry — the thing they don't say out loud but that drives their decisions.]

Example format:
**[Challenge Name]**
[2–3 sentence description of the challenge in their reality. Include the fear or worry they have about it.]

---

#### Needs

**Professional Needs:**
[What they need to do their job better — functional, tactical]

**Personal Needs:**
[Career advancement, recognition, time, confidence]

**Inferred Needs:**
[Unstated needs they'd recognize if you named them — psychological safety, validation, peer credibility]

---

#### Ideal Experience

[What their world looks like if the problem is solved. Be specific and evocative — what's different on a Tuesday afternoon when this is working?]

---

#### Generated Quotes

[4–6 quotes that capture how this person actually talks about their problem. Pull from real buyer reviews, forum posts, and LinkedIn content where possible. These should feel raw and authentic, not polished.]

> "[Quote 1]"
> "[Quote 2]"
> "[Quote 3]"
> "[Quote 4]"

---

#### Buying Decision Process

[How this person evaluates and decides. 4–6 decision filters — the questions they ask themselves internally before committing.]

**1. [Filter Name]**
- [Question they ask / risk they're evaluating]

---

#### Motivations

**Professional:**
[Career goals, performance metrics, what they're trying to prove at work]

**Personal:**
[What they want from their life and work beyond the job title]

**Deep driver:**
[The underlying thing — the emotional core of what they want. One sentence.]

---

#### Influences

[What shapes their thinking and decisions:]
- Peers and communities
- Publications and media
- Metrics they track
- Internal stakeholders with power over them
- Events and forums they attend

---

#### Messaging Implications

[5–7 specific, actionable points on how to talk to this person effectively. What to lead with, what to avoid, how to frame the product, and what proof types matter most to them.]

---

#### Strategic Summary

[A sharp, direct synthesis of this person: what they actually need, what they're afraid of, and how to sell to them. 3–5 sentences. Be direct — don't hedge. This is the section another skill would read to quickly get oriented before writing copy or building a campaign.]

---

[Repeat the full persona structure for each buying committee member.]

---

## Part 6: Research Sources

[List URLs, review sites, forum threads, reports, and other sources consulted. Makes the document auditable and shows it's data-backed rather than assumed.]

- [Source 1 — what it contributed]
- [Source 2 — what it contributed]
```

---

## Calibration Notes

**Research before writing.** If you don't know something specific enough to be useful, research it rather than filling with generics. The fastest path to a useless document is writing "they care about ROI" without explaining what ROI means in their specific role and industry context.

**Buyer language is the prize.** The most valuable output of your research is the exact phrases buyers use to describe their pain. "I was drowning in manual reconciliation" is 10x more useful than "they struggle with inefficiency." G2 reviews and Reddit threads are the primary sources for this — use them.

**Triggers must be specific.** "Company is scaling" is not a trigger. "Just posted 3 AE job listings on LinkedIn" is a trigger. "CFO asked for channel attribution last week" is a trigger. The trigger event section should give Brandon something he can actually search for in Clay or LinkedIn Sales Navigator.

**Persona depth standard.** Follow the depth of the CEO Steve persona document at `~/Obsidian/04-Strategy/Personas/CEO Steve.md` as the quality bar. Every section should be as substantive as that document.

**Scoring rubric customization.** The 5 default scoring dimensions are a starting point. Customize them to be predictive for this specific client. Ask: what's the single best signal that an account is a Tier 1? That answer should appear in the rubric.

---

## Output

Save the completed document to:
```
~/Obsidian/01-Clients/<ClientName>/icp.md
```

Overwrite any existing content. After writing, confirm the file path and approximate word count.

If the client directory doesn't exist, create it before writing.
