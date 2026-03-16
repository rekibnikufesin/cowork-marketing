# Getting Started

This walks you through setting up the workspace from scratch. Budget 30-60 minutes for the initial setup. After that, maintenance is minimal — you'll update files as things change, not on a schedule.

## Step 1: Install the Plugin

Before filling in any templates, install the marketing-skills plugin so it's available during setup.

1. Open Claude Desktop > Settings > Plugins
2. Install from file: `plugins/marketing-skills.zip`
3. Restart your Cowork session with this folder selected

## Step 2: Run the Product Marketing Context Skill

This is the most important step. The product-marketing-context skill walks you through building a comprehensive profile of your product, audience, and competitive position.

In your Cowork session, tell Claude:

> "Let's set up my product marketing context"

Claude will trigger the `product-marketing-context` skill and guide you through a structured conversation covering:

- Product overview and category
- Target audience and personas
- Problems you solve and why alternatives fall short
- Competitive landscape
- Differentiation and objections
- Brand voice and customer language
- Proof points and goals

The output gets saved to `.agents/product-marketing-context.md`. This file is the foundation everything else builds on — every other marketing skill references it.

**If you manage multiple brands or entities**, the template supports multiple sections. Just tell Claude "I have a second brand to add" and it'll extend the file.

## Step 3: Fill In CLAUDE.md

Open `CLAUDE.md` and fill in:

**You:** Name, role, company, timezone, key accounts. This is so Claude knows who's talking and can reference your context accurately.

**People:** Your team members — names, nicknames, what they own. This lets you say "check with Mike about the timeline" and Claude knows who Mike is and what he's responsible for.

**Terms:** Internal acronyms and shorthand your team uses. This is the difference between Claude asking "what's a GA launch?" vs. knowing it's your General Availability launch on April 15th.

**Active Projects:** What's in flight right now, with status indicators and pointers to project detail files.

**Retrieval Triggers:** These are the instructions that tell Claude *when* to pull in deeper context. For example: "When creating launch-related content, READ memory/projects/product-launch.md for messaging guardrails." This is how you avoid Claude generating content that violates an embargo or gets a detail wrong.

**Preferences:** How you like to communicate. Claude reads these and adapts.

## Step 4: Set Up Your Glossary

Open `memory/glossary.md` and populate:

- **Acronyms:** Every abbreviation your team uses. Include context so Claude knows when each is relevant.
- **Internal terms:** The words your team invented or uses differently than the rest of the world.
- **Nicknames:** Maps casual names to full names and roles. This is surprisingly useful — you'll naturally say "Sam's handling the livestream" and Claude needs to know Sam is Samantha Chen, your community lead.
- **External partners:** Key relationships with enough context that Claude can reference them accurately in content.

## Step 5: Create Project Files

For each active project, create a file in `memory/projects/`. Use `example-project.md` as your template.

The most important section is **Messaging Guardrails**. This is where you document:

- What's safe to say publicly
- What's embargoed and until when
- What should be pushed through specific channels (main account vs. personal vs. partners)
- How to respond to common pushback
- Numbers or claims that need caveats

This is the section that saves you from a bad tweet. Take the time to fill it in properly.

## Step 6: Seed Community Intel

Open `memory/context/community-intel.md` and capture:

- Current community sentiment on active topics
- Who the key voices are and what they're saying
- Questions that keep coming up
- Content gaps — topics people need explained but nobody's covered well

This file should be updated frequently. After community calls, Discord sessions, or scanning Twitter/Telegram, drop the highlights in here. Claude uses it to make content timely and responsive.

## Step 7: Verify It Works

Start a fresh Cowork session with the folder selected. Try these to confirm everything's connected:

1. **Shorthand test:** Use a nickname or acronym from your glossary in a request. Claude should understand without asking.
2. **Guardrails test:** Ask Claude to write a tweet about a project with messaging restrictions. It should respect the guardrails from your project file.
3. **Context test:** Ask for content ideas. Claude should reference your audience, competitive landscape, and content gaps — not generic suggestions.
4. **Skill test:** Ask Claude to "audit my SEO" or "write a cold email sequence." The relevant marketing skill should activate automatically.

If any of these fail, check that your files are saved and that the Cowork session has the correct folder selected.

## Ongoing Maintenance

This isn't a set-it-and-forget-it system. The value scales with how current your context is.

**Update frequently:**
- `memory/context/community-intel.md` — after any community interaction
- `memory/projects/*.md` — when timelines, messaging, or status changes
- `CLAUDE.md` active projects table — when projects start, ship, or change priority

**Update occasionally:**
- `.agents/product-marketing-context.md` — when positioning, audience, or competitive landscape shifts
- `memory/glossary.md` — when new terms, people, or partners emerge

**Update rarely:**
- `CLAUDE.md` preferences — once it's right, it stays right
- Template structure — the structure works; the content is what changes
