# Git and GitHub Cheat Sheet

## 🧠 Overview

* **Git** is a version control system for tracking code changes.
* **GitHub** is a platform to host and collaborate on Git repositories.
* Repositories contain your project's folders, files, and version history.
* Git uses **branches** and **commits** to manage your work and history safely.

---

## 🔧 Git Basics

### What is Git?

Git is a **Version Control System (VCS)** that lets you:

* Save snapshots of your project over time
* Reference any past version
* Experiment safely using branches

> Git's motto: Never lose anything. Ever.

---

## 💾 Commits and States

### Git Tracks Files in 3 States:

* **Unstaged** – changed but not marked for saving
* **Staged** – marked to be saved
* **Committed** – officially saved to Git history

### Common Git Commands

```bash
git init                     # Start a Git repository
git status                  # Show file changes
git add filename            # Stage file for commit
git commit -m "message"     # Commit staged files
```

### Writing Good Commit Messages

Start with a **type** followed by a colon and a short description.

**Types:**

* `feat` – new feature
* `fix` – bug fix
* `test` – test-related code
* `docs` – documentation updates
* `refactor` – code improvements (non-feature/bug)

**Examples:**

* `feat: Add shuffle to deck`
* `fix: Resolve off-by-one error`
* `docs: Update usage section in README`

---

## 🔁 Git Workflow

### Creating a Git Repo

```bash
mkdir git_practice
cd git_practice
git init
touch README.md
echo "# Git Practice" > README.md
git add README.md
git commit -m "Initial commit"
```

### Committing Changes

```bash
git status                  # Check for changes
git add filename            # Stage specific file
git commit -m "your message" # Save to history
```

---

## ☁️ GitHub Basics

### What is GitHub?

GitHub hosts your Git projects **online** so teammates can collaborate.

* **Local repo** – on your machine
* **Remote repo** – hosted on GitHub

### Creating and Connecting a GitHub Repo

1. Go to GitHub > New Repository > Name it (no README)
2. Copy the SSH URL
3. In your terminal:

```bash
git remote add origin git@github.com:your-username/repo-name.git
git push -u origin main
```

### Helpful GitHub Commands

```bash
git remote -v                      # View connected remotes
git remote add origin [url]       # Connect local repo to GitHub
git push origin main              # Push local code to GitHub
git pull origin main              # Pull changes from GitHub
```

> ✅ You can make multiple commits before pushing them all at once.

---

## 🌱 Branching in Git

Branches let you experiment and develop features safely.

### Common Branch Commands

```bash
git branch                        # View branches
git branch feature_name           # Create a new branch
git checkout feature_name         # Switch to a branch
git checkout -b feature_name      # Create + switch to branch
git push origin feature_name      # Push branch to GitHub
git pull origin main              # Sync with latest main
```

---

## 🔀 Pull Requests (PRs)

* Used to merge changes from one branch into another (e.g., feature → main)
* Allows teammates to review your code before merging

### Typical PR Workflow

```bash
git checkout main
git pull origin main
git checkout -b feature_login
# Make changes
# Add and commit

git push origin feature_login
# Open PR on GitHub to merge feature_login → main
```

### After Merging

```bash
git checkout main
git pull origin main
```

---

## 🧪 Practice Exercise

1. Create a folder `git_practice`
2. `git init`
3. Create and edit a `README.md`
4. Commit changes
5. Make more changes
6. Commit again
7. Create GitHub repo and push
8. Create a new branch and push it
9. Open and merge a PR

---

## 🧠 Wrap-Up Review

* ✅ How do you create a Git repo locally?
* ✅ What makes a good commit message?
* ✅ What’s the difference between `git add` and `git commit`?
* ✅ Why do we use branches and PRs?

---

Happy Committing! 💻✨
