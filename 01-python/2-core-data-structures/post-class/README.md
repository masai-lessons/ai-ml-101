# Session 1.2 — Post-Class Assignments

> **Work through Set 1 + the mini-build.** Set 2 is bonus — try it if you want extra practice.
> **Tools:** Google Colab. One new notebook called `s1-2-homework.ipynb`.

---

## How to do these problems

1. Open Colab → New notebook → name it `s1-2-homework.ipynb`.
2. For **each problem**, create a new code cell.
3. **Try without peeking at the solutions** at the bottom. Sit with the problem before scrolling — confusion is the job.
4. If a problem feels impossible, write down *what you tried* and *where you got stuck*. Bring it to Session 2.1.
5. Save the notebook (auto-saves to your Google Drive).

---

## Set 1 — Drill (10 problems)

### 1. Build a list
Create a list called `subjects` with these five items: `"Maths"`, `"Physics"`, `"Chemistry"`, `"Biology"`, `"English"`. Print it.

### 2. Index practice
Using your `subjects` list:
- Print the **first** subject.
- Print the **last** subject (use negative indexing).
- Print the **third** subject (remember — Python counts from 0).

### 3. Slice it
Using your `subjects` list, print:
- The first three subjects.
- The last two subjects.
- Every other subject (hint: `subjects[::2]`).

### 4. Mutate it
Starting from `subjects = ["Maths", "Physics", "Chemistry", "Biology", "English"]`:
- Replace `"Biology"` with `"Computer Science"`.
- Add `"History"` at the end using `.append()`.
- Remove `"Physics"`.
- Print the final list.

### 5. The `len()` and `in` check
Given `cart = ["milk", "bread", "eggs", "butter"]`:
- Print how many items are in the cart.
- Print whether `"sugar"` is in the cart (should give `False`).
- Print whether `"bread"` is in the cart (should give `True`).

### 6. Sort it
Given `marks = [72, 95, 60, 88, 83]`:
- Print the marks sorted in ascending order.
- Print them sorted in descending order.
- Print the **highest** mark.
- Print the **lowest** mark.

### 7. Build a tuple
Create a tuple called `student_record` with: name `"Aisha"`, age `21`, city `"Bangalore"`, GPA `9.1`. Print the entire tuple, then print just the name and just the GPA.

### 8. The single-item tuple trap
Predict (in a comment), then run:
```python
a = (42)
b = (42,)
print(type(a))
print(type(b))
```
What's the difference? Why does the comma matter?

### 9. Try to break a tuple
Run this:
```python
colors = ("red", "green", "blue")
colors[0] = "yellow"
```
Write a one-line comment explaining the error you get and *why* Python refuses.

### 10. Tuple unpacking
Given `point = (12, 25, 7)`, unpack it into three variables `x`, `y`, `z` in **one line**, then print:
```
x = 12, y = 25, z = 7
```
(Use an f-string.)

---

## Set 2 — Bonus (5 problems)

### 11. List of mixed types
Create a list `mixed = ["Aarav", 22, True, 3.14]`. Print each item along with its type using a loop:
```
Aarav <class 'str'>
22 <class 'int'>
…
```
*(Hint: `for item in mixed:` then `print(item, type(item))`)*

### 12. `.append()` vs `.extend()`
Predict (in a comment), then run:
```python
a = [1, 2, 3]
a.append([4, 5])
print(a)

b = [1, 2, 3]
b.extend([4, 5])
print(b)
```
What's the difference? Which one would you use to add multiple items at once?

### 13. The `sort()` returns None bug
Predict (in a comment), then run:
```python
nums = [3, 1, 2]
result = nums.sort()
print(result)
print(nums)
```
What is `result`? What is `nums`? Why does this confuse beginners?

### 14. Convert between list and tuple
Given:
```python
days = ("Mon", "Tue", "Wed", "Thu", "Fri")
```
- Convert it to a list, add `"Sat"`, then convert back to a tuple. Print the result.

### 15. Nested list access
Given:
```python
classroom = [
    ["Aarav", 88],
    ["Priya", 95],
    ["Ravi",  72],
]
```
Print:
- Priya's row (the whole inner list).
- Just Priya's score.
- Aarav's name.

---

## Mini-Build — "Class Roster Manager"

Build a small program that manages a class roster.

