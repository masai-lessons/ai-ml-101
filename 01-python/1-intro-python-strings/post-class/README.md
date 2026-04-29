# Session 1.1 — Post-Class Assignments

> **Work through Set 1 + the mini-build.** Set 2 is bonus — try it if you want extra practice.
> **Tools:** Google Colab. One new notebook called `s1-1-homework.ipynb`.

---

## How to do these problems

1. Open Colab → New notebook → name it `s1-1-homework.ipynb`.
2. For **each problem**, create a new code cell.
3. **Try without peeking at the solutions** at the bottom. Sit with the problem before scrolling — confusion is the job.
4. If a problem feels impossible, write down *what you tried* and *where you got stuck*. Bring it to Session 1.2.
5. Save the notebook (it auto-saves to your Google Drive).

---

## Set 1 — Drill (10 problems)

These cover everything from class. Do them in order.

### 1. Print, math, types
Make Python print:
```
2025
40.5
True
```
…by computing each one with arithmetic (e.g. `print(2000 + 25)`).

### 2. Storing values
Create three variables:
- `name` — your name (a string)
- `age` — your age (an int)
- `is_learning_python` — `True`

Then print all three on one line, separated by commas.

### 3. Type detective
Predict what `type()` will return for each, then run it to check:
```python
print(type(100))
print(type(99.99))
print(type("99.99"))
print(type(True))
print(type("True"))
```
Write a one-line comment next to each `print` saying what you expected.

### 4. The +1 trap
Why does `"5" + 1` fail but `5 + 1` work? In a comment cell, write your answer in your own words, then write code that **fixes** `"5" + 1` to give you `6`.

### 5. Concatenation
Given:
```python
city = "Mumbai"
state = "Maharashtra"
```
Print: `Mumbai, Maharashtra` — using `+` only.

### 6. Length
Given `s = "Artificial Intelligence"`, print:
- The length of the string.
- The length without the space (hint: `replace`).

### 7. Indexing
Given `word = "FOUNDATION"`:
- Print the first character.
- Print the last character (use negative indexing).
- Print the 4th character (remember — Python counts from 0).

### 8. Slicing
Given `course = "AI ML 101"`:
- Print just `"AI"`.
- Print just `"ML"`.
- Print just `"101"`.
- Print the whole thing **reversed** (hint: `course[::-1]`).

### 9. Repeat
Print a separator line of 40 dashes. Then print the word `"WOW"` repeated 5 times.

### 10. Build a profile string
Use these variables:
```python
name = "Priya"
age = 22
city = "Pune"
```
Use an **f-string** to print exactly:
```
Priya, 22 years old, lives in Pune.
```

---

## Set 2 — String methods bonus (5 problems)

### 11. Username clean-up
Given `raw = "  Aisha_Khan_2025  "`, produce a cleaned version: no spaces around it, all lowercase. Print the result.

### 12. Capitalise a name
Given `name = "aisha mehta"`, print it as `"Aisha Mehta"`.
Hint: there's a built-in method called `.title()`. Try it.

### 13. Count vowels
Given:
```python
text = "neural networks are powerful"
```
Print the total number of vowels (a, e, i, o, u). Use `.count()` for each vowel and add them up.

### 14. Ban a word
Given `s = "I love Java a lot"`, replace `"Java"` with `"Python"` and print the result.

### 15. CSV row → labelled output
Given:
```python
row = "Aisha,22,Bangalore,AI Engineer"
```
Split it on the comma, then use f-strings to print:
```
Name: Aisha
Age: 22
City: Bangalore
Role: AI Engineer
```

### 16. The floating-point surprise
Run this and look carefully at the output:
```python
print(0.1 + 0.2)
```
In a comment, write **what you got** and **why** (one sentence — recall what we said in class). Then use `round()` to make the answer come out as `0.3`.

---

## Mini-Build — "Name Card Generator"

Build a small program that prints a formatted introduction card.

### Spec
1. Use these three variables (you can change the values):
   ```python
   first_name = "Ritesh"
   last_name = "Firodiya"
   city = "Bangalore"
   ```
