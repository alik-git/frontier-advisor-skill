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

## Choose for leverage, not workload

A large task does not automatically need advice. Consult where one judgment can
prevent substantial downstream rework. Strong signals include:

- an uncertain contract, source of truth, or system boundary;
- several plausible approaches with materially different consequences;
- an expensive, irreversible, externally visible, security-sensitive, or
  safety-sensitive action;
- contradictory evidence, recurring failure, or a stalled strategy;
- unclear acceptance criteria or an experiment without a stop condition;
- a change that crosses repositories, components, interfaces, or ownership;
- a consequential completion claim that deserves independent challenge.

Use the lower-cost executor for gathering facts and carrying out settled work.
The advisor should spend tokens on the decision that changes what that work is.

## Orient before asking

Before consulting:

- inspect enough primary evidence to describe the current state accurately;
- separate confirmed facts, interpretations, and unknowns;
- state what is fixed and what remains a genuine choice;
- identify permission, safety, publishing, and human-decision boundaries;
- preserve failed attempts and counterevidence that bear on the decision.

Do not present an invented rationale as fact or describe only the preferred
option. A leading brief invites confident rubber-stamping.

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
- failed attempts, counterevidence, and viable alternatives when relevant;
- the current interpretation or proposed approach;
- one specific question.

Ask for a decisive recommendation, key risk, missing evidence, and next action
in about 200 words. Do not send the whole conversation unless the native tool
does so automatically.

## Ask questions that change the next action

Choose the question with the highest decision value. Useful forms include:

- Which assumption in this plan is most likely to be wrong?
- What evidence would falsify the current interpretation?
- What is the smallest safe approach that satisfies the real contract?
- Which source of truth or boundary am I overlooking?
- What must remain unchanged for compatibility, safety, or user intent?
- What exact acceptance or stop criterion should govern the next step?
- Does the proposed test actually observe the risk it claims to cover?
- What is the cheapest decisive check before an expensive action?

Do not ask all of these at once. One precise question usually produces better
advice than a broad request for thoughts.

## Apply advice deliberately

- Translate the recommendation into a small execution plan before editing.
- Verify important advisor assumptions against primary sources or experiments.
- Keep all original permission and side-effect boundaries; advice is not new
  authorization to publish, deploy, message, purchase, or operate hardware.
- If advice conflicts with empirical evidence, name the conflict and gather the
  cheapest evidence that distinguishes the explanations.
- Reconsult when there is new evidence or a genuinely new decision. Repeating
  the same question with the same context is not progress.
- If rejecting material advice, record the evidence or constraint that overrode
  it instead of silently ignoring it.

## Review before publishing

Save local work and gather verification before a completion review, but do not
commit, push, deploy, or otherwise publish merely to prepare the review.

For a completion review, provide the actual diff or result, the tests or checks
run, the original acceptance criteria, and known caveats. Ask for the most
consequential missed failure, not a fresh implementation or a style rewrite.

An advisor's approval does not strengthen weak evidence. Confirm that the tests
exercise the claimed contract and that user-visible or operational claims were
verified at the correct boundary.

Give the advice serious weight. Override it only with primary-source evidence
or an empirical failure, and surface any unresolved conflict rather than
silently choosing a side.

## Avoid common failure modes

- Do not call an after-the-fact review "planning" if implementation already
  committed the task to an approach.
- Do not hand the advisor a tool-heavy execution loop, broad research project,
  or mechanical implementation task.
- Do not use advice as evidence for facts the advisor could not independently
  observe.
- Do not keep an experiment or debugging loop running without a baseline,
  acceptance gate, and stop-or-change-strategy condition.
- Do not add advisor councils, scoring systems, fixed call quotas, or elaborate
  orchestration unless the host genuinely requires them.
- Do not hard-code model names, host versions, project details, or private paths
  into this portable skill.
