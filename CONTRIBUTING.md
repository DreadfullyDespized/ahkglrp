# Contributing to ahkglrp

**Repo label: TEST** — All branches = TEST; the owner seat merges when the process below is complete. Verified work merges to master, and Dread tests master. Source of truth: fleet skill "Repo registry (PROD vs TEST)".
**Owner seat:** Rig (Stream Tools).
**Tracking:** GitHub issues.

## Process (required for every change, no exceptions)
1. Open a GitHub issue first: problem, evidence, acceptance criteria.
2. Branch `cursor/<issue#>-<slug>`. Never commit directly to `master`.
3. One scoped PR per issue. Body: `Closes #<issue>`, what, why, evidence (run links/logs/file:line), test plan + results, risk/rollback.
4. CI green (or local proof when Actions minutes are exhausted). Never skip hooks or checks; no force-push to shared branches.
5. Review by someone other than the author (grader ≠ doer); resolve all threads.
6. Merge: TEST → the owner merges when steps 1–5 are done.
7. After merge: confirm the issue closed and post-merge checks passed; update the tracking card with PR link + evidence.

Images committed to this repo must be inside a password-protected archive.

## Rules and what enforces them
| Rule (Dread) | Enforcer | Runs |
|---|---|---|
| No passwords/secrets in git (cleartext or otherwise documented in-repo) | `tools/checks/no_secrets.py` | `.github/workflows/no-secrets.yml` on every PR; same command locally |
