# [![Upptime](https://raw.githubusercontent.com/upptime/upptime.js.org/master/static/img/logo.svg)](https://upptime.js.org)

This repository is customized: keep **your** configuration (`.upptimerc.yml`), **README**, and **generated status data** (`history/`, `api/`, `graphs/`, …). Do not overwrite them with the demo repo [upptime/upptime](https://github.com/upptime/upptime/).

**Upstream updates** should only pull GitHub Actions under `.github/workflows/` (bug fixes, newer action versions).

Add the `upstream` remote once if missing:

```bash
git remote add upstream https://github.com/upptime/upptime.git
```

Sync workflows only:

```bash
git fetch upstream
git checkout master

# Optional: review workflow changes before applying
git diff HEAD upstream/master -- .github/workflows

git checkout upstream/master -- .github/workflows
git add .github/workflows
git commit -m "Sync .github/workflows from upptime/upptime"
git push origin master
```

If you edited any workflow files locally, inspect `git diff` before committing and re-apply changes as needed.
