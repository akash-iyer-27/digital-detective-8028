# Mission 2 — Become Comfortable with the Terminal

## 1. Task / Objective

The aim of this mission was to use the command-line interface to inspect folders, create and manage practice files, understand flags and pipes, and explain what a package manager does.

## 2. Work Completed

- Practised nine basic Terminal operations and recorded what each one does.
- Created a `terminal-practice` folder inside this mission folder and practised safe file changes there.
- Compared a plain `ls` with `ls -lah` and explained the flags.
- Used a pipe to send a detailed listing to `head`.
- Checked whether Homebrew is installed and explained why package managers are useful.

## 3. Commands / Tools Used

| Command | Purpose |
|---|---|
| `pwd` | Shows the full path of the current folder. |
| `ls` | Lists files and folders in the current location. |
| `ls -l` | Lists files in a detailed format. |
| `cd` | Changes the current folder. |
| `mkdir` | Creates a new folder. |
| `touch` | Creates an empty file. |
| `cp` | Copies a file. |
| `mv` | Moves or renames a file. |
| `cat` | Displays the contents of a file. |
| `echo` with `>` and `>>` | Writes text to a file, replacing it (`>`) or adding to the end (`>>`). |
| `ls -lah` | Detailed listing with hidden files and human-readable sizes. |
| `\|` with `head` | Sends one command's output into another and shows only the first lines. |
| `brew --version`, `brew list` | Checks Homebrew and lists the packages it manages. |

**Tools used:** Terminal, text editor and Git.

## 4. My Understanding

### Task 2.1 — Basic Terminal operations

| Operation / command name | What it does | What I observed |
| --- | --- | --- |
| Current-directory display (`pwd`) | Prints the full path of the folder I am in. | It printed a path ending in `mission-02-terminal`, with my username shown as `[redacted]`. |
| Directory listing (`ls`) | Lists the files and folders in the current location. | It listed the files and folders in the mission folder. |
| Detailed listing (`ls -l`) | Lists the same items with permissions, owner, size and date modified. | Each item moved onto its own line with extra columns. |
| Change directory (`cd ..`) | Moves to the parent folder. | After `cd ..` the path no longer ended in `mission-02-terminal`. I was in the main project folder. |
| Create directory (`mkdir terminal-practice`) | Creates a new empty folder. | A new `terminal-practice` folder appeared in `ls`. |
| Create empty file (`touch empty.txt`) | Creates an empty file. | `empty.txt` appeared in the folder. |
| Copy file (`cp empty.txt empty-copy.txt`) | Makes a duplicate under a new name and leaves the original. | Both `empty.txt` and `empty-copy.txt` existed. |
| Move / rename file (`mv empty-copy.txt empty-renamed.txt`) | Changes the file's name or location. | `empty-copy.txt` disappeared and `empty-renamed.txt` appeared. |
| Display file contents (`cat empty.txt`) | Prints what is inside a file. | Nothing was printed, because the file is empty. |

### Task 2.2 — Safe file changes

Inside `terminal-practice` I created `notes.txt` with one line, added a second line, and displayed it with `cat` to confirm both lines were there. I then copied it to `notes-backup.txt` and renamed the backup to `notes-backup-renamed.txt`.

**What is the difference between replacing a file's contents and adding text to the end?**
Replacing (`>`) wipes what was in the file and writes the new text. Adding to the end (`>>`) keeps the old text and puts the new text after it. My first line survived because I used `>>` for the second.

**What is the difference between copying a file and moving a file?**
Copying makes a second file and keeps the original. Moving relocates or renames the file, so only one file exists afterwards.

**What information does the current-directory display provide?**
It shows exactly where I am in the folder structure, so I know which files my commands will affect.

**Why is a directory-listing operation useful?**
It shows what is in a folder, so I can check that a command did what I expected and find file names without guessing.

### Task 2.3 — Flags and pipes

A flag changes how a command behaves. I ran `ls` and then `ls -lah` in the main project folder.

- `ls` showed only the names of visible files and folders.
- `-l` switched to the long format, with permissions, owner, size and date for each item.
- `-a` included hidden items, such as `.git` and `.gitignore`, which plain `ls` did not show.
- `-h` made file sizes readable, such as `4.0K` instead of a number of bytes.

I then ran `ls -lah | head -5`. The pipe symbol `|` takes the output of the command on its left and passes it to the command on its right as input. Here `ls -lah` produced the full detailed listing, and `head -5` kept only the first five lines. I redacted the owner name in the evidence.

### Task 2.4 — Package managers

Homebrew: `Homebrew 7.0.6`

A package manager installs, updates and removes software from one place, so I don't have to download and set up each program by hand. It also keeps track of what is installed and handles the other programs a tool depends on. This keeps my tools consistent and easy to update or remove.

## 5. Difficulties Faced

No major difficulties

## 6. How I Resolved Them

Not applicable

## 7. Evidence / Files

- `terminal-practice/` folder in this mission folder, containing `empty.txt`, `empty-renamed.txt`, `notes.txt`, `notes-backup-renamed.txt`.
- `evidence/mission-02-terminal-output.txt`, containing selected command output with the username replaced by `[redacted]`.

## 8. Commit Details

- **Commit message:** `Complete Terminal and file management mission`
- **Status:** Pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm the files, README and commit are visible.