# Git Sample Flow

## 🚀 A Recommended Workflow for Teams

---

## 🏗️ Setting Up the Repository

1. **Initialize local repo and file structure:**

```bash
mkdir your-project-name
cd your-project-name
touch index.html style.css script.js
```

2. **Initial commit:**

```bash
git init
git add .
git commit -m "Initial commit"
```

3. **Create a new GitHub repo** (Do NOT initialize with a README)
4. **Link local to remote:**

```bash
git remote add origin git@github.com:your-username/repo-name.git
git branch -M main
git push -u origin main
```

5. **Invite collaborators** via GitHub > Settings > Collaborators
6. **Teammates clone the repo (no forking):**

```bash
git clone git@github.com:your-username/repo-name.git
```

---

## 🔁 General Workflow (For Each Feature)

### ✅ Start From `main`

```bash
git checkout main
git pull origin main
```

### 🌿 Create a New Branch

```bash
git checkout -b feature/branch-name
```

### 🛠 Do the Work

- Use `git status` and `git diff` frequently
- Add and commit changes regularly:

```bash
git add .
git commit -m "feat: [your message]"
```

### 🔄 Sync With Remote Main Before Pushing

```bash
git checkout main
git pull origin main
git checkout feature/branch-name
git merge main
```

> ⚠️ Resolve any merge conflicts, test your code

### 🚀 Push Feature Branch to GitHub

```bash
git push origin feature/branch-name
```

### 📬 Open a Pull Request

1. Go to GitHub
2. Open a PR to merge `feature/branch-name` → `main`
3. Write an informative description
4. Add teammates as reviewers
5. Submit PR

### 🧠 Code Review

- Teammates review, comment, and either **Merge** or **Request Changes**

### 🧹 After Merge

```bash
git checkout main
git pull origin main
```

If you're continuing on a branch:

```bash
git checkout feature/branch-name
git merge main
```

Ready for a new feature? ✅ Go back to step 1!

---

## 🧪 Optional: Deeper Code Review

If you want to **test your teammate’s PR code locally**:

1. Run:

```bash
git fetch
git checkout their-feature-branch
```

2. Review the code in your editor, test the app, run any checks
3. Leave a detailed review on GitHub

---

## 📝 Short & Sweet Summary

- Start on `main`, update it
- Create a branch for your work
- Push the branch when ready
- Partner reviews and merges
- Everyone pulls updated `main`

Repeat! 🌀

---

Happy Shipping! 🚢

