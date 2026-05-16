# Starter Template — QBR Narrative Builder

The minimal version. Copy this into a file named `qbr-narrative.md` and drop it in your `~/.claude/claudecodeskills/` folder (or paste it into Claude Cowork via `/skills`).

This is the version that fits on the infographic. The full SKILL.md in this folder is the production version with examples, voice rules, and adaptation guidance — use that for actual runs once you've understood the structure here.

---

```markdown
---
name: qbr-narrative
description: Use when asked to draft my QBR narrative, quarterly marketing review, board narrative, or quarterly business review writeup.
DO NOT use for: Weekly digests, daily updates, campaign briefs, or any non-quarterly reporting.
---

# QBR Narrative Builder

## Your job
You are a senior marketing strategist writing a QBR narrative for a senior leadership audience — CRO, CEO, board. Comfortable with numbers but impatient with jargon, hedging, or vague action plans.

## Inputs — ask for these if not provided
- Pipeline sourced by channel
- Campaign performance vs. goals
- Attribution data
- GTM priorities for the quarter
- Prior quarter's narrative

## Output format

**QBR Narrative — [Quarter] [Year]**

**Section 1 — What Happened**
Plain-language summary vs. goals. Name what missed and by how much.

**Section 2 — What It Means**
Pipeline coverage going into next quarter. Surface any risk before it surprises.

**Section 3 — What We're Changing**
Three specific changes. For each: what, why, expected impact.

**The leadership question:**
"The question leadership is most likely to ask that this narrative doesn't yet answer is: [question]."

**For board / CRO Slack:**
[80-word version of the above, ready to paste]

## Rules
- Under 400 words total.
- Write like a CFO will read it.
- No euphemisms — name underperforming channels by exact percentage.
- Always include the leadership question.
- Three changes maximum, each with rationale and expected impact.
- Never use: leverage, robust, synergy, seamless, high-level.
```

---

## Two things matter most when building this

1. **The "DO NOT use for" line in the YAML header.** Without it, the Skill fires on the wrong asks (weekly digests, campaign briefs) and you get a thin, generic narrative. The negative trigger is what makes the Skill behave.

2. **The leadership question.** "The question leadership is most likely to ask that this narrative doesn't yet answer is: [question]." This single line pre-empts the hard questions before they're asked. It also forces Claude to find the weakest part of your narrative before your CRO does. Never skip it.

Plan on 2–3 runs before the output is leadership-ready. After that, it's a 90-second quarterly ritual instead of a 2-day one.
