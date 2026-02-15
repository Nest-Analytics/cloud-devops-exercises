# Week 2 – Optional Practice: Git Workflow (Fork, Branch, PR)

This is optional practice for extra confidence with Git and GitHub. You can submit it if you want.

---

## Objective
By the end of this practice, you should be comfortable with:
- forking a repository
- cloning to your laptop
- checking status and history
- creating a branch
- making and committing changes
- pushing to GitHub
- opening and merging a Pull Request (PR) in your own fork

---

## Repo to use
Fork this repository into your GitHub account:

https://github.com/helloSanmi/learn-repo.git

---

## Tasks

### 1) Fork the repository
- Open the repo link above.
- Click **Fork**.
- Confirm you now have the repo under your own GitHub account.

### 2) Clone your fork to your laptop
```bash
git clone <YOUR_FORK_URL>
cd <REPO_FOLDER_NAME>
````

### 3) Inspect the repository locally

Run:

```bash
git status
git log --oneline --max-count=10
```

### 4) Create a new branch

Use this naming format:
`feature/week2-git-practice`

```bash
git checkout -b feature/week2-git-practice
```

### 5) Make a simple change

Do one of the following (choose one):

* Update `README.md` by adding your name under a section called `Training student`
* Create a new file `week-02-git-practice.txt` and add 3 lines describing what you practised

Confirm the change is detected:

```bash
git status
```

### 6) Stage, commit, and push

```bash
git add .
git commit -m "Week 2: git practice update"
git push -u origin feature/week2-git-practice
```

### 7) Open and merge a Pull Request (PR) in your fork

On GitHub (in your fork):

* Open a PR from `feature/week2-git-practice` into `main`
* Merge the PR

### 8) Pull the latest main (after merge)

Back on your laptop:

```bash
git checkout main
git pull
```

---

## Optional evidence (if you want to submit)

If you choose to submit this optional practice, add it under:

`week-02/optional-git-practice/`

Include:

* `notes.md` (what you did and what you learned)
* `screenshots/` containing:

  * `git log --oneline` output
  * PR merged page in GitHub

Suggested structure:

```text
week-02/
  optional-git-practice/
    notes.md
    screenshots/
```
