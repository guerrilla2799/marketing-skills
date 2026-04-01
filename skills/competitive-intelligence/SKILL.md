---
name: competitive-intelligence
description: Build a comprehensive competitive analysis and intelligence document for a B2B SaaS client. Use this skill when the user wants to research competitors, create a competitive landscape overview, build battle cards, analyze competitor positioning and pricing, identify differentiation opportunities, or populate a client's competitive.md file. Trigger on phrases like "competitive analysis for [client]", "research competitors", "who are [client]'s competitors", "build competitive intel", "update competitive.md", or any request involving competitive research for a fractional CMO client engagement.
---

# Competitive Intelligence Skill

Build a deep, research-backed competitive analysis document and write it to the client's `competitive.md` file in `~/Obsidian/01-Clients/[ClientName]/competitive.md`.

## What This Produces

A living competitive intelligence document covering:
1. Market Landscape Overview
2. Competitor Index (quick-reference table)
3. Feature / Capability Matrix
4. Per-Competitor Deep Dives
5. Pricing & Packaging Analysis
6. Win / Loss Themes
7. Differentiation Map
8. Positioning Opportunities
9. Battle Cards (one per Tier 1 competitor)
10. Intel Refresh Log

---

## Step 1: Gather Inputs

**Required minimum inputs:**
- Client name (to locate their folder at `~/Obsidian/01-Clients/[ClientName]/`)
- Client website URL
- Client LinkedIn company page URL

**Optional inputs (use if provided):**
- Known competitor list (names and/or URLs)
- Win/loss context, sales call themes, Gong insights
- Specific competitors to focus on or deprioritize
- Any other relevant context

**Always read the client's existing context files first:**
```
~/Obsidian/01-Clients/[ClientName]/CLAUDE.md
~/Obsidian/01-Clients/[ClientName]/context.md
~/Obsidian/01-Clients/[ClientName]/positioning.md  (if exists)
~/Obsidian/01-Clients/[ClientName]/icp.md          (if exists)
~/Obsidian/01-Clients/[ClientName]/messaging.md    (if exists)
```

Extract from these files: ICP, ACV, GTM motion, positioning claims, known competitors already mentioned, tech stack, PMF level.

---

## Step 2: Identify Competitors

**If the user provided a competitor list:** Proceed to Step 3. Confirm the list with a quick "I'll research these X competitors: [list]. Anything to add or remove before I start?"

**If no competitor list was provided:**
1. Research competitors using web search. Search for:
   - `"[client company] competitors"` and `"[client company] alternatives"`
   - `"[product category] software comparison"` on G2, Capterra, TrustRadius
   - `site:g2.com "[client company]"` to find their G2 profile and the "Alternatives" tab
   - LinkedIn for companies in the same category
   - Crunchbase for funding-stage peers in the same space
2. Build a proposed list of 5–8 candidates, organized by tier:
   - **Tier 1 (Direct):** Same ICP, same problem, same GTM motion — head-to-head competition
   - **Tier 2 (Adjacent):** Overlapping ICP or overlapping capability, but not identical
   - **Tier 3 (Indirect):** "Do nothing / status quo" or category-adjacent tools that lose deals to
3. Present the list to the user for verification before proceeding. Format:
   ```
   Here are the competitors I found. Please confirm, add, or remove before I research them:

   **Tier 1 (Direct):**
   - CompanyA (companya.com) — [one-line description]
   - CompanyB (companyb.com) — [one-line description]

   **Tier 2 (Adjacent):**
   - CompanyC — [one-line description]

   **Tier 3 / Indirect:**
   - Status quo / spreadsheets
   - [other]
   ```
4. Wait for user confirmation before proceeding to research.

---

## Step 3: Research Each Competitor

For each confirmed competitor, conduct deep web research. Cover all of the following:

### Primary Research Sources
- **Company website:** Homepage, product pages, pricing page (if public), about/team page
- **G2 / Capterra / TrustRadius:** Star ratings, review themes, pros/cons, user segments, feature ratings
- **LinkedIn:** Company size, headcount growth (are they scaling?), recent job postings (signals roadmap/priorities), executive team
- **Crunchbase / PitchBook:** Funding history, investors, last round amount and date
- **Pricing page:** Tiers, packaging logic, what's gated, trial/freemium availability
- **Case studies / customer stories:** Who they serve, outcomes they claim, logos they display
- **Recent news:** Acquisitions, product launches, executive hires/departures, layoffs
- **Reddit / community forums:** What real users say, complaints, switching reasons

### Per-Competitor Research Checklist
For each competitor, capture:
- [ ] Company overview (founded, funding, headcount, HQ)
- [ ] Core product positioning (tagline, hero claim, primary use case)
- [ ] ICP they target (industry, company size, buyer role)
- [ ] ACV signals (pricing tier ranges, deal sizes mentioned in reviews)
- [ ] GTM motion (PLG, SLG, channel, partner-led)
- [ ] Pricing model (per seat, usage-based, flat, tiered)
- [ ] Pricing ranges (if public or estimable from reviews)
- [ ] Key differentiators they claim
- [ ] Feature highlights and gaps vs. client
- [ ] Common praise themes from reviews
- [ ] Common complaints / weaknesses from reviews
- [ ] Recent strategic moves (last 90–180 days)
- [ ] Sales tactics observed (free trials, demos, aggressive outbound, etc.)

---

## Step 4: Synthesize and Write the Document

Write the full `competitive.md` file using the template in `references/competitive-template.md`.

**Synthesis guidelines:**
- Be honest and specific — avoid vague claims like "Company X has strong features." Name the features.
- For differentiation, apply April Dunford's framework: only count something as a differentiator if competitors genuinely lack it or are meaningfully weaker. Shared strengths are table stakes, not differentiators.
- For pricing, triangulate: pricing page + G2 reviews mentioning price + Glassdoor AE comp signals + deal size references in case studies.
- For battle cards, think like a sales rep: what does a rep need in a 30-second hallway conversation before a demo?
- Win/loss themes should reflect what's actually in context files, call notes, or client-provided intel — flag clearly if speculative.
- Positioning opportunities should be whitespace: claims no competitor is owning that align with the client's actual strengths.

---

## Step 5: Write the File

Write the completed document to:
```
~/Obsidian/01-Clients/[ClientName]/competitive.md
```

Overwrite if file exists (it may be empty or a stub). After writing, confirm the file path and give the user a quick summary:
- Number of competitors analyzed
- Top 2–3 differentiation opportunities identified
- Most dangerous competitor and why
- Recommended next step (e.g., share battle cards with sales, validate win/loss themes with Gong)

---

## Quality Standards

Every competitive.md should pass these checks before writing:
- [ ] Every competitor claim is sourced (from web research, reviews, or client-provided intel) — not invented
- [ ] Differentiators are genuine, not just features the client also has
- [ ] Battle cards are specific enough for a sales rep to use immediately
- [ ] Pricing section includes a clear "So what does this mean for how we price/position?" synthesis
- [ ] Intel Refresh Log has a concrete cadence and specific signals to watch
- [ ] "Do nothing / status quo" is represented as a competitive alternative
- [ ] The document reads as a strategic asset, not a feature spreadsheet

---

## Notes on Tone

This document is used for:
- Brandon's own strategic analysis and client advisory
- Feeding positioning and messaging work
- Briefing client sales teams

Write with precision and strategic clarity. Be direct about where the client is weaker than competitors — surface the truth, because hiding it doesn't help. Flag anything speculative clearly with `[ESTIMATED]` or `[UNVERIFIED]`.
