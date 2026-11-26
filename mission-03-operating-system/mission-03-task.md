# Mission 3 - Understand the Operating System

## Task 3.1 - Explore your operating system

| Information explored | What it tells you | What I observed |
| --- | --- | --- |
| Operating system/system details | Shows which OS the computer is using, its version and processor type. | My computer runs macOS 27.2.1 on an arm64 processor. I checked it using `sw_vers` and `uname -srm`. |
| Current account identity | Shows which user account is currently logged in. | I hid my username for privacy, but I could confirm that I was using a normal local account and not the `root` account. |
| Available and used storage | Shows how much storage is already used and how much is still free. | I checked the main `/` volume with `df -h /`. It showed 926Gi total, 13Gi used and 716Gi available. |
| System activity snapshot | Shows which programs are running and how much CPU and memory they are using. | I used `top -l 1 \| head -10` and saw 669 processes in total, with the CPU about 88% idle. I also used `ps -ax -o pid,comm \| head -15` to see the process list. |

---

## Task 3.2 - Understand processes

1. What is a process?
A process is just a program that is running on the computer. For example, when I open Chrome or VS Code, it starts running as a process and uses things like RAM and CPU.

2. What does the PID column represent?
PID means Process ID. Every running process gets its own number so the operating system can identify it and keep track of it.

3. Two examples of processes that may be running on your computer:
1. Background system process: `launchd` (PID 1), the first process on my Mac, which starts and manages other processes.
2. Background system process: `logd` (PID 535), which collects log messages from the system.

---

## Task 3.3 - Understand paths and permissions

1. What is the difference between an absolute path and a relative path?
- Absolute path: It gives the full location of a file starting from the root folder. It doesn't depend on which folder I am currently in.
  Example: `/Users/[redacted]/digital-detective-8028/mission-03-operating-system`

- Relative path: It gives the file location based on the folder I am already working in, so I don't have to type the full path.
  Example: `mission-02-terminal/terminal-practice/notes.txt` (when I am inside the main assignment folder).

2. Owner permissions check (`ls -l`):
I checked `mission-02-terminal/terminal-practice/notes.txt` using `ls -l` and got `-rw-r--r--` as the permission value. This means I can read and edit the file because I am its owner. Other users can only read it, and nobody has permission to execute it.

---

## Task 3.4 - Explain operating system responsibilities

| OS responsibility | My explanation | Example |
| --- | --- | --- |
| Process management | The OS manages the programs running on the computer and decides how they share the CPU. | `top` showed 669 processes on my Mac, and the OS shares the CPU between all of them. |
| Memory management | It keeps track of the RAM being used by different applications. | When I close a heavy Chrome tab, its memory is freed for other apps. |
| Device management | It helps the computer communicate with connected hardware devices. | Sending the image to the display and picking up the webcam when a video call starts. |
| File management | It helps store and organise files and folders so they are easier to find. | Saving `notes.txt` in `terminal-practice` and finding it again with `ls`. |
| User interface/shell | It gives us a way to interact with the computer, either through the screen or by typing commands. | Clicking folders in Finder and typing `ls` in Terminal both reach the same OS. |
| Security and permissions | It controls who can access or make changes to files and system settings. | `notes.txt` is `rw-r--r--`, so other users can read it but cannot change it. |