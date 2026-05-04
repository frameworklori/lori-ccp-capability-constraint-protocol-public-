# LORI-CCP Capability Constraint Protocol

Capability Constraint Protocol (CCP) is an AI safety evaluation framework for detecting when an AI response may reduce the capability gap between a non-expert user and high-impact harm.

This public repository presents the framework at a high level. It intentionally excludes sensitive implementation details, full scoring logic, adversarial stress tests, evaluator prompts, and operational configurations.

---

## Why This Repository Exists

This project is motivated by real-world events where gaps between intent and capability led to irreversible harm.

Incidents such as public mass violence — including school and public-space shootings — reveal a critical safety challenge:

The risk is not only in explicit harmful instructions,
but in subtle guidance that helps bridge the gap between abstract intent and practical capability.

In many cases, individuals do not begin with a complete plan.
They move from vague thoughts to actionable steps over time — often through fragmented information, multi-turn interactions, or seemingly harmless analysis.

This repository explores a different approach to AI safety:

Instead of focusing on keywords or isolated responses,
it focuses on whether an AI system reduces the **capability gap** for non-expert users.

The Capability Constraint Protocol (CCP) is designed to detect and constrain that transition —
before abstract intent becomes real-world execution.

This work does not attempt to analyze or reproduce any specific incident.
It exists to prevent future harm by improving how AI systems evaluate risk at the capability level.


## What Problem This Solves

AI safety failures are not always caused by explicit harmful instructions.

A response can be risky because it provides the missing bridge between:
- abstract understanding  
- and real-world capability  

CCP focuses on identifying that bridge.

It evaluates whether a model response materially increases a user's ability to act in ways that could lead to serious harm.

---

## Why Traditional Filtering Fails

Keyword-based filtering is insufficient because:

- It can be bypassed through paraphrasing or abstraction  
- It cannot detect multi-turn accumulation of knowledge  
- It often blocks benign educational or defensive discussions  
- It fails to recognize when harmless fragments combine into actionable capability  

CCP does not rely on surface-level signals alone.

Instead, it evaluates how much a response changes what a user can actually do.

---

## Core Principle: Capability Delta

The central idea behind CCP is **capability delta**.

Rather than asking:
> “Is this request dangerous?”

CCP asks:
> “Does this response reduce the effort, uncertainty, or decision-making required for a user to perform a high-impact action?”

This shift avoids reliance on intent inference and focuses on measurable impact.

---

## Conceptual Evaluation Dimensions

CCP evaluates responses across multiple dimensions of capability impact, including:

- Reduction of uncertainty in execution  
- Structural combination of knowledge into usable form  
- Progressive narrowing across multi-turn interaction  
- Accumulated synthesis over time  
- Output orientation (defensive vs enabling)

Detailed scoring methods and thresholds are intentionally not disclosed in this public repository.

---

## Framework Structure

The framework consists of two complementary layers:

### CJM-R (Rule-Based Layer)
A structured evaluator that identifies observable patterns associated with capability changes.

### CJM-L (Semantic / Learned Layer)
A higher-level evaluator designed to detect implicit, abstract, or non-obvious capability shifts that cannot be captured by rules alone.

The full interaction between these layers is not publicly disclosed.

---

## Response Modes

CCP maps evaluation outcomes into a small set of response behaviors:

- Allow benign content  
- Reduce specificity where risk begins to emerge  
- Limit or fragment synthesis that increases actionability  
- Redirect toward defensive or educational framing  
- Refuse responses that significantly enable harmful capability  

Exact thresholds and internal mappings are intentionally abstracted.

---

## Public Safety Boundary

This repository includes only:

- High-level architecture  
- Conceptual evaluation framework  
- Redacted evaluation schema  
- Non-operational examples  
- Ethics and limitations statements  

This repository does NOT include:

- Full scoring rules or calibration details  
- Adversarial stress test datasets  
- Red-team trajectories  
- Evaluator prompts or internal logic  
- Real-world operational procedures  
- Any content that enables harm or bypass of safety systems  

---

## Public Redaction Policy

All public examples follow strict redaction standards.

Sensitive elements are replaced with placeholders such as:

- `[REDACTED_REQUEST]`  
- `[SENSITIVE_TARGET]`  
- `[OPERATIONAL_DETAIL_REMOVED]`  

The goal is to demonstrate evaluation principles without exposing actionable pathways.

---

## Security Notice

This repository is intended for transparency and research understanding.

It is **not** a specification of enforcement boundaries.

Key components of the system are intentionally omitted, abstracted, or simplified.

Any attempt to reverse-engineer safety mechanisms from this repository will result in incomplete or misleading conclusions.

---

## Ethics and Limitations

CCP is designed to reduce capability transfer risks, not to determine user intent.

Limitations include:

- It does not fully prevent multi-system or cross-session accumulation  
- It cannot reliably distinguish expert vs non-expert users without external validation  
- It requires careful calibration to avoid over-restriction of legitimate research  
- Cognitive and narrative domains remain inherently harder to evaluate than physical ones  

The framework should be understood as a **risk-reduction layer**, not a complete solution.

---

## Research Use Only

This repository is provided for:

- Conceptual understanding  
- Research discussion  
- Framework-level analysis  

It is not intended for direct deployment without additional safeguards, private components, and controlled evaluation.

---

© 2026 LORI Ethical System — All Rights Reserved  
Capability Constraint Protocol (CCP)
