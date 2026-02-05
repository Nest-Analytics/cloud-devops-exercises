Deliverables (What to submit)

Submit your Week 1 work in the cloud-devops-submissions repository under your personal branch in a folder named week-01/.

Your week-01/ folder must include:

notes.md (short write-up)

screenshots/ (evidence screenshots)

scripts/ (optional, only if you created any scripts)

commands.txt (commands you ran)

Suggested structure:

week-01/
  notes.md
  commands.txt
  screenshots/
  scripts/


Minimum evidence required:

terminal evidence of the mini exercise commands completing successfully

SSH connection evidence (connected to VM and ran whoami, hostname, pwd, ls)

evidence that the repo was cloned on the VM (ls inside the repo folder)

Submission is complete when you push your work to your branch and open a PR into main.

Checklist (Self-check before submitting)

I can explain “cloud” in one sentence.

I can explain IaaS vs PaaS vs SaaS.

I ran the Week 1 mini exercise commands and captured evidence.

I connected to a Linux VM using SSH and ran the basic identity commands.

I cloned the demo repo on the VM and opened its README.

My submission is in week-01/ in my branch, and I opened a PR to main.


# Acceptance Criteria

---

### `week-01/acceptance-criteria.md`

```md
# Week 1 – Acceptance Criteria (Marking Checklist)

A Week 1 submission is marked complete when the following are present in the student PR.

---

## Repository and structure
- Submission is in the `cloud-devops-submissions` repository.
- Student used their personal branch.
- Work is inside a `week-01/` folder.

Required files/folders:
- `week-01/notes.md`
- `week-01/commands.txt`
- `week-01/screenshots/`

---

## Cloud understanding (from notes.md)
The student includes short answers that show they understand:
- what “cloud” means in simple terms
- what IaaS is (and that a Linux VM is an IaaS example)
- what PaaS is (example: managed web app platform)
- what SaaS is (example: online software such as email/document tools)
- what DevOps means in this programme (building + running + deploying + maintaining)

---

## Linux basics evidence
In screenshots and/or `commands.txt`, the student shows successful use of:
- `pwd`
- `ls` or `ls -l`
- `mkdir` and `cd`
- `echo "..." > notes.txt`
- `cat notes.txt`

---

## VM and SSH evidence
Student shows:
- SSH connection command used (redact private key path if needed)
- successful connection to the VM
- output of:
  - `whoami`
  - `hostname`
  - `pwd`
  - `ls`

---

## Demo app clone evidence
Student shows:
- `git clone` was executed on the VM
- the repo folder exists (`ls`)
- they opened the README (`cat README.md`)

Running the app is not required for Week 1.

---

## Submission completeness
- Work is pushed to the student branch.
- A PR is opened into `main`.
- The PR description clearly states: `week-01/` is the folder to review.
