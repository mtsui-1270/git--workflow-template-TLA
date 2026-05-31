# Git Workflow Guide

> **Golden rule:** Never commit directly to `main`. Always work on a branch.

---

## The Everyday Loop

```
main
 └── your-feature-branch   ← you work here
      └── pull request      ← teammates review here
           └── merge        ← goes back into main
```

---

## Step-by-Step

### Starting a new task
```bash
git checkout main
git pull origin main
git checkout -b your-name/short-description
# Example: git checkout -b mariah/add-login-page
```

### Saving your work
```bash
git add .
git commit -m "Short description of what you did"
git push origin your-name/short-description
```

### Opening a Pull Request(PR)
1. Go to your repo on GitHub
2. Click **"Compare & pull request"**
3. Write a short description of what you changed
4. Tag a teammate to review
5. Wait for approval before merging

### After your PR is merged
```bash
git checkout main
git pull origin main
```

---

## Branch Naming
Use: `your-name/what-youre-doing`
- ✅ `mariah/add-login-page`
- ✅ `name/fix-nav-bug`
- ❌ `test`, `stuff`, `branch1`

---

## Merge Conflict? Don't Panic.
```bash
git checkout your-branch
git pull origin main
```
Git will mark conflicts like this in your file:
```
<<<<<<< HEAD
your version
=======
teammate's version
>>>>>>> main
```
Pick one version, delete the markers, save, then `git add .` and `git commit`.

---

## Quick Fixes
| Problem | Solution |
|--------|----------|
| "What branch am I on?" | `git branch` — the `*` one is yours |
| "My push was rejected" | `git pull origin your-branch` first, then push |
| "I committed to main by accident" | Don't push — ask a teammate |
