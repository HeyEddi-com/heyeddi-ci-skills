# HeyEddi CI Skills

[![skills.sh](https://skills.sh/b/HeyEddi-com/heyeddi-ci-skills)](https://skills.sh/HeyEddi-com/heyeddi-ci-skills)

Badge populates after skills.sh indexes the first installs.

**Product-specific agent skills for [HeyEddi CI](https://ci.heyeddi.com)**, not a general CI toolkit. Use these when your GitHub App is HeyEddi CI: `eddi-ci.yaml`, PR findings, failing Checks, and Spot runners.

**Product:** [ci.heyeddi.com](https://ci.heyeddi.com) · **Policy docs:** [ci.heyeddi.com/docs#policy](https://ci.heyeddi.com/docs#policy)

**skills.sh:** [skills.sh/heyeddi-com/heyeddi-ci-skills](https://www.skills.sh/heyeddi-com/heyeddi-ci-skills)

**SSOT:** skills are authored in [`HeyEddi-com/heyeddi-skills`](https://github.com/HeyEddi-com/heyeddi-skills) (pack `heyeddi-ci-skills`). This repo is the **published skills.sh package** (mirror), not a second authoring tree.

For the broader open toolkit (design, handoff, human PR review, …), install the hub instead.

## Install

```bash
npx skills add HeyEddi-com/heyeddi-ci-skills -a cursor -y --skill '*'
```

Pin a release:

```bash
npx skills add https://github.com/HeyEddi-com/heyeddi-ci-skills/tree/v1.4.11 -a cursor -y --skill '*'
```

Full open toolkit (design, handoff, human PR review, …):

```bash
npx skills add HeyEddi-com/heyeddi-skills -a cursor -y --skill '*'
```

## Pack (v1.4.11)

| Skill | Role |
|-------|------|
| `@heyeddi-ci-config` | Author `eddi-ci.yaml` from the live policy contract |
| `@heyeddi-pr-respond` | Reply to all PR review feedback (human + HeyEddi CI) |
| `@heyeddi-ci-fails` | Diagnose failing GitHub Checks |
| `@heyeddi-ci-runners` | Spot: GHA overflow/always and sealed `pipeline:` jobs |
| `@heyeddi-ci-guide` | Commands, auth, feedback paths |
| `@heyeddi` | Router, working agreement, next step |
| `@heyeddi-setup` | Repo preferences |
| `@heyeddi-local-first` | Permission check for commit, push, PR, merge |
| `@pre-merge-gate` | Merge readiness |
| `@engineering-excellence` | Engineering and cost audits |
| `@heyeddi-product` | Backlog and product review |

## Product honesty

- **Merging**: below production the agent merges once `@pre-merge-gate --signoff` exits 0; a production merge takes **authorize merge** in the current turn
- **No structured FP API yet** — use PR debate / `support@heyeddi.com`
- **Runners**: Spot is shipped; claim a job ran only with Check or Spot evidence
- **PR scratch** under `.heyeddi/docs/pr-*` is ephemeral / gitignored

## Hub maintainer

```bash
# from HeyEddi-com/heyeddi-skills
./scripts/publish-ci-pack-repo.sh --out /path/to/heyeddi-ci-skills --push
```
