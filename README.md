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

### Codex ([skill docs](https://developers.openai.com/codex/skills))

```bash
mkdir -p ~/.agents/skills && \
git clone https://github.com/alik-git/frontier-advisor-skill.git \
  ~/.agents/skills/frontier-advisor
```

### Claude Code ([skill docs](https://code.claude.com/docs/en/skills))

```bash
mkdir -p ~/.claude/skills && \
git clone https://github.com/alik-git/frontier-advisor-skill.git \
  ~/.claude/skills/frontier-advisor
```

Both hosts detect installed skills automatically. If the skill does not appear,
restart the agent.

## Use

- In Codex, mention `$frontier-advisor` or let Codex invoke it automatically.
- In Claude Code, run `/frontier-advisor` or let Claude invoke it automatically.

## Compatibility and model setup

The shared `SKILL.md` follows the Agent Skills standard. `agents/openai.yaml`
adds first-class Codex and ChatGPT UI metadata; Claude Code reads the shared
skill and ignores that optional host-specific file.

Choose a lower-cost main model and configure a stronger advisor through the
host. The skill prefers a native Advisor tool when available and otherwise uses
a stronger read-only subagent. Exact model names and settings vary, so none are
hard-coded here.

## License

MIT
