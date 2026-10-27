# Reason First

A compact first-principles reasoning skill for software engineering.

Reason First helps a coding agent separate goals from proposed solutions, distinguish facts from assumptions, and derive changes from the relationships that actually determine the result. It works with your project's existing instructions and tools, without requiring a particular language, framework, or external service.

## What it does

1. Define the outcome and acceptance criteria.
2. Separate evidence, constraints, invariants, and assumptions.
3. Build a useful model and test assumptions that affect the decision.
4. Derive a sufficient solution and identify what would refute its predictions.
5. Verify the result and stop when the goal is met.

The depth follows the task: a label change stays a label change. It does not require a formal report, multiple alternatives, or a rewrite of existing architecture.

## Install

In Codex, ask the built-in skill installer:

```text
Use $skill-installer to install reason-first from
https://github.com/yangguofengtop/reason-first.
The skill is at repository path "."; use "reason-first" as its installation name.
```

For manual installation, clone this repository and place the `reason-first` directory in the user skills directory supported by your agent:

```bash
git clone https://github.com/yangguofengtop/reason-first.git
```

Keep `SKILL.md` directly inside that directory. The skill uses the `SKILL.md` format; `agents/openai.yaml` supplies Codex display metadata. Other agents may require their own installation or invocation steps.

## Use

```text
Use $reason-first to investigate why checkout is slow.
Establish evidence before choosing an optimization, then implement and verify it.
```

```text
Use $reason-first to evaluate this design. Identify constraints and key assumptions.
Analysis only; do not change code.
```

The skill's instructions are in English; they do not require English responses. Your language preferences and workspace instructions still apply.

## Scope

Useful for ambiguous requirements, debugging, performance work, and design tradeoffs. It preserves explicit technology choices and authorization boundaries. It does not replace domain knowledge, project rules, or actual testing, and it does not assume that existing conventions are wrong.

## Contributing

Issues and pull requests are welcome. For a proposed instruction change, describe the task, the observed decision, and how the change improves it. Prefer a focused correction over another general rule, and keep the core skill concise.

## License

[MIT](LICENSE).
