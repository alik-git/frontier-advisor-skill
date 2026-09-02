---
name: frontier-advisor
description: "Use only when the user explicitly asks for frontier-advisor, an advisor consultation, or a stronger-model review. Do not invoke automatically based on task complexity."
---

# Frontier Advisor

Remain the executor. Use a stronger model for judgment, not labor; keep file
edits, commands, tests, and the user-facing answer in this session.

## Invocation

Use this skill only when the user explicitly requests an advisor consultation.
Do not infer invocation from task complexity, risk, failures, or model choice.

## Consult at decision points

1. Do enough read-only orientation to frame the problem with evidence.
2. Consult before committing to a consequential interpretation or approach.
3. Execute the resulting plan yourself.
4. Consult again only when evidence conflicts with the plan, the approach stops
   converging, or a consequential result needs an independent completion check.

## Choose for leverage, not workload

A large task does not automatically need advice. Consult where one judgment can
prevent substantial downstream rework. Strong signals include:

- an uncertain contract, source of truth, or system boundary with several
  plausible interpretations;
- an expensive, irreversible, externally visible, security-sensitive, or
  safety-sensitive action;
- contradictory evidence, recurring failure, or a stalled strategy;
- unclear acceptance criteria or an experiment without a stop condition;
- a consequential completion claim that deserves independent challenge.

Use the lower-cost executor for gathering facts and carrying out settled work.
Skip advice when the next action is routine or dictated by fresh tool output. If
nearly every turn needs frontier capability, switch the main model instead.

## Use the native path first

- If the host provides a native advisor tool, use it.
- Otherwise start one foreground, read-only subagent using a stronger available
  model and reasoning level. Do not run it in parallel with the decision it is
  reviewing.
- Reuse the same advisor thread for follow-ups. Do not spawn nested advisors.
- Tell a subagent advisor not to edit files, run state-changing commands, send
  messages, publish anything, or delegate further.

## Give a compact brief

Orient with primary evidence first. When the host does not forward the
transcript automatically, include only:

- the objective and acceptance criteria;
- confirmed facts, interpretations, unknowns, and relevant exact evidence;
- constraints, permission boundaries, and what is fixed versus undecided;
- failed attempts, counterevidence, and viable alternatives when relevant;
- the proposed approach and one specific question.

Do not present an invented rationale as fact or only describe the preferred
option. Ask for a decisive recommendation, key risk, missing evidence, and next
action in about 200 words. Do not send the whole conversation unless the native
tool does so automatically.

## Ask questions that change the next action

Choose the question with the highest decision value. Useful forms include:

- Which assumption is most likely wrong, and what would falsify it?
- What is the smallest safe approach that satisfies the real contract?
- Which source of truth or boundary am I overlooking?
- What must remain unchanged for compatibility, safety, or user intent?
- What exact acceptance or stop criterion should govern the next step?
- Does the proposed test actually observe the risk it claims to cover?
- What is the cheapest decisive check before an expensive action?

Do not ask all of these at once. One precise question usually produces better
advice than a broad request for thoughts.

## Apply advice deliberately

- Translate the recommendation into a small plan and verify its important
  assumptions against primary sources or experiments.
- Keep all original permission and side-effect boundaries; advice is not new
  authorization to publish, deploy, message, purchase, or operate hardware.
- If advice conflicts with empirical evidence, name the conflict and gather the
  cheapest evidence that distinguishes the explanations.
- Reconsult when there is new evidence or a genuinely new decision. Repeating
  the same question with the same context is not progress.
- Give advice serious weight, but record the evidence or constraint when
  overriding it and surface unresolved conflicts.

## Review before publishing

Gather the actual diff or result, verification, acceptance criteria, and known
caveats before a completion review. Do not publish merely to prepare the review.

Ask for the most consequential missed failure, not a fresh implementation or a
style rewrite.

An advisor's approval does not strengthen weak evidence. Confirm that the tests
exercise the claimed contract and that user-visible or operational claims were
verified at the correct boundary.

## Avoid common failure modes

- Do not hand the advisor a tool-heavy execution loop, broad research project,
  or mechanical implementation task.
- Do not use advice as evidence for facts the advisor could not independently
  observe.
- Do not keep an experiment or debugging loop running without a baseline,
  acceptance gate, and stop-or-change-strategy condition.

Keep the skill portable: do not add advisor councils, scoring systems, fixed
call quotas, hard-coded model names, host versions, project details, or private
paths unless the host genuinely requires them.
