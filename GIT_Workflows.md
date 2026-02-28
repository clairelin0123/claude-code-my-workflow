# Common git workflows
---

## 1️⃣ Clone the Repository (First Time Only)

```bash
git clone https://github.com/username/project.git
cd project
```

This creates a local copy of the remote repository.

---

## 2️⃣ Create a Feature Branch

Always branch off `main` (or `develop`, depending on team setup):

```bash
git checkout main
git pull origin main
git checkout -b feature/my-new-feature
```

This keeps your work isolated.

---

## 3️⃣ Make Changes & Stage Them

After editing files:

```bash
git status          # See what changed
git add file.txt    # Stage specific file
git add .           # Stage everything
```

---

## 4️⃣ Commit Your Changes

```bash
git commit -m "Add: user login validation"
```

Good commit messages:

* Use present tense
* Be descriptive but concise

Example:

```
Fix: prevent crash on empty input
```

---

## 5️⃣ Push to Remote

```bash
git push origin feature/my-new-feature
```

---

## 6️⃣ Open a Pull Request (PR)

On platforms like:

* GitHub
* GitLab
* Bitbucket

Create a Pull Request (PR) to merge your branch into `main`.

Team members review your code before merging.

---

## 7️⃣ Merge & Clean Up

After approval:

```bash
git checkout main
git pull origin main
git branch -d feature/my-new-feature
```

Optional (delete remote branch):

```bash
git push origin --delete feature/my-new-feature
```

---

# 🔁 Alternative Team Workflows

### 🔹 Git Flow

* `main` → production
* `develop` → integration branch
* `feature/*`
* `release/*`
* `hotfix/*`

Good for larger teams with release cycles.

---

### 🔹 Trunk-Based Development

* Short-lived branches
* Frequent merges to `main`
* Heavy CI/CD usage

Popular in modern DevOps teams.

---

# 🧠 Summary of the Typical Flow

```
main → feature branch → commit → push → pull request → merge
```

---


