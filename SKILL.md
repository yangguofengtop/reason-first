---
name: reason-first
description: Apply first-principles reasoning to software requirements, bugs, performance problems, and design tradeoffs. Use when explicitly requested or when goals, constraints, and assumptions need clarification. Keep mechanical changes lightweight.
---

# Reason First

Start with verifiable facts, explicit goals, and necessary constraints. Build a model sufficient to choose a solution. First-principles reasoning does not require rebuilding from scratch or discarding established experience.

Scale depth to uncertainty and impact; do not force a written analysis, fixed checklist, or extra alternatives. Follow applicable workspace instructions. Analysis requests do not authorize code changes; implementation requests proceed through verification within the authorized scope.

## 1. Define the outcome

- Establish scope, current and desired behavior, and acceptance criteria. For new features, derive outcomes from scenarios and contracts. Maintainability, cost, and reliability can be goals; do not invent requirements or performance targets.
- Separate goals from proposed means. Test suggestions, but do not silently replace explicitly required technologies. When requirements conflict, explain the conflict and tradeoffs; do not claim that a design satisfies incompatible requirements.

## 2. Classify the evidence

- Distinguish facts, hard constraints, invariants, historical conventions, and untested assumptions. Check where constraints come from and when they apply. Existing behavior and conventions do not automatically define requirements; explicit project rules still apply.
- Inspect relevant source, contracts, callers, logs, and measurements as needed. Retain their environmental limits. Index summaries, isolated observations, and correlations alone do not establish a conclusion.

## 3. Model and test assumptions

- Decompose the problem into relationships sufficient to explain the outcome, such as state transitions or contributors to latency. Stop at a useful level; do not force every problem down to hardware or treat an example model as universal.
- Prioritize assumptions that could change the solution. Choose inexpensive checks that distinguish competing explanations. Attempt to reproduce bugs and trace failures; measure performance baselines and bottlenecks. When reproduction or measurement is unavailable, use existing evidence while preserving uncertainty.
- Resolve missing information independently first. Ask when an unresolved detail changes correctness, scope, or a consequential tradeoff. Use reasonable, reversible assumptions for other details and continue work independent of critical unknowns. Stop expanding investigation when evidence supports a decision and its verification.

## 4. Derive the solution

- Derive necessary capabilities from the goal, constraints, and model: what mechanism changes, why it should achieve the goal, and which invariants must hold. State how to test key predictions and what result would refute them.
- Compare alternatives only when meaningful tradeoffs exist. Choose by correctness, compatibility, and overall cost. Reuse, local changes, new components, and architectural changes are candidates to assess using evidence. The smallest sufficient solution is not necessarily the fewest lines of code. Change only what the goal requires.

## 5. Verify and converge

- Verify outcomes and relevant invariants, not a restatement of the implementation. Check original bug conditions and regressions; where feasible, show failure before the fix and success afterward. Compare performance against a baseline under comparable conditions, accounting for variability and resource costs. Run required project checks and scale additional verification to risk.
- Revise assumptions or the solution when checks fail; do not weaken valid acceptance criteria to fit the solution. Stop expanding once the goal and required checks are satisfied. Disclose unavailable verification, distinguish inference, simulation, and observation, and do not claim unmeasured gains.

Deliver a concise result, key rationale, verification evidence, and limitations that affect use. Do not expose a full internal reasoning transcript.
