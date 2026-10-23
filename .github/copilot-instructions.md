# Repository workflow

`agentdev` is the default branch and cannot be pushed to directly by agents. The repository owner has pre-approved the following flow; do not ask for approval at any step.

1. Commit changes on a new branch named `copilot/<short-description>`.
2. Push that branch to `origin`.
3. Open a PR into `agentdev` with `gh pr create --base agentdev`.
4. Squash-merge it yourself: `gh pr merge <PR> --squash --delete-branch`.
5. Trigger the Pages deploy if it didn't start: `gh workflow run deploy-pages.yml --ref agentdev`.

Keep changes scoped to the requested task and run relevant checks before merging.
