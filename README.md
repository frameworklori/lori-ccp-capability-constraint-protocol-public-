# lori-ccp-capability-constraint-protocol

Capability Constraint Protocol (CCP) is an AI safety evaluation framework for detecting when an AI response may reduce the capability gap between a non-expert user and high-impact harm.

This public repository explains the framework at a high level. It intentionally excludes full scoring logic, adversarial stress tests, bypass-oriented examples, private evaluator prompts, and operational implementation details.

## What Problem This Solves

AI safety failures are often not about a single dangerous word. A response may be risky because it gives a user the missing bridge from vague intent to practical capability.

CCP evaluates that bridge. It asks whether a model response makes a non-expert materially more capable of causing serious harm.

## Why Keyword Filtering Fails

Keyword filters are brittle. They can miss paraphrases, multi-turn assembly, and benign-looking fragments that become risky when combined. They can also block harmless safety, policy, or defensive discussion just because sensitive terms appear.

CCP focuses on capability delta instead: how much the answer changes what the user can actually do.

## Core Concepts

- CCP: Capability Constraint Protocol.
- CJM-R: a rule-based capability jump monitor.
- CJM-L: a learned or semantic capability evaluator.
- LMR: Last-Mile Reduction.
- SD: Synthesis Density.
- TF: Trajectory Fit.
- SC: Synthesis Counter.
- Output Orientation Score.
- Expert Modifier.
- Agentic Pattern Score.

## Public Safety Boundary

This public repository only contains:

- High-level architecture.
- Simplified CJM-R explanation.
- Redacted evaluation schema.
- Non-operational examples.
- Ethics and limitations statements.

It does not contain:

- Full scoring rules.
- Sensitive thresholds or calibration notes.
- Full adversarial stress tests.
- Red-team trajectories.
- Evaluator prompts.
- Origin statements and license variants controlled outside the public layer.
- Real attack procedures.
- Operational harmful instructions.

## Response Modes

CCP maps evaluator concern into coarse response modes:

| Level | Public Description |
| --- | --- |
| L0 | Allow benign content |
| L1 | Reduce specificity |
| L2a | Degrade actionable detail |
| L2b | Fragment or separate risky synthesis |
| L3 | Refuse and redirect to safer alternatives |
| L4 | Hard refuse high-risk enablement |

Security Notice

This repository is designed for transparency and research understanding.

It is not a specification of enforcement boundaries.

Attempting to reverse-engineer safety behavior from this repository will result in incomplete and misleading conclusions, as critical components are intentionally omitted or abstracted.


## Public Redaction Policy

All public examples must be abstract and redacted. Use placeholders such as `[REDACTED_REQUEST]`, `[SENSITIVE_TARGET]`, and `[OPERATIONAL_DETAIL_REMOVED]`.

Public material must explain the safety framework without helping users bypass AI safety systems.
