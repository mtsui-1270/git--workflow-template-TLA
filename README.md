# Git Workflow Guide

## The Core Commands

```bash
git status              # see what files you've changed
git add .               # stage all your changes
git commit -m "message" # save a snapshot with a description
git push origin main    # send it to GitHub
```

---

## Making Your First Commit to a Branch

```bash
# 1. Create and switch to a new branch
git checkout -b your-name/feature-name

# 2. Check what you've changed
git status

# 3. Stage your changes
git add .

# 4. Commit with a clear message
git commit -m "Initial commit: add login page"

# 5. Push the branch to GitHub
git push origin your-name/feature-name
```

---

## Everyday Loop (After Your First Commit)

```bash
# Make your changes, then:
git status              # what changed?
git add .               # stage it
git commit -m "..."     # save it
git push origin your-branch  # send to GitHub
```

---

## Good Commit Messages
- ✅ `"Add navbar with working links"`
- ✅ `"Fix broken login button"`
- ❌ `"stuff"`, `"changes"`, `"asdfgh"`
