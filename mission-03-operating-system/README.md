# Mission 3 — Understand the Operating System

## 1. Task / Objective

The aim of this mission was to explore my operating system, look at running processes, check storage, understand absolute and relative paths and file permissions, and explain what an operating system is responsible for.

## 2. Work Completed

- Checked my operating system details, the active account, the available storage and a snapshot of system activity.
- Viewed the list of running processes and found the PID column.
- Moved between the project folder and a subfolder and observed how the path changed.
- Read the permissions of a file from my Mission 2 practice area.
- Filled in a table of operating-system responsibilities.
- Saved selected, privacy-safe output in `evidence/mission-03-os-output.txt`.

## 3. Commands / Tools Used

| Command | Purpose |
|---|---|
| `sw_vers` | Shows the macOS name and version. |
| `uname -srm` | Shows the kernel name, release and processor type. |
| `whoami` | Shows which account is currently active. |
| `df -h /` | Shows total, used and available storage in readable units. |
| `top -l 1 \| head -10` | Takes one snapshot of system activity and shows only the first lines. |
| `ps -ax -o pid,comm \| head -15` | Lists running processes with their PID and name. |
| `pwd` | Shows my current location. |
| `cd` | Moves between folders. |
| `ls -l` | Shows a file's permissions, owner and size. |

**Tools used:** Terminal and a text editor.

## 4. My Understanding

### Task 3.1 — Exploring my operating system

| Information explored | What it tells you | Your observation (privacy-safe) |
| --- | --- | --- |
| Operating system / system details (`sw_vers`, `uname -srm`) | Which OS and version the computer runs, and the kernel and processor type. | macOS 27.2.1 (build 26B131), running on a Darwin 27.2.0 kernel with an arm64 processor. |
| Current account identity (`whoami`) | Which user account the commands run as, which decides what I am allowed to do. | The active account is `[redacted]`. |
| Available and used storage (`df -h /`) | How much of the drive is used and how much is free. | The main volume is 926Gi in size, with 13Gi used and 716Gi available (2% capacity). |
| System activity snapshot (`top -l 1`) | A one-time view of CPU use, memory use and the number of running processes. | 669 processes in total (2 running, 667 sleeping), CPU 88.69% idle, and 15G of memory in use. |

### Task 3.2 — Processes

**What is a process?**
A process is a program that is currently running. When I open an app, the operating system starts a process for it and gives it CPU time and memory.

**What does the PID column represent?**
PID stands for process identifier. It is a unique number the operating system gives each process so it can track and control it.

**Two examples of processes on my computer:**
- `launchd` (PID 1), the first process on my Mac. It starts and manages other processes.
- `logd` (PID 535), a background process that collects system log messages.

### Task 3.3 — Paths and permissions

When I moved from the project folder into `mission-03-operating-system`, the path printed by `pwd` got longer by that folder name. When I went back with `cd ..`, it returned to the project folder.

**Absolute path:** the full address of a file or folder starting from the root `/`. It works from anywhere. Example: `/Users/[redacted]/digital-detective-8028/mission-03-operating-system`

**Relative path:** an address worked out from where I currently am. Example: from the project folder, `mission-03-operating-system/README.md`.

**Permissions:** I ran `ls -l` on `notes.txt` from my Mission 2 practice folder. The permission string was `-rw-r--r--`. The first character `-` means it is a normal file. For the owner the permissions are `rw-`, so the owner can read and write the file but cannot execute it. The next two sets (`r--` and `r--`) show that the group and other users can only read it. The file is 34 bytes. I did not change any permissions.

| Permission | Meaning | Example |
| --- | --- | --- |
| r — Read | Allows a file's contents to be read. | Opening a text file. |
| w — Write | Allows a file to be changed. | Editing a text file. |
| x — Execute | Allows a file to be run; on a directory, allows access and traversal. | Running a script. |

### Task 3.4 — Operating-system responsibilities

| OS responsibility | Your explanation | Example |
| --- | --- | --- |
| Process management | Decides which programs run, starts and stops them, and shares CPU time between them. | With 669 processes on my Mac, the OS switches the CPU between them so they all seem to run together. |
| Memory management | Gives each program the RAM it needs and keeps programs from using each other's memory. | Closing an app frees its memory for other apps. |
| Device management | Controls hardware such as the keyboard, display and Wi-Fi through drivers. | The OS sends the image to the display and takes input from the trackpad. |
| File management | Organises files in folders and handles creating, reading, writing and deleting them. | Saving a file puts it on the SSD under a path I can find later. |
| User interface / shell | Gives me a way to talk to the computer, either through graphics or typed commands. | The macOS desktop and the Terminal shell. |
| Security and permissions | Controls who can access files and actions, and protects the system. | My `notes.txt` has `rw-` for the owner, so only the owner can change it. |

## 5. Difficulties Faced

Several commands printed my computer username and device name, such as `whoami`, `pwd`, `ls -l` and the Terminal prompt itself. The assignment says not to publish these, so I could not paste the output straight into my evidence file. I also found the `top` output long and hard to read at first, because it prints many lines of numbers.

## 6. How I Resolved Them

I replaced my username and device name with `[redacted]` before saving anything, then searched my files with `grep` to check that neither name was left. For `top`, I used `top -l 1 | head -10` so I only got one snapshot and the first few lines, and I focused on the process count, CPU usage and memory lines.

## 7. Evidence / Files

- `evidence/mission-03-os-output.txt`: selected output from `sw_vers`, `uname`, `df`, `top`, `ps`, `pwd` and `ls -l`, with my username replaced by `[redacted]`.
- `mission-03-operating-system/README.md`: this file, with the tables for system information, permissions and OS responsibilities.

## 8. Commit Details

- **Commit message:** `Document operating system and file management`
- **Status:** Pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm the README, evidence file and commit are visible.