What Rebase Actually Does
Imagine this history:
```bash
A---B---C  (main)
     \
      D---E (feature)
```
You created a feature branch from commit B, and made commits D and E.

But meanwhile the main branch added commit C.

If you merge, history becomes messy:
```bash
A---B---C------M (main)
     \        /
      D------E
```
But rebase rewrites history:
```bash
A---B---C---D'---E' (feature)
```
your commits are re-applied on top of main.

## Real Workflow 
You are working on a branch:
```bash
A---B---C------M (main)
     \        /
      D------E
```
Step 1 — Update main
```bash
git checkout main
git pull origin main
```
Step 2 — Go back to your feature branch
```bash
git checkout feature/login
```
Step 3 — Rebase
```bash
git rebase main
```
