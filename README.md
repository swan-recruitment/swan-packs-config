# swan-packs-config

Public, **code-free** repository with reusable configuration for the Swan org:
- `.github/workflows/` — reusable CI workflows
- `.github/ISSUE_TEMPLATE/` — issue forms
- `.github/CODEOWNERS` — required reviewers for config changes
- `PULL_REQUEST_TEMPLATE.md` — standard PR template
- `VERSION.md` — human-readable version notes

> **No secrets, no application code.** Treat this as the public “source of truth” for standards & templates. Private repos pull from here via PRs (manually or automated).

## How private repos consume this

**Option A — Subtree (manual, keeps history)**
```bash
git remote add config https://github.com/<org>/swan-packs-config.git
git fetch config
git subtree add --prefix=.github config main --squash
# later updates
git fetch config
git subtree pull --prefix=.github config main --squash
