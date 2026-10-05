# Git Standards

These standards apply to everyone working on BisonRides.

For how we write code, see [CODING_STANDARDS.md](CODING_STANDARDS.md).

## 1. General rules

- Plan before opening a branch. Talk through the approach on Discord or in the issue first.
- Never commit secrets. Use environment variables and keep `.env` in `.gitignore`. Provide a `.env.example`.
- You own the code you commit. If it breaks the pipeline or causes a bug, you fix it.

## 2. Branches

- `main` is always stable and deployable.
- `dev` is the integration branch. Issue branches split from `dev`.
- We merge `dev` into `main` rarely and carefully.
- One branch per issue. Name it `issue-number-short-description`.
  - Examples: `12-post-ride-form`, `31-seat-count-bug`, `5-readme`
- Do not let a branch fall more than one week behind `dev`. Rebase or merge `dev` often.

## 3. Commits

- Commit messages are short and in the present tense.
  - Example: `add max detour field to ride posting`
- Keep commits small and focused.
- No dead code, commented-out code, or leftover debug prints in commits.

## 4. Pull requests

- Every PR links to an issue (`Closes #12`).
- Every PR needs 2 approving reviews before merge.
- Do not review your own PR. Do not merge with failing checks.
- Keep PRs small. If it is over about 400 changed lines, consider splitting it.
- The PR description says what changed, why, and how to test it.
- Add screenshots for any UI change.
- A task is done once it is merged.

### PR checklist

- [ ] Linked to an issue
- [ ] Tests added or updated
- [ ] CI passes (lint, tests, SonarCloud)
- [ ] No secrets or debug code
- [ ] Docs updated if behavior changed
- [ ] PR checked by two reviewers

## 5. Code review

- Reviewers respond within 24 hours on weekdays.
- Review comments should be specific and kind. Use "I noticed..." or "Could you explain...".
- If the author cannot explain the code in review, it does not get merged.

## 6. CI/CD

- GitHub Actions runs on every PR: lint, tests, build.
- SonarCloud runs on PR. Fix new issues before merging.
- Trivy scan on PR.
- CD builds a Docker image and Render deploys it.
- Do not disable or skip a check to get a PR through. Ask for help instead.

## 7. Changing these standards

Anyone can propose a change by opening a PR on this file. We decide by team vote. Review the standards at the start of each sprint.
