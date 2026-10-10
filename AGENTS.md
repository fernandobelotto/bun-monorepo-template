# AGENTS.md

<!-- BEGIN:github-workflow -->
## Workflow: issue → PR → merge → run locally

Every feature, bug fix, and architecture decision is tracked on GitHub so the repository keeps a clear record. This workflow overrides any older instruction in this repository (or in its skills) to commit or push straight to `main`. If the user asks for a different flow in a session, follow the user.

1. **Record it before coding.**
   - Create a GitHub issue with `gh issue create`: a clear title, the context/problem, the proposed solution or decision, and acceptance criteria (for bugs: steps to reproduce, expected vs. actual). Add a `bug`, `enhancement`, or `architecture` label when the repository has it.
   - Write the same details to `docs/issues/<issue-number>-<short-slug>.md`, linking the issue at the top. Update this file if the plan changes during implementation; it is committed together with the change.
2. **Implement on a branch.** Use the repository's branch naming convention if it has one, otherwise `<type>/<issue-number>-<short-slug>` (e.g. `feat/42-dark-mode`, `fix/57-crash-on-launch`). Follow the repository's commit conventions and reference the issue (`#42`) in commits.
3. **Open the PR, wait for CI, then merge** once the code is finished and the relevant local checks pass:
   - Push the branch and run `gh pr create` with a short summary, how to test, and `Closes #<issue-number>`.
   - If the repository has CI, wait for it with `gh pr checks --watch`. If a check fails, fix it on the same branch, push, and wait again until everything is green. If no checks are reported, go straight to merging.
   - Once CI is green, merge with `gh pr merge --squash --delete-branch` — no waiting for human review. Then update the local checkout: `git switch main && git pull`.
   - If the merge is blocked (conflicts, other required checks), fix the cause and merge. Do not bypass branch protection with `--admin` unless the user asks, and never leave a PR open without saying so.
4. **While CI runs, hand off for testing:**
   - Tell the user briefly what changed and how to test it, with links to the issue and PR.
   - Start the app on this machine using the repository's own run command (dev server, `make run`, build and launch the Mac app, iOS simulator, Expo, etc.) so it is ready to try, and say where to find it (URL, app window, simulator). If the project has nothing to run, say how to verify the change instead.
<!-- END:github-workflow -->
