# Luna Chat Coder — repository development protocol

## Purpose

Use this skill when developing or modifying a repository that adopts the Luna Chat Coder protocol. The goal is reliable, recoverable repository work: establish exact source state, work in the available local/sandbox environment first, validate changes, and use remote CI only when it provides a real capability or verification gap.

## Core workflow

1. Read `AGENTS.md` and repository-specific instructions before changing code.
2. Establish the exact Git commit/ref being worked on. Do not rely on an ambiguous or stale working tree.
3. Prefer the local or ChatGPT sandbox/container for source inspection, editing, tests, and builds when those capabilities are available.
4. Keep changes focused and preserve existing project conventions.
5. Run the narrowest useful tests first, then the project build and broader checks when appropriate.
6. Treat GitHub Actions as a remote verification/execution surface, not the default development environment.
7. If an Action fails, inspect the failed job, step, and logs before retrying. Fix the underlying cause when the failure is actionable.
8. Preserve durable state in commits, branches, PRs, and other repository artifacts so work can be recovered after a context or sandbox reset.
9. Before declaring completion, verify the final repository state and report what changed and what was validated.

## Remote Actions missions

Use Actions when a task needs a capability unavailable locally/sandboxed, such as a required remote environment, deployment, platform-specific execution, or a bounded file-generation/transport task. Keep the mission narrow and deterministic. Do not use repeated Actions runs as a substitute for debugging locally.

## Failure diagnosis

For a failed workflow, identify the exact failing job and step, inspect its logs and annotations, distinguish source/test failures from infrastructure failures, and only then decide whether to modify code, workflow configuration, or retry. Do not blindly rerun a failing workflow.

## Recovery

If a conversation or sandbox is interrupted, recover from the durable repository state: inspect the current branch/PR head and recent commits, compare the working goal with the repository state, and continue from the latest verified commit. Do not assume that an earlier in-memory workspace still exists.

## Downstream projects

A repository using this template may add its own `AGENTS.md`, skills, build commands, test commands, deployment rules, and technology-specific instructions. Those project-specific instructions take precedence where they conflict with this generic protocol.
