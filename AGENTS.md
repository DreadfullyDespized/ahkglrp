# AGENTS.md

Short outline for agents. This repo has no CONTRIBUTING.md yet; the fleet process applies.

## What this repo is for

Dread's AutoHotkey v1 script for Green Leaf RP, a GTA V roleplay server. Public. Not made by or for the server's staff. Tier is not set yet: ask Dread before any merge.

## What is allowed in this repo

- `AHKGLRP.ahk`, its changelog and docs.
- Checks and workflows once they land through a PR.

## What is NOT allowed

- Secrets, tokens, or personal machine paths added as defaults.
- Code comments in added lines.
- Images outside a password-protected archive.
- Pushing to `master`, force-pushing, or merging without Dread's say-so.

## Prove a change

No check scripts on `master` yet. For a docs-only change: confirm `AGENTS.md` still has every Required H2 (What this repo is for, What is allowed in this repo, What is NOT allowed, Prove a change, Pointers) and that README.md still matches usage. For script changes: load `AHKGLRP.ahk` in AutoHotkey v1 on a Windows box and smoke the hotkeys you touched.

## Grader and merge

Grader starts at FAIL. The person who wrote the change does not grade it. ASK (ahkglrp) = Dread sets tier. Until then, no bot merges this repo.

## Correction loop

No correction-loop doc yet — follow CONTRIBUTING if present.

## Landmines

- Never merge without Dread setting the tier → ASK gate (no bot merge)
- Never add secrets, tokens or personal machine paths as defaults → reviewers
- Never add code comments in added lines → reviewers (no no_new_comments CI yet)
- Never skip the Required AGENTS.md headings → reviewers (no headings CI yet)

## Pointers

- Usage and environment: [README.md](README.md)
- Process: none in this repo yet; ask Dread
- CI checks: none on `master` yet (headings CI skipped — no Python check harness)
