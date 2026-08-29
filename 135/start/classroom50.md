# CLI Student Guide

An end-to-end walkthrough of the `gh student` CLI (already installed in your Development Environment).

**The path:** [log in](#1-log-in) → [accept an assignment](#2-accept-an-assignment)
→ [clone and work](#3-clone-and-work) → [submit](#4-submit).
## Before you start

You must have already:

1. signed up for GitHub
2. ensured your GitHub username follows the required *labsection#-lastname-firstname* format
3. joined the CSE-UNR organization by clicking "accept" in the invitation email
4. opened a <strong>terminal window</strong> in your *development environment*

## 1. Log in

```sh
gh student login
```
<img width="1175" height="694" alt="gh_student_auth" src="https://github.com/user-attachments/assets/b9d5f803-ae04-4403-9fd7-92b0a9c2efa8" />

This runs `gh auth login` with the scopes you need. If you skip it, the next
command logs you in automatically. `gh student logout` mirrors `gh auth logout`.

## 2. Accept an assignment

```sh
gh student accept <org> <classroom> <assignment>
```
<img width="1175" height="694" alt="gh_student_accept" src="https://github.com/user-attachments/assets/680da4c9-4f8a-4e3b-b083-08d4d2510a2f" />

- `<org>` — your classroom's GitHub organization.
- `<classroom>` — the classroom your teacher set up (e.g., `cs-principles`).
- `<assignment>` — the assignment slug (e.g., `hello`).

Already accepted? The command reports `Assignment already accepted` and leaves
your existing repo (and your work) alone.

If accept fails, see
[Common `gh student accept` errors](Troubleshooting#common-gh-student-accept-errors)
in Troubleshooting.

## 3. Clone and work

Run the `git clone` command that `gh student accept` printed by pressing the `Enter` key. Edit, commit, and
push to your repository's default branch as usual.

## 4. Submit

From inside the cloned repository:

```sh
gh student submit
```

![gh student submit](images/gh_student_submit.gif)

This snapshots your current branch and pushes it as a new commit. The autograde
workflow runs automatically: it tags the commit `submit/<UTC-timestamp>-<short-sha>`,
grades it, and publishes a GitHub Release with your score a minute or two later.

> [!NOTE]
> On most assignments you can also `git push` directly — the result is the
> same. `gh student submit` exists mainly to pull any teacher-side updates to
> `.gitignore` and `.github/` from the template before pushing. (For a
> template-less assignment there's nothing to refresh, so it just commits and
> pushes.)
>
> Some assignments grade **only on submit** (your teacher will say so, and a
> plain push shows a passing check that says the push was not graded). There,
> `gh student submit` pushes the `submit/…` tag that triggers grading — or tag
> a commit yourself: `git tag submit/final && git push origin submit/final`.
> Any tag under `submit/` grades.
>
> Some assignments also name **milestone tags** (e.g. `phase1`, `phase2`,
> `complete` — your teacher will tell you). Push one to grade that commit:
> `git tag phase1 && git push origin phase1`. The graded result appears as a
> normal `submit/…` release.

When submit finishes, it prints two URLs:

- **Autograde** — the Actions tab, where the run appears in a few seconds.
- **Releases** — where the scored Release lands once grading finishes.

**Good to know:**

- **Every push grades (by default).** Each push to the default branch
  triggers one graded run, which tags and Releases the commit it ends on — so
  a push of several commits grades once, while the submissions page counts
  each of those commits. The first commit, from accepting, has nothing to
  grade and is skipped; the empty commit that opens your Feedback PR at accept
  time is likewise neither graded nor counted. The latest Release is always
  your most recent
  submission. On a **submit-only** assignment, only `gh student submit` (or a
  hand-pushed `submit/*` tag) grades; regular pushes save your work without
  grading it.
- **Pull after teacher-side workflow updates.** If your teacher changes the
  assignment's autograding trigger, a small commit lands in your repo. It is
  neither graded nor counted as a submission. Run `git pull` before your next
  push, or git will report a conflict.
- **History is preserved.** Submissions stack as commits; prior commits stay
  reachable for review.
- **No git config required.** Commits are authored with the `user.name` and
  `user.email` configured for your clone, so signed commits stay verified. In
  a shell with no git identity, submit falls back to your GitHub login and
  noreply email, so it still works.
- **Build artifacts are excluded.** Only tracked and untracked-not-ignored files
  are submitted.
- the `gh student accept <org> <classroom> <assignment>` command creates a repository at
  `<org>/<classroom>-<assignment>-<username>` from the assignment's template (or
  a new repository with a README and the autograding files if it's
  template-less), then prints a `git clone` command. The repository is
  **private** unless your teacher configured the assignment to create public
  repositories; in that case accept warns you first that your work will be
  visible to anyone on the internet.

<details>
<summary>What accept does, step by step</summary>

1. Auto-accepts any pending organization invitation.
2. Looks up the assignment in the classroom's published manifest.
3. Resolves the autograder workflow.
4. Creates your repository (a template copy, or a new
   README-initialized repository) — private unless the assignment opts into
   public repositories, in which case you're warned first.
5. Commits the setup files (`.classroom50.yaml` and the autograde workflow).
6. Opens the Feedback PR, when the assignment enables it.
7. Sets your repo role: `push` for an individual assignment, or `admin` for a
   group assignment (so a group founder can invite teammates).
8. Prints the `git clone` command.

</details>

## See also

- [`gh student` reference](gh-student) — every command and flag.
- [Troubleshooting](Troubleshooting) — debug flags and common errors.
