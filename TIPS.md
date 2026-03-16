# Tips & Lessons Learned

Practical advice from running this setup daily for real marketing work across multiple brands. These are patterns that emerged from actual use, not theory.

## The Memory System

**Retrieval triggers are the secret weapon.** The retrieval triggers section in CLAUDE.md is what turns passive documentation into active context. Without them, Claude has the information but doesn't know when to use it. With them, Claude automatically pulls in project guardrails when you ask for a tweet about your launch, without you having to say "remember to check the messaging constraints."

**Messaging guardrails prevent disasters.** If there's one section to get right, it's the messaging guardrails in your project files. Document what can't be said, what's embargoed, what needs caveats, and which channel each message should go through. Claude will respect these constraints in every piece of content it generates. The five minutes you spend writing "don't mention the partnership before Tuesday" will save you from the tweet you can't un-send.

**Use the glossary aggressively.** Every internal term, acronym, and nickname should be in the glossary. The payoff is that you can talk to Claude the way you talk to your team — shorthand, first names, abbreviations — and it just works. If you find yourself explaining a term to Claude, that's a glossary entry you're missing.

**Community intel is perishable.** Update `community-intel.md` after every community interaction — calls, Discord threads, Twitter spaces, Telegram chats. Stale community intel is worse than no community intel because Claude will generate content that responds to last week's concerns instead of today's.

## Working with Skills

**Let skills trigger naturally.** You don't need to say "use the cold-email skill." Just say "write me a cold email sequence for [audience]" and the skill activates. The skill descriptions are written as trigger patterns — Claude matches your intent to the right skill automatically.

**Product marketing context is the foundation.** Every other marketing skill references `product-marketing-context.md`. If that file is thin, every skill's output will be thin. Invest the time upfront — a thorough product context document is the single highest-leverage thing you can do.

**Run the product-marketing-context skill interactively.** Don't try to fill in the template manually by staring at blank fields. Tell Claude "let's set up my product marketing context" and let the skill guide you through a conversation. Claude will ask the right questions and you'll end up with better, more honest answers than if you tried to write marketing copy about yourself from scratch.

**Skills compose well.** After running a content strategy session, you can immediately say "now write the first blog post" and Claude carries the strategic context forward. The skills aren't isolated — they build on each other within a session.

## Content Generation

**Give Claude the "why" and let it figure out the "what."** Instead of "write a tweet about our product launch," try "we need to build anticipation for the launch without revealing the date — what angles work?" Claude's content is better when it understands the strategic intent, not just the deliverable format.

**Use the objections table.** The objections section in your product marketing context isn't just for sales. It's how Claude learns to write content that preemptively addresses skepticism. If your community pushes back on a claim, document the objection and the honest response. Claude will weave that nuance into content instead of writing tone-deaf puff pieces.

**Multiple entities work.** If you manage a personal brand alongside a company brand, the multi-entity structure in product-marketing-context actually works. Claude tracks which voice, audience, and guardrails apply to which entity. Just be explicit about which entity you're working on when you start a task.

**Anti-personas are underrated.** The anti-persona field ("who is NOT your customer") is one of the most useful things in the product marketing context. It stops Claude from writing content aimed at people you don't want to attract. If you're trying to reach institutional investors, not retail speculators, say so — Claude will adjust tone, complexity, and messaging accordingly.

## Workflow Patterns

**Start sessions with context checks.** When you start a new Cowork session, Claude reads CLAUDE.md automatically. But if you've updated memory files since the last session, tell Claude "check the latest community intel" or "review the project file for [project]" to make sure it's working with current information.

**Batch similar work.** Content generation is faster when you're in the same strategic headspace. Do all your social content in one session, all your email sequences in another. Context carries forward within a session, so the second piece of content benefits from the thinking that went into the first.

**Use Claude to update the memory files.** After a team meeting or community call, tell Claude "update community-intel.md with these notes: [paste your raw notes]." Claude will structure them into the right format. You don't have to maintain the files manually — Claude can maintain them from your rough inputs.

**Don't over-template.** These templates are starting points. If a section doesn't apply to your business, delete it. If you need a section that doesn't exist, add it. The structure should serve your workflow, not the other way around.

## Common Mistakes

**Skipping the product marketing context.** Everything downstream suffers. The quality difference between "Claude with context" and "Claude without context" is night and day. Don't skip it, don't half-ass it.

**Stale project files.** A project file with outdated messaging guardrails is actively dangerous. If timelines shift or embargoes lift, update the file. If you don't have time to update the file, at least tell Claude at the start of the session what's changed.

**Being vague in retrieval triggers.** "Read the project file when relevant" is useless. "When creating launch-related content, READ memory/projects/product-launch.md for messaging guardrails and embargo dates" is useful. Be specific about what triggers the retrieval and what Claude should look for in the file.

**Treating this as a one-time setup.** The initial setup gets you 70% of the value. The other 30% comes from keeping the context current. Community sentiment shifts, projects evolve, competitive landscape changes. The system is only as good as the information in it.
