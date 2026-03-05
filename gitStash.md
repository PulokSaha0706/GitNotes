Use git stash to move them to the correct branch.

```bash
# 1. Stash changes on main
git stash push -u   # -u includes untracked files

# 2. Switch to the correct branch
git checkout login

# 3. Apply stash there
git stash pop       # brings changes to login branch

# 4. Commit
git add .
git commit -m "Work moved from main to login branch"
```
