# squirrel-proof 🐿️

A learning coach agent for brains that chase squirrels.

If you have ADHD, brain fog or forty open tabs, "just ask the AI" turns into reading confident walls of text you forget by dinner. squirrel-proof flips it: the AI gives you the map, you rebuild it from memory, and the agent won't let you skip that part.

## What it does
- **One tiny piece per reply.** One idea, a breadcrumb (`📍 topic › section › piece 2/5`) so you never lose your place, a short recap, then it stops.
- **Rabbit holes get parked, not chased.** Every question you ask gets tagged KEEP, LATER or SKIP, so you know what not to learn right now.
- **A map file per topic** holds the structure (tree, current position, a return stack for side quests), so your working memory doesn't have to.
- **Hands on per concept.** You type one command and predict the output before the next idea.
- **No analogies, no vague words.** Exact programs, exact data, small numbered diagrams that zoom instead of redrawing.
- **Finish gate.** "I get it" means you explain it back from memory, or you're not done.
- **Warm ups after breaks** and a small spaced repetition queue.
- **Modes:** explain a codebase, debug (your hypothesis first), TDD, refactor, and build mode (you drive, it types, and it marks your mistakes with hints instead of fixing them).

## Install (Claude Code)
```bash
git clone https://github.com/SwapnilChand/squirrel-proof
mkdir -p ~/.claude/agents
cp squirrel-proof/agents/learn.md ~/.claude/agents/
```
Then in Claude Code, tag `@learn` or switch to the agent and say what you want to learn.

It keeps its notes in a `.learn/` folder (context, goals, decisions, journal, learning-maps). It will create what's missing; `templates/learning-map.md` shows the map format.

Works as a system prompt in other tools too: paste `agents/learn.md` (minus the frontmatter) into your agent or custom instructions.

## Why it works
- Generating a map from memory beats rereading one, so the map file holds structure, never your understanding.
- Small wins every 20 to 30 minutes keep you in flow; the agent steps down when you say "idk" and up when you're breezing.
- Repeat definitions word for word (the Canon) so terms never drift.

## License
MIT
