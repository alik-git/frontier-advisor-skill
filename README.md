# Frontier Advisor

A portable Agent Skill for pairing a lower-cost executor model with a stronger
advisor model at important decision points.

The executor keeps ownership of the task: it reads files, runs tools, edits,
tests, and writes the final answer. The advisor is used only for judgment—such
as choosing an approach, resolving contradictory evidence, or reviewing a
consequential result.

## Design principles

- Orient with read-only evidence before asking for advice.
- Prefer a host's native advisor tool when one exists.
- Otherwise use one stronger, read-only subagent in the foreground.
- Send a compact, specific brief instead of an entire transcript.
- Skip trivial, mechanical, and directly reactive work.
- Switch the main model when frontier capability is needed throughout the task.

## What good advice should challenge

A useful consultation should change or confirm a consequential next action. It
should identify the weakest assumption, the missing evidence, the simplest safe
approach, or the acceptance gate that determines whether to continue. The
executor supplies counterevidence, verifies the advice against primary sources,
and retains ownership of execution and permissions.

## Install

Clone the repository, enter its root directory, then link that directory into
the user-level skill directory used by your agent.

### Codex

```bash
mkdir -p ~/.agents/skills
ln -s "$PWD" ~/.agents/skills/frontier-advisor
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
ln -s "$PWD" ~/.claude/skills/frontier-advisor
```

Claude Code installations with the native Advisor tool will use that path
instead of creating a subagent. Restart the agent if it does not discover the
new skill automatically.

## Model setup

Choose a capable lower-cost model as the main executor and configure a stronger
model as the advisor. Exact model names and configuration surfaces vary by host,
so the skill intentionally does not hard-code them.

## License

MIT
