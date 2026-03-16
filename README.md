# Marketing Content Cowork

A ready-to-use workspace for running marketing content operations through Claude's Cowork mode. Includes a structured memory system, product marketing context templates, and a comprehensive marketing skills plugin with 30+ specialized skills.

Built by [Will Button](https://x.com/0xWillButton) after running this setup daily for real marketing work across multiple brands.

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/cowork-marketing.git ~/cowork-marketing
```

### 2. Install the plugin

Open Claude Desktop, go to **Cowork > Customize > + > Upload plugin**, and select `plugins/marketing-skills.zip` from this repo.

### 3. Start a Cowork session

Open Cowork and select the `cowork-marketing` folder as your workspace. Then paste this prompt:

> I just cloned the marketing content cowork repo. Read GETTING-STARTED.md and walk me through the setup process. Start with Step 2 (I already installed the plugin).

Claude will read the setup guide, then walk you through filling in your product context, CLAUDE.md, glossary, project files, and community intel — interactively, one section at a time. Budget about 30-60 minutes for the first run.

## What You Get

Once setup is complete, every Cowork session with this folder starts with Claude already knowing your product, audience, team, terminology, active projects, and messaging constraints. No re-explaining. No generic output.

The CLAUDE.md file acts as persistent working memory. Retrieval triggers in that file tell Claude *when* to pull in deeper context — so when you ask for a tweet about your launch, Claude automatically checks your project file for messaging guardrails without you having to remind it.

The marketing-skills plugin adds 30+ specialized skills that activate contextually:

| Category | Skills |
|----------|--------|
| **Content** | Content strategy, copywriting, copy editing, social content |
| **SEO** | SEO audit, AI SEO, programmatic SEO, schema markup, site architecture |
| **CRO** | Page CRO, signup flow, onboarding, form optimization, popups, paywall/upgrade |
| **Email** | Email sequences, cold email |
| **Ads** | Paid ads strategy, ad creative generation |
| **Strategy** | Launch strategy, pricing, marketing ideas, competitor alternatives, A/B testing |
| **Revenue** | RevOps, referral programs, churn prevention, sales enablement |
| **Analytics** | Analytics tracking, free tool strategy |
| **Foundation** | Product marketing context setup |

Just ask for what you need — "write a cold email sequence," "audit my SEO," "plan my launch" — and the right skill loads automatically.

## Repo Structure

```
.
├── CLAUDE.md                          # Working memory — who you are, your team, active projects
├── GETTING-STARTED.md                 # Setup walkthrough (Claude reads this and guides you)
├── TIPS.md                            # Lessons learned from daily use
├── .agents/
│   └── product-marketing-context.md   # Deep product/brand context for content generation
├── memory/
│   ├── glossary.md                    # Internal terms, acronyms, nicknames
│   ├── projects/
│   │   └── example-project.md         # Template for active project context
│   └── context/
│       └── community-intel.md         # Community sentiment, content gaps
└── plugins/
    └── marketing-skills.zip           # 30+ marketing skills for Cowork
```

## Ongoing Use

See [TIPS.md](TIPS.md) for practical advice from daily use — retrieval triggers, guardrails, batch workflows, common mistakes, and what we learned the hard way.

## Requirements

- Claude Desktop with Cowork mode enabled
- A Claude Pro or Team subscription

## Credits

The marketing skills plugin is built on [Corey Haines' Marketing Skills](https://github.com/coreyhaines31/marketingskills), packaged as a Cowork plugin. Go give him a star.

## License

MIT — use it however you want.