### Spec
1. Start with this list:
   ```python
   roster = ["Aarav", "Priya", "Ravi", "Sneha"]
   ```
2. Operations to perform (in this order):
   - **Add** `"Kiran"` to the end.
   - **Insert** `"Divya"` at position 1.
   - **Remove** `"Ravi"`.
   - **Sort** the roster alphabetically.
3. Build a tuple `class_info = ("Batch-2024", 30, "Computer Science")` (batch code, total seats, department) — these are fixed for the program's lifetime.
4. Unpack the tuple into three variables `batch`, `seats`, `dept`.
5. Print exactly this report:

```
========================================
       CLASS ROSTER REPORT
========================================
Batch      : Batch-2024
Department : Computer Science
Seats      : 30
Enrolled   : 5
Roster     : ['Aarav', 'Divya', 'Kiran', 'Priya', 'Sneha']
========================================
```

### Constraints
- Use **at least three** list methods (`append`, `insert`, `remove`, `sort`, etc.).
- Use **tuple unpacking** for `class_info`.
- Use **`len()`** for the enrolled count.
- Use **f-strings** for the report.
- Keep it under 20 lines of code.

---

## Bonus Mini-Build — "Cricket Scorecard" (optional)

> 🟡 **Optional.** A taste of how lists + tuples work together to model real data.

### The problem

You're tracking a T20 cricket innings. Build:
- A **list** of batter scores (changes ball-by-ball — mutable).
- A **tuple** of fixed match details (venue, date, opposition — immutable).

### Spec
1. Create `match_info = ("Wankhede Stadium", "2024-03-15", "Australia")`.
2. Start with `scores = [12, 0, 45]` (three batters in so far).
3. Operations:
   - Batter 4 comes in and scores 33 → `.append(33)`.
   - Batter 2's score gets corrected from `0` to `8` (re-assign by index).
   - Batter 5 scores 21 → append.
4. Compute:
   - **Total runs** using `sum(scores)`.
   - **Highest score** using `max(scores)`.
   - **Number of batters** using `len(scores)`.
5. Unpack `match_info` into `venue`, `date`, `opposition`.
6. Print a scorecard:

```
--- Match Scorecard ---
Venue     : Wankhede Stadium
Date      : 2024-03-15
Vs.       : Australia
Batters   : 5
Total     : 119
Top score : 45
Scores    : [12, 8, 45, 33, 21]
```

