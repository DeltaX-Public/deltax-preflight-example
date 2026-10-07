# DeltaX Preflight external example

This independent repository exercises the [DeltaX Preflight](https://github.com/DeltaX-Public/deltax-preflight) pull request gate. Its default proposal contains one reviewed local action and one rejected public action, so the expected check result is `PASS_SINGLE`. No proposed action runs.

The workflow reads `.preflight/policy.json` and `.preflight/manifest.json` from the base branch, derives evidence for the exact proposal in a pull request, and runs a pinned public Preflight commit. The proposal is data only. A changed payload must stop for missing evidence; two reviewed local actions must stop for selection. See the [installation recipe](https://github.com/DeltaX-Public/deltax-preflight/tree/main/examples/github-agent-gate) to add this gate to another repository.

This is a bounded example of an owner-reviewed action menu. The manifest asserts facts about its listed payloads; it does not verify arbitrary external facts or authorize execution.

The positive pull request changes this description while keeping the reviewed proposal intact.

The workflow pins the commit published as the [v0.1.0 public preview](https://github.com/DeltaX-Public/deltax-preflight/releases/tag/v0.1.0).
