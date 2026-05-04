# CCP Architecture: Public Overview

Capability Constraint Protocol (CCP) evaluates whether a model response materially increases a user's harmful capability.

## Public Architecture

At a high level, CCP compares:

- The user's apparent starting capability.
- The response's contribution to practical capability.
- The degree to which the response preserves or removes actionable detail.
- Whether the response redirects toward safety.

## Monitor Types

- CJM-R: a rule-based monitor that uses structured capability-jump signals.
- CJM-L: a semantic monitor that reviews context and implicit capability transfer.

The public version does not disclose full scoring rules, private thresholds, calibration notes, evaluator prompts, or adversarial stress-test design.

## Safety-Preserving Outputs

CCP can recommend allowing benign content, degrading specificity, fragmenting risky synthesis, refusing, or hard refusing.

