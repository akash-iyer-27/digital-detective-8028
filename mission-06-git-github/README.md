# Mission 6 — Git and GitHub

## 1. Task / Objective

The aim of this mission was to understand version control, stage and commit changes, create a branch, open a Pull Request and explain how the collaboration workflow works.

## 2. Work Completed

- Checked the repository status, staged a README file, committed it and viewed the commit history.
- Created a branch called `update-about` and added a "My Learning" section to the root `README.md`.
- Published the branch to GitHub and opened a Pull Request from `update-about` into `main`.
- **Pull Request status:** Open, not merged.
- Wrote a glossary of Git commands in my own words.
- Saved my notes in `mission-06-task.md`.

## 3. Commands / Tools Used

| Git operation | Purpose |
|---|---|
| `git status` | Shows which files are changed, staged or untracked. |
| `git switch -c update-about` | Creates the `update-about` branch and moves to it. |
| `git branch` | Lists branches and marks the current one. |
| `git add README.md` | Stages the README change for the next commit. |
| `git commit -m` | Saves the staged changes as a commit with a message. |
| `git log --oneline` | Shows the commit history in a short form. |
| `git log --oneline main..update-about` | Shows commits that are on `update-about` but not on `main`. |
| `git push` / `git push -u origin update-about` | Publishes the branch to GitHub. |
| `git switch main` | Moves back to the `main` branch. |

**Tools used:** Terminal, a text editor and the GitHub website.

## 4. My Understanding

### Task 6.1 — Basic Git workflow

| Git operation | What it does in my own words |
| --- | --- |
| Check repository status | Shows which files I have changed and which of them are ready to be committed. |
| Stage selected changes | Picks the specific changes I want to include in my next commit. |
| Create a commit | Saves the staged changes as a snapshot in the history, with a message that says what I did. |
| View commit history | Lists my earlier commits with their messages, so I can see how the project has changed. |

**Staging vs committing:** Staging (`git add`) chooses which changes will go into the next snapshot. Committing (`git commit`) actually saves that snapshot in the history. Staging lets me commit only the files I want, instead of everything at once.

### Task 6.2 — Branch

I created a branch called `update-about` and added a "My Learning" section to the root `README.md`. I checked `git status`, staged only the README, committed it with the message `Add My Learning section to root README` and pushed the branch to GitHub.

### Task 6.3 — Pull Request

I opened a Pull Request from `update-about` into `main` with a short description of the README change. I reviewed the changed file in the **Files changed** tab. The Pull Request is open and not merged, because I was not asked to merge it.

**What is a branch?** A branch is a separate line of work inside the same repository. I can make changes on it without touching `main`.

**What is a Pull Request?** A Pull Request is a request on GitHub to bring the changes from one branch into another. Other people can review the changes and comment before they are merged.

**Why are they useful when people work together?** Everyone can work on their own branch without breaking the main code. A Pull Request lets the team check changes before they are added.

### Task 6.4 — Git command glossary

| Operation | Command | One-line explanation |
| --- | --- | --- |
| Initialise a repository | `git init` | Turns a normal folder into a Git repository so changes can be tracked. |
| Check status | `git status` | Shows what has changed and what is staged. |
| Stage changes | `git add` | Marks changes to be included in the next commit. |
| Commit changes | `git commit -m "message"` | Saves the staged changes in the history. |
| View history | `git log --oneline` | Lists the previous commits. |
| Create or list branches | `git branch` | Lists the branches, and `git switch -c name` creates a new one. |
| Switch branches | `git switch name` | Moves me to another branch. |
| Publish changes | `git push` | Uploads my commits to GitHub. |
| Retrieve remote changes | `git pull` | Downloads new commits from GitHub and brings them into my branch. |

## 5. Difficulties Faced

When I tried to create the Pull Request, GitHub showed "There isn't anything to compare. main and update-about are identical." I had created the `update-about` branch and pushed it, but I had not yet added and committed the "My Learning" change, so the branch had no commit that `main` did not already have.

## 6. How I Resolved Them

I ran `git branch`, `git log --oneline` and `git log --oneline main..update-about` and saw that both branches pointed to the same commit and that the second command printed nothing. Then I edited the root `README.md`, staged it with `git add README.md`, committed it and pushed. After that, GitHub showed the changed file and I could create the Pull Request.

## 7. Evidence / Files

- Branch `update-about` and its Pull Request on https://github.com/akash-iyer-27/digital-detective-8028
- `README.md` in the root folder, with the "My Learning" section (on the `update-about` branch).
- `mission-06-git-github/mission-06-task.md`: my notes for this mission.
- `mission-06-git-github/README.md`: this file.

## 8. Commit Details

- **Commit messages:**
  - `Add My Learning section to root README` (on the `update-about` branch)
  - `Complete Git and GitHub collaboration mission` (this README and my notes, on `main`)
- **Status:** Pushed to GitHub. Pull Request status: Open, not merged.
- **Verification:** Checked on GitHub that the branch, the Pull Request and the commits are visible.