### Constraints
- `match_info` must stay a tuple (don't modify it).
- `scores` must use list mutation methods.
- One f-string for the report.

---

## 🛠️ Stuck? Visualise it

Lists *change in place* — that's invisible if you only look at `print()` output. Use these to **see** what's happening.

| Tool | What it's for |
|------|----------------|
| 🔍 [**Python Tutor**](https://pythontutor.com/visualize.html#mode=edit) | The killer tool for this session. Paste your list code, hit "Visualize Execution", step through each line. You'll *see* `.append()`, `.insert()`, `.remove()` rearrange the boxes — and you'll *see* the red error when you try to mutate a tuple. |
| 📖 [**Python docs — Data Structures**](https://docs.python.org/3/tutorial/datastructures.html) | Official reference for lists, tuples, and (preview) dictionaries. |
| 📋 [**Python docs — All list methods**](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists) | The full list method menu — append, extend, insert, remove, pop, clear, index, count, sort, reverse, copy. |
| 📚 [**W3Schools — Lists**](https://www.w3schools.com/python/python_lists.asp) · [**Tuples**](https://www.w3schools.com/python/python_tuples.asp) | Cheatsheet style — fast lookup with examples. |

> **Try this in Python Tutor:** paste any of the homework problems into [pythontutor.com/visualize.html](https://pythontutor.com/visualize.html#mode=edit), step through, and watch your list change. The "wait, what just happened?" feeling vanishes.

---

## Reflection — write in a markdown cell

1. **What clicked today?** One thing that made sense quickly.
2. **What's still fuzzy?** One thing you'd want me to re-explain in 2.1. Be specific.
3. **List vs. tuple — in your own words:** when would you reach for each? Try one sentence.

---

## Preview — Session 2.1

**Title:** Advanced Data Structures — Dictionaries & Sets

So far you've stored data **by position** (index 0, 1, 2…). But what if you want to store data **by name** — `student["Aisha"] = 88`? That's a **dictionary**. And what if you want a collection where every item is unique (no duplicates)? That's a **set**.

These two structures unlock everything from configuration files to JSON APIs to vector search. See you next class.

---

<details>
<summary><b>Solutions — try first, then peek</b></summary>

### Set 1

```python
# 1
subjects = ["Maths", "Physics", "Chemistry", "Biology", "English"]
print(subjects)

# 2
print(subjects[0])     # Maths
print(subjects[-1])    # English
print(subjects[2])     # Chemistry

# 3
print(subjects[:3])    # ['Maths', 'Physics', 'Chemistry']
print(subjects[-2:])   # ['Biology', 'English']
print(subjects[::2])   # ['Maths', 'Chemistry', 'English']

# 4
subjects = ["Maths", "Physics", "Chemistry", "Biology", "English"]
subjects[3] = "Computer Science"
subjects.append("History")
subjects.remove("Physics")
print(subjects)

# 5
cart = ["milk", "bread", "eggs", "butter"]
print(len(cart))             # 4
print("sugar" in cart)       # False
print("bread" in cart)       # True

# 6
marks = [72, 95, 60, 88, 83]
print(sorted(marks))                  # [60, 72, 83, 88, 95]
print(sorted(marks, reverse=True))    # [95, 88, 83, 72, 60]
print(max(marks))                     # 95
print(min(marks))                     # 60

# 7
student_record = ("Aisha", 21, "Bangalore", 9.1)
print(student_record)
print(student_record[0])    # Aisha
print(student_record[3])    # 9.1

# 8 — (42) is just an int with parens around it; (42,) is a real one-item tuple
a = (42)
b = (42,)
print(type(a))   # <class 'int'>
print(type(b))   # <class 'tuple'>

# 9 — TypeError: 'tuple' object does not support item assignment
# Tuples are immutable by design — Python refuses to let you change them.

# 10
point = (12, 25, 7)
x, y, z = point
print(f"x = {x}, y = {y}, z = {z}")
```

### Set 2

```python
# 11
mixed = ["Aarav", 22, True, 3.14]
for item in mixed:
    print(item, type(item))

# 12 — append adds the WHOLE list as one nested item; extend adds each item separately.
a = [1, 2, 3]
a.append([4, 5])
print(a)         # [1, 2, 3, [4, 5]]

b = [1, 2, 3]
b.extend([4, 5])
print(b)         # [1, 2, 3, 4, 5]

# 13 — sort() returns None and modifies in place. Always sort, THEN use the list.
nums = [3, 1, 2]
result = nums.sort()
print(result)    # None
print(nums)      # [1, 2, 3]

# 14
days = ("Mon", "Tue", "Wed", "Thu", "Fri")
days_list = list(days)
days_list.append("Sat")
days = tuple(days_list)
print(days)      # ('Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat')

# 15
classroom = [
    ["Aarav", 88],
    ["Priya", 95],
    ["Ravi",  72],
]
print(classroom[1])       # ['Priya', 95]
print(classroom[1][1])    # 95
print(classroom[0][0])    # Aarav
```

### Mini-Build — Class Roster Manager

```python
roster = ["Aarav", "Priya", "Ravi", "Sneha"]

roster.append("Kiran")
roster.insert(1, "Divya")
roster.remove("Ravi")
roster.sort()

class_info = ("Batch-2024", 30, "Computer Science")
batch, seats, dept = class_info

print("=" * 40)
print("       CLASS ROSTER REPORT")
print("=" * 40)
print(f"Batch      : {batch}")
print(f"Department : {dept}")
print(f"Seats      : {seats}")
print(f"Enrolled   : {len(roster)}")
print(f"Roster     : {roster}")
print("=" * 40)
```

### Bonus Mini-Build — Cricket Scorecard

```python
match_info = ("Wankhede Stadium", "2024-03-15", "Australia")
scores = [12, 0, 45]

scores.append(33)
scores[1] = 8
scores.append(21)

total     = sum(scores)
top_score = max(scores)
batters   = len(scores)

venue, date, opposition = match_info

print("--- Match Scorecard ---")
print(f"Venue     : {venue}")
print(f"Date      : {date}")
print(f"Vs.       : {opposition}")
print(f"Batters   : {batters}")
print(f"Total     : {total}")
print(f"Top score : {top_score}")
print(f"Scores    : {scores}")
```

</details>
