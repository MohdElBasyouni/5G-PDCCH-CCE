---

# Mohamed's Fork Workflow

## Repository Structure

- `origin` → My GitHub fork
- `upstream` → Original source repository

Check remotes:

```bash
git remote -v
```

---

## Update My Fork From Source

```bash
git fetch upstream
git merge upstream/main
git push origin main
```

---

## Pull Latest Changes Locally

```bash
git pull
```

---

## Push My Own Changes

```bash
git add .
git commit -m "Describe changes"
git push origin main
```

---

## Safety

`upstream` push is intentionally disabled.

Verify:

```bash
git remote -v
```

Expected:

```text
upstream DISABLED (push)
```

Never push directly to upstream.

---

## PR Workflow

Fetch a PR locally:

```bash
git fetch upstream pull/PR_NUMBER/head:pr-PR_NUMBER
git checkout pr-PR_NUMBER
```

Push PR branch to my fork:

```bash
git push -u origin pr-PR_NUMBER
```

Return to main:

```bash
git checkout main
```

