# HeyEddi CI Skills

[![skills.sh](https://skills.sh/b/HeyEddi-com/heyeddi-ci-skills)](https://skills.sh/HeyEddi-com/heyeddi-ci-skills)

Cursor agent skills for **[HeyEddi CI](https://ci.heyeddi.com)** — PR review policy, `eddi-ci.yaml`, failing Checks, and Spot runners (placeholder / fail-closed).

**Product:** [ci.heyeddi.com](https://ci.heyeddi.com) · **Policy docs:** [ci.heyeddi.com/docs#policy](https://ci.heyeddi.com/docs#policy)

**skills.sh:** [skills.sh/heyeddi-com/heyeddi-ci-skills](https://www.skills.sh/heyeddi-com/heyeddi-ci-skills)

**SSOT:** skills are authored in [`HeyEddi-com/heyeddi-skills`](https://github.com/HeyEddi-com/heyeddi-skills) (pack `heyeddi-ci-skills`). This repo is the **published skills.sh package** (mirror), not a second authoring tree.

## Install

```bash
npx skills add HeyEddi-com/heyeddi-ci-skills -a cursor -y --skill '*'
```

Pin a release:

```bash
npx skills add https://github.com/HeyEddi-com/heyeddi-ci-skills/tree/v1.2.0 -a cursor -y --skill '*'
```

Full product pack (design, handoff, human PR review, …):

```bash
npx skills add HeyEddi-com/heyeddi-skills -a cursor -y --skill '*'
```

## Pack (v1.2.0)

| Skill | Role |
|-------|------|
| `@heyeddi-ci-config` | Author `eddi-ci.yaml` from the live policy contract |
| `@heyeddi-ci-respond` | Reply to HeyEddi CI findings (not human review) |
| `@heyeddi-ci-fails` | Diagnose failing GitHub Checks |
| `@heyeddi-ci-runners` | PLACEHOLDER — `pipeline:` YAML only (Spot not executing) |
| `@heyeddi-ci-guide` | Commands, auth, feedback paths |

## Product honesty

- **No unauthorized merge** — agents need explicit **authorize merge** in the current turn
- **No structured FP API yet** — use PR debate / `support@heyeddi.com`
- **Runners fail-closed** — do not claim jobs ran
- **PR scratch** under `.heyeddi/docs/pr-*` is ephemeral / gitignored

## Hub maintainer

```bash
# from HeyEddi-com/heyeddi-skills
./scripts/publish-ci-pack-repo.sh --out /path/to/heyeddi-ci-skills --push
```
