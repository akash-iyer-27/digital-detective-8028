# Mission 5 - Numbers and Data

## Task 5.1 - Convert Numbers by Hand

For this task, I converted numbers between decimal, binary and hexadecimal. I used repeated division by 2 for decimal to binary, and place values for the other conversions.

### 1. Convert decimal 13 to binary

I divided 13 by 2 again and again and noted each remainder.

13 / 2 = 6, remainder 1
6 / 2 = 3, remainder 0
3 / 2 = 1, remainder 1
1 / 2 = 0, remainder 1

Reading the remainders from bottom to top:

**Answer: 1101**

### 2. Convert decimal 25 to binary

25 / 2 = 12, remainder 1
12 / 2 = 6, remainder 0
6 / 2 = 3, remainder 0
3 / 2 = 1, remainder 1
1 / 2 = 0, remainder 1

Reading from bottom to top:

**Answer: 11001**

### 3. Convert binary 1010 to decimal

Each binary digit is multiplied by its place value (8, 4, 2, 1).

1010
= (1 x 8) + (0 x 4) + (1 x 2) + (0 x 1)
= 8 + 0 + 2 + 0

**Answer: 10**

### 4. Convert binary 1101 to decimal

1101
= (1 x 8) + (1 x 4) + (0 x 2) + (1 x 1)
= 8 + 4 + 0 + 1

**Answer: 13**

### 5. Convert hexadecimal A to decimal

In hexadecimal, the letter A stands for 10.

A = 10 x 1

**Answer: 10**

### 6. Convert hexadecimal 1F to decimal

In hexadecimal, F stands for 15, and the place values are 16 and 1.

1F
= (1 x 16) + (15 x 1)
= 16 + 15

**Answer: 31**

### 7. Convert binary 1111 to hexadecimal

I first changed the binary number to decimal.

1111
= (1 x 8) + (1 x 4) + (1 x 2) + (1 x 1)
= 8 + 4 + 2 + 1
= 15

15 is written as F in hexadecimal.

**Answer: F**

---

## Task 5.2 - Verify Using Python

After finishing the conversions by hand, I checked them in Python. I opened the interactive environment from Terminal with:

python3

### 1. Decimal to Binary

Expression: `bin(13)`
Output: `'0b1101'`

Expression: `bin(25)`
Output: `'0b11001'`

Both matched my manual answers. The `bin()` function converts a decimal number into binary, and the `0b` at the start shows that the value is binary.

### 2. Binary to Decimal

Expression: `int('1010', 2)`
Output: `10`

Expression: `int('1101', 2)`
Output: `13`

Both matched. The `int()` function converts text into a number, and the 2 tells Python the text is in base 2.

### 3. Decimal to Hexadecimal

Expression: `hex(10)`
Output: `'0xa'`

Expression: `hex(255)`
Output: `'0xff'`

The `hex()` function converts a decimal number into hexadecimal. The `0x` at the start shows that the value is hexadecimal, and 10 is A, which matches what I learned in Task 5.1.

### 4. Hexadecimal to Decimal

Expression: `int('A', 16)`
Output: `10`

Expression: `int('1F', 16)`
Output: `31`

Both matched my manual answers. Here the 16 tells Python the text is in base 16.

### 5. Extra check: Binary to Hexadecimal

Expression: `hex(int('1111', 2))`
Output: `'0xf'`

`int()` first turns the binary value into decimal and `hex()` then turns it into hexadecimal, so the answer is F.

### Verification Summary

All of my Python results matched my manual answers, so I am confident my conversions were correct.

---

## Task 5.3 - Build a Small Number Converter

I created a Python file called `number_converter.py`. It asks the user for a decimal number and then displays the binary and hexadecimal forms.

```python
# Number converter: decimal to binary and hexadecimal
number = int(input("Enter a decimal number: "))

print("Binary:", bin(number)[2:])
print("Hexadecimal:", hex(number)[2:])
```

### Python functions used

1. `input()` - Reads what the user types.
2. `int()` - Converts the typed text into a whole number.
3. `bin()` - Converts the number into binary.
4. `hex()` - Converts the number into hexadecimal.
5. `print()` - Shows the results on the screen.

### Test cases

I ran the program with `python3 number_converter.py` and tested three different numbers.

| Decimal input | Binary output | Hexadecimal output |
|---|---|---|
| 10 | 1010 | a |
| 25 | 11001 | 19 |
| 42 | 101010 | 2a |

### How the conversion functions work

`bin()` changes a number into its binary form and `hex()` changes it into its hexadecimal form. Both add a prefix (`0b` or `0x`) to the result. In my program I used `[2:]` to cut off the first two characters, so only the digits are shown.

---

## Task 5.4 - How Is Text Stored?

A computer can only store numbers, so text has to be converted into numbers first. A character encoding standard gives every letter and symbol its own number.

### 1. ASCII codes

- Uppercase A = 65
- Lowercase a = 97

I checked these in Python with `ord("A")` and `ord("a")`.

### 2. Why does a computer need an encoding standard?

Without an encoding standard, the computer would not know which number stands for which character. A standard makes sure every program and device reads the same numbers as the same text.

### 3. Example of a character outside basic ASCII

The Indian Rupee symbol (₹) is not part of basic ASCII, which only covers English letters, digits and a few symbols. UTF-8 can store it.

### What I understood

I practised converting numbers between decimal, binary and hexadecimal by hand and checked each one in Python. I also learned that computers store text as numbers, and that encoding standards such as ASCII and UTF-8 decide which number matches which character.