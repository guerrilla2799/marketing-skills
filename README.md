# Marketing Skills for Claude Code

A curated collection of 27 Claude Code skills for B2B SaaS marketing — covering strategy, content, SEO, CRO, paid ads, sales enablement, and AI image generation.

## Skills

### Foundation
| Skill | Description |
|-------|-------------|
| `skill-creator` | Build and benchmark new Claude Code skills |
| `nanobanana2` | AI image generation (Gemini) with legible text, multi-resolution, green screen |
| `product-marketing-context` | Create foundational product/ICP/positioning context for other skills |

### Strategy & Planning
| Skill | Description |
|-------|-------------|
| `gtm-strategy` | Plan go-to-market motions and market entry |
| `content-strategy` | Plan content strategy and topic selection |
| `pricing-strategy` | Develop pricing tiers, packaging, and monetization models |
| `launch-strategy` | Plan product launches, feature announcements, and release strategy |
| `marketing-psychology` | Apply 70+ behavioral science mental models to marketing |
| `icp-builder` | Build research-backed ICP and buyer persona documents |
| `competitive-intelligence` | Build competitive analysis, battle cards, and positioning intel |

### Content & Copy
| Skill | Description |
|-------|-------------|
| `copywriting` | Write marketing copy for homepage, landing pages, pricing, and feature pages |
| `linkedin-posts` | Create LinkedIn-specific social content |
| `cold-email` | Write B2B cold outreach emails and follow-up sequences |
| `email-sequence` | Create automated email flows, drip campaigns, and lifecycle emails |
| `ad-creative` | Generate and scale ad creative — headlines, descriptions, and copy |
| `lead-magnets` | Create lead magnets for email capture and lead generation |

### SEO & Discovery
| Skill | Description |
|-------|-------------|
| `seo-strategy` | Plan and prioritize SEO work and execution |
| `keyword-research` | Identify target keywords and analyze search intent |
| `competitor-research` | Analyze competitor positioning, content, and backlinks |

### Conversion Optimization
| Skill | Description |
|-------|-------------|
| `page-cro` | Improve conversion rates on marketing pages |
| `form-cro` | Optimize lead capture, contact, and demo request forms |
| `landing-page-generator` | Build and optimize campaign landing pages |
| `ab-test-setup` | Plan, design, and implement A/B tests and experiments |

### Sales & Revenue
| Skill | Description |
|-------|-------------|
| `sales-enablement` | Create sales collateral, pitch decks, and objection handling docs |
| `paid-ads` | Manage Google, Meta, and LinkedIn ad campaigns |
| `customer-research` | Conduct and synthesize customer research |
| `revops` | Revenue operations, lead lifecycle, and marketing-to-sales handoff |

## Installation

### Install all skills
```bash
# Clone and copy to your Claude Code skills directory
git clone https://github.com/guerrilla2799/marketing-skills.git /tmp/marketing-skills
cp -r /tmp/marketing-skills/skills/* ~/.claude/claudecodeskills/
```

### Install a single skill
```bash
cp -r /tmp/marketing-skills/skills/<skill-name> ~/.claude/claudecodeskills/
```

### Register skills
After copying, create matching command files in `~/.claude/commands/` for each skill so they appear as slash commands.

## Sources

Skills in this collection are sourced and adapted from:
- [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) (MIT License)
- [kostja94/marketing-skills](https://github.com/kostja94/marketing-skills)
- Local custom skills (skill-creator, nanobanana2, icp-builder, competitive-intelligence)

## License

MIT
