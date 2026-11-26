# Mission 4 — How Programs Run

## 1. Task / Objective

The aim of this mission was to create and run a simple Python program, and to compare how compilers and interpreters translate or execute programs.

## 2. Work Completed

- Created `hello.py`, a one-line Python program that prints "Hello from Python".
- Ran it from Terminal using Python 3 and confirmed the message appeared.
- Filled in a comparison table of compilers and interpreters and wrote a short explanation.

## 3. Commands / Tools Used

| Command / tool | Purpose |
|---|---|
| `echo` with `>` | Created `hello.py` and wrote the program line into it. |
| `cat hello.py` | Displayed the file to check its contents. |
| `python3 hello.py` | Ran the program using the Python 3 interpreter. |
| `print()` | Python function that displays text on the screen. |

**Tools used:** Terminal, Python 3 and a text editor.

## 4. My Understanding

### Task 4.1 — Running a Python program

`hello.py` contains one line:

```python
print("Hello from Python")
```

I ran it with `python3 hello.py` and the terminal displayed:

```
Hello from Python
```

Python read the file and carried out the instruction when I ran it, without a separate build step first.

### Task 4.2 — Compiler and interpreter

| Point | Compiler | Interpreter |
| --- | --- | --- |
| When translation / execution happens | The whole program is translated before it runs. | The program is read and executed line by line while it runs. |
| Typical output | A separate executable file (machine code) that can run on its own. | No separate file. The program's results appear directly as it runs. |
| One example | GCC for C, which turns C code into an executable. | The Python interpreter (`python3`). |
| One advantage | The finished program usually runs faster. | It is quicker to test and change code, because I can run it straight away. |

A compiler translates the whole source code into machine code before the program runs, and produces a file that can be run later without the source. An interpreter reads the code and carries out the instructions while the program is running. In my test, `python3 hello.py` ran the file straight away with no extra step. In practice, many languages mix both approaches. Python, for example, first turns code into bytecode and then runs that.

## 5. Difficulties Faced

No major difficulties

## 6. How I Resolved Them

Not applicable

## 7. Evidence / Files

- `mission-04-programs/hello.py`: the Python program.
- `mission-04-programs/README.md`: this file, with the program output and the comparison table.

## 8. Commit Details

- **Commit message:** `Compare compilers and interpreters`
- **Status:** Pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm `hello.py`, the README and the commit are visible.