**Team Template for Code Collaboration**

# Project Name

> One sentence describing what this project does and who it's for.

---------------------

## Table of Contents

- [What This Project Does](#what-this-project-does)
- [Tech Stack](#tech-stack)
- [Getting Started (Local Setup)](#getting-started-local-setup)
- [Git Workflow](#git-workflow)
- [Project Structure](#project-structure)
- [Common Issues](#common-issues)
- [Team](#team)

---------------------

## What This Project Does

Replace this with 2–3 sentences describing:
- What the app/tool does
- Who uses it
- What problem it solves

---------------------

## Tech Stack

| Layer      | Technology         |
|------------|--------------------|
| Frontend   | ex HTML/CSS/JS   |
| Backend    | ex Python/Flask  |
| Database   | ex SQLite        |
| Version Control | Git + GitHub  |

---------------------

## Getting Started (Local Setup)

Follow these steps **in order** the first time you set up the project.

### 1. Prerequisites

Make sure you have these installed before anything else:

- [ ] [Git](https://git-scm.com/downloads)
- [ ] [Node.js](https://nodejs.org/) (if applicable) — check with `node -v`
- [ ] [Python 3](https://www.python.org/) (if applicable) — check with `python3 --version`

### 2. Clone the Repository

```bash
git clone https://github.com/YOUR-ORG/YOUR-REPO.git
cd YOUR-REPO
```

### 3. Install Dependencies

```bash
# If using Node/npm:
npm install

# If using Python:
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

```bash
cp .env.example .env
```

Open `.env` and fill in any required values (ask a teammate if you're unsure what goes here).

### 5. Run the Project Locally

```bash
# Example for a Node app:
npm start

# Example for a Python/Flask app:
python app.py
```

Then open your browser to `http://localhost:3000` (or whatever port the app uses).

---------------------

## Git Workflow

> **The golden rule:** Never commit directly to `main`. Always work on a branch.

### The Everyday Loop

```
main
 └── your-feature-branch   ← you work here
      └── pull request      ← teammates review here
           └── merge        ← goes back into main
```

### Step-by-Step

#### Starting a new task

```bash
# 1. Make sure your local main is up to date
git checkout main
git pull origin main

# 2. Create a new branch for your task
git checkout -b your-name/short-description
# Example: git checkout -b sofia/add-login-page
```

#### Saving your work

```bash
# 3. Stage your changes
git add .                    # adds everything
git add filename.js          # OR add a specific file

# 4. Commit with a clear message
git commit -m "Add login form with email validation"

# 5. Push your branch to GitHub
git push origin your-name/short-description
```

#### Opening a Pull Request (PR)

1. Go to the repo on GitHub
2. Click **"Compare & pull request"** (it usually appears automatically)
3. Write a short description of what you changed and why
4. Tag a teammate to review
5. Wait for approval before merging

#### After your PR is merged

```bash
# Switch back to main and pull the latest
git checkout main
git pull origin main

# Delete your old branch (cleanup)
git branch -d your-name/short-description
```

---

### Branch Naming Convention

Use this format: `your-name/what-youre-doing`

| Good ✅                        | Avoid ❌         |
|-------------------------------|-----------------|
| `sofia/add-login-page`        | `test`          |
| `marcus/fix-nav-bug`          | `stuff`         |
| `priya/update-readme`         | `branch1`       |

---

### Commit Message Tips

Write messages like you're finishing the sentence: *"This commit will..."*

| Good ✅                                    | Avoid ❌              |
|-------------------------------------------|----------------------|
| `Add user authentication route`           | `stuff`              |
| `Fix broken link in navbar`               | `idk`                |
| `Update README with setup instructions`   | `asdfgh`             |

---

### Merge Conflict? Don't Panic.

A merge conflict happens when two people changed the same line of code. Here's how to fix it:

```bash
# Pull main into your branch to surface the conflict locally
git checkout your-branch
git pull origin main
```

Git will mark conflicts in your files like this:

```
<<<<<<< HEAD
your version of the code
=======
your teammate's version
>>>>>>> main
```

1. Open the file and decide which version to keep (or combine both)
2. Delete the `<<<<`, `====`, `>>>>` markers
3. Save, then `git add .` and `git commit`

When in doubt, talk to your teammate before overwriting their code.

---

## Project Structure

```
project-root/
├── README.md          ← you are here
├── index.html         ← main entry point (if web app)
├── app.py             ← main entry point (if Python)
├── src/               ← source code
│   ├── components/
│   └── styles/
├── static/            ← images, fonts, assets
├── .env.example       ← template for environment variables
├── .gitignore         ← files Git should never track
└── requirements.txt   ← Python dependencies (if applicable)
```

> Update this to match your actual project structure.

---

## Common Issues

**"I can't run the project — module not found"**
→ You probably skipped `npm install` or `pip install -r requirements.txt`. Run it again.

**"My push was rejected"**
→ Someone else pushed to the same branch. Run `git pull origin your-branch` first, resolve any conflicts, then push again.

**"I accidentally committed to main"**
→ Don't push yet. Ask a teammate — this is fixable. (The command is `git reset HEAD~1` but confirm before running it.)

**"I don't know what branch I'm on"**
→ Run `git branch`. The one with `*` next to it is your current branch.

---

## Team

| Name | Role | GitHub |
|------|------|--------|
|      |      |        |
|      |      |        |
|      |      |        |

---

*Last updated: May 2026*