2. Compute and store:
   - `full_name` — first + last (with a space between)
   - `initials` — uppercase initials with dots (e.g. `R.F.`)
   - `name_length` — length of `full_name` (including the space)
3. Print exactly this card using **f-strings** and `print()`:

```
========================================
       INTRODUCTION CARD
========================================
Name     : Ritesh Firodiya
Initials : R.F.
City     : Bangalore
Length   : 15 characters
========================================
```

### Constraints
- Use **at least one** f-string.
- Use **at least one** string method (`.upper()`, `.split()`, `.strip()`, `.replace()`, etc.).
- Use **`len()`** for the length line.
- Keep it under 15 lines of code.

---

## Bonus Mini-Build — "Cleaning a Messy Registration Entry" (optional)

> 🟡 **Optional.** Try it if Set 1 + the Name Card felt easy. This is a taste of what real-world data cleaning looks like — every concept you learnt today, working together on one messy string.

### The problem

You've received a single registration entry from a form submission. It's messy — extra spaces, inconsistent casing, the age came in as text:

```python
raw_entry = "  priya SHARMA | 22 | priya@masai.school | mumbai  "
```

Your job: clean it up, validate it, and print a tidy report.

### Spec
1. Strip outer whitespace from `raw_entry`.
2. Split it on `" | "` (pipe with spaces) to get four fields.
3. Clean each field:
   - `name` → strip + `.title()` → `"Priya Sharma"`
   - `age` → strip + convert to `int` → `22`
   - `email` → strip + `.lower()` → `"priya@masai.school"`
   - `city` → strip + `.title()` → `"Mumbai"`
4. Build two boolean checks:
   - `is_adult = age >= 18`
   - `has_at_sign = "@" in email`
5. Print a report using **f-strings**, exactly:

```
--- Cleaned Record ---
Name:  Priya Sharma
Age:   22 (Adult)
Email: priya@masai.school (Valid)
City:  Mumbai
```

(Use the words `Adult`/`Minor` and `Valid`/`Invalid` based on the booleans.)

### Constraints
- Use `.strip()`, `.split()`, `.title()`, `.lower()`, `int()`, `in`, and at least one f-string.
- Keep it under 20 lines of code.
- If you can't get the conditional `Adult/Minor` text working, hardcode it for now — we'll cover proper `if`/`else` in Session 2.2.

> 💡 **Why this matters:** This is exactly what the opening phase of every data-science task looks like — the data arrives messy, and you clean it before you can analyse it.

---

## 🛠️ Stuck? Visualise it

When code feels confusing, **see** it instead of staring at it.

