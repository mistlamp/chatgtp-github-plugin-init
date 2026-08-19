# Recovery

The repository is the durable source of truth for completed work.

After a conversation, sandbox, or Codespace interruption:

1. Inspect the current branch and latest commit.
2. Inspect the relevant PR, workflow, or deployment state if the task involved one.
3. Compare the durable repository state with the requested goal.
4. Resume from the latest verified commit rather than reconstructing changes from memory.
5. Re-run the smallest relevant validation before continuing.

Avoid treating temporary workspace state as authoritative. Commits, PRs, workflow results, and deployment artifacts are the durable checkpoints.
