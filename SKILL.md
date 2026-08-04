---
name: frontier-advisor
description: "Use automatically for substantive multi-step work where a lower-cost executor benefits from stronger judgment: before committing to a consequential approach, after recurring or contradictory failures, when changing strategy, or before declaring risky work complete. Use for architecture, migrations, cross-repository or interface changes, security or safety questions, expensive operations, and difficult debugging. Skip trivial, mechanical, or directly reactive work, and skip tasks that need the strongest model on every turn."
---

# Frontier Advisor

Remain the executor. Use a stronger model for judgment, not labor; keep file
edits, commands, tests, and the user-facing answer in this session.

## Consult at decision points

1. Do enough read-only orientation to frame the problem with evidence.
2. Consult before committing to a consequential interpretation or approach.
3. Execute the resulting plan yourself.
4. Consult again only when evidence conflicts with the plan, the approach stops
   converging, or a consequential result needs an independent completion check.

Skip a consultation when the work is routine or the next action is dictated by
fresh tool output. If nearly every turn needs frontier capability, recommend
switching the main model instead of repeatedly consulting an advisor.

## Use the native path first

- If the host provides a native advisor tool, use it.
- Otherwise start one foreground, read-only subagent using a stronger available
  model and reasoning level. Do not run it in parallel with the decision it is
  reviewing.
- Reuse the same advisor thread for follow-ups. Do not spawn nested advisors.
- Tell a subagent advisor not to edit files, run state-changing commands, send
  messages, publish anything, or delegate further.

## Give a compact brief

When the host does not forward the transcript automatically, include only:

- the objective and acceptance criteria;
- the constraints and permission boundaries;
- exact evidence, relevant paths, errors, and verification results;
- the current interpretation or proposed approach;
- one specific question.

Ask for a decisive recommendation, key risk, missing evidence, and next action
in about 200 words. Do not send the whole conversation unless the native tool
does so automatically.

## Bound the spend

- Normally use at most two consultations: one for direction and one for a
  difficult correction or consequential completion review.
- Allow one extra reconciliation call only when primary evidence contradicts
  the advice.
- Save local work and gather verification before a completion review, but do
  not commit, push, deploy, or otherwise publish merely to prepare the review.

Give the advice serious weight. Override it only with primary-source evidence
or an empirical failure, and surface any unresolved conflict rather than
silently choosing a side.
