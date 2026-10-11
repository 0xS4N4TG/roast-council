# roast-council

Four Claude Code subagents that roast your idea, each in its own context window, then hand you one verdict.

- **Skeptic:** assumes the idea already failed and works out why
- **Customer:** would they actually pay?
- **Competitor:** how would a rival crush you?
- **Investor:** does the math work?

Each one runs separately and only a summary comes back, so they don't just agree with each other.

## Install

Copy the four files from `agents/` into either location:

```
git clone https://github.com/0xS4N4TG/roast-council
cp roast-council/agents/*.md ~/.claude/agents/
```

- `~/.claude/agents/`: available in every project
- `.claude/agents/` inside one project: just that project (commit it to share with a team)

Claude Code picks up new files within a few seconds. If `~/.claude/agents/` didn't exist when your session started, restart the session.

## Use

Paste this into Claude Code, with your idea at the end:

> Use the skeptic, customer, competitor and investor subagents in parallel to roast this idea. Give each one only the idea, not the others' answers. Then combine their reports into one verdict: KILL, CHANGE or BUILD, the 3 biggest risks, and the 5 questions I should ask real customers this week.
>
> Idea: …

You get back one verdict, the three biggest risks and five questions to take to real customers.

MIT licensed.
