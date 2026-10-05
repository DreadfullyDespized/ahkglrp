# AGENTS.md

Short outline for agents. Process detail lives in CONTRIBUTING.md.

## What this repo is for

Dread's AutoHotkey v1 script for Green Leaf RP, a GTA V roleplay server. Public. Not made by or for the server's staff. TEST repo: Rig merges after a separate grader PASS plus local proof.

## What is allowed in this repo

- `AHKGLRP.ahk`, its changelog and docs.
- Checks and workflows once they land through a PR.

## What is NOT allowed

- Passwords or secrets in git (cleartext or otherwise documented in-repo); use env vars or a secret store.
- Code comments in added lines.
- Images outside a password-protected archive.
- Pushing to `master`, force-pushing, or merging without Dread's say-so.

## Prove a change

Run `python3 tools/checks/no_secrets.py` from the repo root (must print OK). For a docs-only change: confirm `AGENTS.md` still has every Required H2 (What this repo is for, What is allowed in this repo, What is NOT allowed, Prove a change, Pointers) and that README.md still matches usage. For script changes: load `AHKGLRP.ahk` in AutoHotkey v1 on a Windows box and smoke the hotkeys you touched.

## Grader and merge

Grader starts at FAIL. The person who wrote the change does not grade it. This is a TEST repo: after a separate grader PASS plus local proof, the owner seat merges (do not wait on hosted Actions when minutes are exhausted).

## Correction loop

No correction-loop doc yet — follow CONTRIBUTING.md.

## Landmines

- Never commit passwords/secrets, tokens, or personal machine paths as defaults → `tools/checks/no_secrets.py` / `no-secrets.yml`
- Never merge your own PR → grader ≠ doer; TEST owner merges after PASS
- Never add code comments in added lines → reviewers (no no_new_comments CI yet)
- Never skip the Required AGENTS.md headings → reviewers (no headings CI yet)

## Pointers

- Usage and environment: [README.md](README.md)
- Process: [CONTRIBUTING.md](CONTRIBUTING.md)
- CI checks in `.github/workflows/`: `no-secrets.yml` (`tools/checks/no_secrets.py`)