| Tool | What it's for |
|------|----------------|
| 🔍 [**Python Tutor**](https://pythontutor.com/visualize.html#mode=edit) | Paste your code → hit "Visualize Execution" → step line-by-line and *see* variables update in memory. Best for: indexing/slicing surprises, type confusion. |
| 📖 [**Python docs — strings**](https://docs.python.org/3/tutorial/introduction.html#strings) | Authoritative reference for string slicing and methods. Bookmark this. |
| 📚 [**W3Schools — Python strings**](https://www.w3schools.com/python/python_strings.asp) | Cheatsheet style — quick lookup with examples. |
| 🐍 [**Python.org**](https://www.python.org) | The official Python homepage. |

> **Pro tip:** When you can't figure out why your code does what it does, paste it into Python Tutor *first* before asking anyone. 70% of the time you'll see the bug yourself.

---

## Reflection — write in a markdown cell

Answer these three honestly. They will sharpen what comes next.

1. **What clicked today?** One thing that made sense quickly.
2. **What's still fuzzy?** One thing you'd want me to re-explain in 1.2. Be specific — "the whole thing" doesn't help.
3. **What will you try on your own?** One small thing you want to play with in Colab this week. Doesn't have to be assigned.

---

## Preview — Session 1.2

**Title:** Core Python Data Structures — Lists & Tuples

So far we've stored *one* value at a time in a variable. But what if you have:
- A class of 60 students' names?
- Marks across 10 subjects?
- All the ingredients for a recipe?

Next class we move from **single values** to **collections** — `lists` (the everyday workhorse) and `tuples` (lists that don't change). You'll be able to store, access, slice, and update entire rows of data in one variable.

Come ready. Bring the questions you couldn't answer on your own.

---

<details>
<summary><b>Solutions — try first, then peek</b></summary>

### Set 1

```python
# 1
print(2000 + 25)
print(40 + 0.5)
print(1 == 1)

# 2
name = "Aisha"
age = 21
is_learning_python = True
print(name, age, is_learning_python)

# 3 — expectations
# int, float, str, bool, str

# 4 — quotes make it a string; you cannot add an int to a str
print(int("5") + 1)   # 6

# 5
city = "Mumbai"
state = "Maharashtra"
print(city + ", " + state)

# 6
s = "Artificial Intelligence"
print(len(s))                       # 23
print(len(s.replace(" ", "")))      # 22

# 7
word = "FOUNDATION"
print(word[0])     # F
print(word[-1])    # N
print(word[3])     # N

# 8
course = "AI ML 101"
print(course[0:2])     # AI
print(course[3:5])     # ML
print(course[6:9])     # 101  (or course[-3:])
print(course[::-1])    # 101 LM IA

# 9
print("-" * 40)
print("WOW" * 5)

# 10
name = "Priya"
age = 22
city = "Pune"
print(f"{name}, {age} years old, lives in {city}.")
```

### Set 2

```python
# 11
raw = "  Aisha_Khan_2025  "
print(raw.strip().lower())          # aisha_khan_2025

# 12
name = "aisha mehta"
print(name.title())                  # Aisha Mehta

# 13
text = "neural networks are powerful"
vowels = (
    text.count("a") + text.count("e") + text.count("i")
    + text.count("o") + text.count("u")
)
print(vowels)                        # 10

# 14
s = "I love Java a lot"
print(s.replace("Java", "Python"))   # I love Python a lot

# 15
row = "Aisha,22,Bangalore,AI Engineer"
parts = row.split(",")
print(f"Name: {parts[0]}")
print(f"Age: {parts[1]}")
print(f"City: {parts[2]}")
print(f"Role: {parts[3]}")

# 16
print(0.1 + 0.2)              # 0.30000000000000004
# Computers store decimals in binary; 0.1 and 0.2 can't be represented exactly,
# so the tiny errors add up. round() fixes it for display.
print(round(0.1 + 0.2, 1))    # 0.3
```

### Mini-Build — Name Card

```python
first_name = "Ritesh"
last_name = "Firodiya"
city = "Bangalore"

full_name = first_name + " " + last_name
initials = f"{first_name[0]}.{last_name[0]}.".upper()
name_length = len(full_name)

print("=" * 40)
print("       INTRODUCTION CARD")
print("=" * 40)
print(f"Name     : {full_name}")
print(f"Initials : {initials}")
print(f"City     : {city}")
print(f"Length   : {name_length} characters")
print("=" * 40)
```

### Bonus Mini-Build — Cleaning a Messy Registration Entry

```python
raw_entry = "  priya SHARMA | 22 | priya@masai.school | mumbai  "

# Step 1 + 2: strip and split
fields = raw_entry.strip().split(" | ")

# Step 3: clean each field
name  = fields[0].strip().title()        # "Priya Sharma"
age   = int(fields[1].strip())           # 22
email = fields[2].strip().lower()        # "priya@masai.school"
city  = fields[3].strip().title()        # "Mumbai"

# Step 4: validation booleans
is_adult     = age >= 18
has_at_sign  = "@" in email

# Step 5: report (using f-strings + ternary expressions)
adult_label  = "Adult" if is_adult else "Minor"
email_label  = "Valid" if has_at_sign else "Invalid"

print("--- Cleaned Record ---")
print(f"Name:  {name}")
print(f"Age:   {age} ({adult_label})")
print(f"Email: {email} ({email_label})")
print(f"City:  {city}")
```

> **Note:** The `"Adult" if is_adult else "Minor"` syntax is a *ternary expression* — a one-line if/else. Don't worry about it yet; we'll cover full `if`/`else` in Session 2.2. Hardcoding `Adult` is fine for now.

</details>
