# Actions missions

GitHub Actions should be used deliberately rather than as the default coding environment.

Use an Actions mission when remote execution, deployment, platform-specific behavior, or another capability gap makes it materially useful. Keep the workflow focused on the requested mission and make its inputs and outputs explicit.

For CI failures, inspect the failing job and step and read the relevant logs before changing code or rerunning the workflow. A rerun is appropriate for a transient/infrastructure failure; an actionable source, test, or configuration failure should normally be fixed first.

For deployments, make the build artifact and deployment target explicit and verify the resulting deployment state before declaring success.
