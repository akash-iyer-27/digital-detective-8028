# Mission 5 — Numbers and Data

## 1. Task / Objective

The aim of this mission was to convert numbers between decimal, binary and hexadecimal by hand, verify the answers with Python, build a small number converter program, and explain how text is stored using encoding standards.

## 2. Work Completed

- Converted seven numbers by hand and showed the working.
- Checked the answers in the Python interactive environment.
- Wrote `number_converter.py` and tested it with three different numbers.
- Answered the questions about ASCII and text encoding.

## 3. Commands / Tools Used

| Command / function | Purpose |
|---|---|
| `python3` | Opened the Python interactive environment and ran my program. |
| `input()` | Asks the user to type a value and returns it as text. |
| `int()` | Converts text to an integer. `int("1010", 2)` reads the text as base 2 and `int("1F", 16)` as base 16. |
| `bin()` | Converts an integer to a binary string starting with `0b`. |
| `hex()` | Converts an integer to a hexadecimal string starting with `0x`. |
| `print()` | Displays results on the screen. |
| `ord()` | Gives the number (code) for a character. |

**Tools used:** Terminal, Python 3 and a text editor.

## 4. My Understanding

### Task 5.1 — Conversions by hand

| Question | Working and answer |
| --- | --- |
| Convert decimal 13 to binary. | Divide by 2 and note the remainders: 13 ÷ 2 = 6 r1; 6 ÷ 2 = 3 r0; 3 ÷ 2 = 1 r1; 1 ÷ 2 = 0 r1. Read the remainders from bottom to top: **1101**. |
| Convert decimal 25 to binary. | 25 ÷ 2 = 12 r1; 12 ÷ 2 = 6 r0; 6 ÷ 2 = 3 r0; 3 ÷ 2 = 1 r1; 1 ÷ 2 = 0 r1. Read from bottom to top: **11001**. |
| Convert binary 1010 to decimal. | Place values 8, 4, 2, 1: (1×8) + (0×4) + (1×2) + (0×1) = 8 + 2 = **10**. |
| Convert binary 1101 to decimal. | (1×8) + (1×4) + (0×2) + (1×1) = 8 + 4 + 1 = **13**. |
| Convert hexadecimal A to decimal. | In hexadecimal, A stands for 10. So the answer is **10**. |
| Convert hexadecimal 1F to decimal. | (1×16) + (F×1) = 16 + 15 = **31**. |
| Convert binary 1111 to hexadecimal. | 1111 in binary is 8 + 4 + 2 + 1 = 15, and 15 is F in hexadecimal. So the answer is **F**. |

### Task 5.2 — Python verification

| Expression tested | Result | Matches my manual answer? |
| --- | --- | --- |
| `bin(13)` | `'0b1101'` | Yes (1101) |
| `bin(25)` | `'0b11001'` | Yes (11001) |
| `int("1010", 2)` | `10` | Yes |
| `int("1101", 2)` | `13` | Yes |
| `hex(10)` | `'0xa'` | Yes (A is 10) |
| `int("A", 16)` | `10` | Yes |
| `int("1F", 16)` | `31` | Yes |
| `hex(15)` | `'0xf'` | Yes (1111 is F) |

Python adds a `0b` prefix to binary results and `0x` to hexadecimal results. These only show which number system the value is in, and are not part of the number.

### Task 5.3 — Number converter

`number_converter.py`:

```python
# Number converter: decimal to binary and hexadecimal
number = int(input("Enter a decimal number: "))

print("Binary:", bin(number))
print("Hexadecimal:", hex(number))
```

**How it works:** `input()` asks for a number and returns it as text. `int()` converts that text into a whole number. `bin()` turns the number into its binary form and `hex()` turns it into its hexadecimal form. `print()` shows both.

I ran it with `python3 number_converter.py` from this folder:

| Test number | Binary output | Hexadecimal output |
| --- | --- | --- |
| 10 | 0b1010 | 0xa |
| 25 | 0b11001 | 0x19 |
| 255 | 0b11111111 | 0xff |

### Task 5.4 — How is text stored?

- The ASCII code for uppercase **A** is **65**, and for lowercase **a** it is **97**. I checked this with `ord("A")` and `ord("a")`.
- A computer only stores numbers (bits), so it needs an encoding standard that says which number stands for which character. Without one, different programs could read the same bits as different letters.
- The rupee symbol **₹** is not part of basic ASCII, because ASCII covers only English letters, digits and a few symbols. UTF-8 can store it.

## 5. Difficulties Faced

No major difficulties

## 6. How I Resolved Them

Not applicable

## 7. Evidence / Files

- `mission-05-numbers-data/number_converter.py`: the working converter program.
- `mission-05-numbers-data/README.md`: this file, with the manual working, Python verification, test results and encoding notes.

## 8. Commit Details

- **Commit message:** `Build number converter and practise data representation`
- **Status:** Pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm the converter, the README and the commit are visible.