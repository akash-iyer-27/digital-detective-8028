
# Mission 0 — Setting Up My GitHub Repository

## 1. Task / Objective

The aim of this mission was to create a public GitHub repository with the correct name and set up the folder structure needed to complete all the missions in the Digital Detective assignment.

## 2. Work Completed

- Created a repository named `digital-detective-8028`, following the naming format given in the assignment.
- Created a local project folder with the same name.
- Created separate folders for all missions (Mission 00 to Mission 08), along with an `evidence/` folder.
- Added an empty `README.md` file to each mission folder.
- Created a main `README.md` file in the root folder.
- Added `number_converter.py` inside `mission-05-numbers-data/`.
- Created a public repository on GitHub and connected it to my local project.
- Pushed all the initial files to GitHub.

## 3. Commands / Tools Used

| Command | Purpose |
|---|---|
| `python3 --version` | Checked the installed Python version. |
| `git --version` | Checked the installed Git version. |
| `mkdir -p` | Created the required folders. |
| `touch` | Created empty files. |
| `ls -R` | Checked the folder structure and files. |
| `git init -b main` | Initialised the project as a Git repository. |
| `git config` | Set up my name and email for Git commits. |
| `git add .` | Added all files to the staging area. |
| `git commit -m` | Saved the changes with a commit message. |
| `git remote add origin` | Connected my local repository to GitHub. |
| `git push -u origin main` | Uploaded the files to GitHub. |

**Tools used:** Terminal, text editor and GitHub website.

**Version details:**
- Python: 3.14.7
- Git: 2.55.0

## 4. My Understanding

Through this mission, I understood how Git and GitHub work together. Git keeps track of changes made to files and maintains a history of previous versions. This makes it easier to check what has changed and recover older versions if needed.

GitHub allows me to store my repository online and access or share it whenever required.

I also understood the importance of organising a project properly. Keeping a separate folder for each mission makes it easier to manage files and find the work related to a particular task. It will also help me maintain a clear commit history as I complete the remaining missions.


## 5. Difficulties Faced

While trying to push my project to GitHub for the first time, I encountered an error in the terminal:

```bash
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/akash-iyer-27/digital-detective-8028.git'
```

At first, I wasn't sure why the push was failing. The error indicated that Git couldn’t find a local branch called main.

## 6. How I Resolved Them

I ran `git branch` and `git log --oneline` and found that my commits were on a branch called `master`, not `main`. The push failed because I was pushing a `main` branch that didn't exist locally. I renamed the branch with `git branch -M main` and ran `git push -u origin main` again, and the push worked.


## 7. Evidence / Files

- **GitHub Repository:** [digital-detective-8028](https://github.com/akash-iyer-27/digital-detective-8028)
- The repository contains all the mission folders, README files and the Python file created for Mission 05.
- The repository is public, and the initial commit is available on GitHub.

## 8. Commit Details

- **Commit message:** `Set up Digital Detective mission structure`
- **Status:** Successfully pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm that the folders and files were uploaded correctly.
