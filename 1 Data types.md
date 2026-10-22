# Python Club: Data Type Challenges 🐍

**Level:** Beginner  
**Focus:** Variables, data types, strings, operators, and type conversion  
**Estimated time:** 60–90 minutes  
**Format:** Individual work or pairs

> **Mission:** Solve the challenges using Python. For each task, run your program, test it with different values, and be ready to explain which data types you used and why.
>
> **Important:** This is the **student task sheet**. It does not include solutions.

## Before you start

- Create a folder named `python-type-challenges`.
- Save each solution as a separate Python file, e.g. `task01.py`, `task02.py`, etc.
- For Tasks 1–6, try to use what you have learned about variables, `print()`, `input()`, `type()`, strings, arithmetic, comparisons, Boolean expressions, and type conversion. **You do not need loops or `if` statements.**
- Tasks 7–10 introduce collection types and can be treated as optional extensions.
- Complete the **bonus challenge** for each task if you finish early.

---

## Round 1 — Basic Data Types

### Task 1 — The Type Detective 🕵️

**Topics:** `int`, `float`, `str`, `bool`, `type()`  
**Difficulty:** Easy

A mysterious programmer has left these variables:

```python
a = 2026
b = "2026"
c = 20.26
d = True
e = "True"
f = 10 / 2
g = 10 // 2
h = 5 > 3
i = "15" + "5"
j = 15 + 5
```

**Your mission:**
1. Without running the code, predict the **value and data type** of each variable.
2. Write a program to print the value and type of each variable.
3. Compare your predictions with the actual results.
4. Explain why two variables can display similar values but have different types.

**Bonus:** Explain the difference between `/` and `//` in Python.

### Task 2 — The Broken Calculator 🔧

**Topics:** `str`, `int`, `float`, `input()`, type conversion  
**Difficulty:** Easy

This calculator has a bug:

```python
number1 = input("First number: ")
number2 = input("Second number: ")
result = number1 + number2
print("Result:", result)
```

When the user types `20` and `5`, it displays `205` instead of `25`.

**Your mission:**
1. Explain why this happens.
2. Fix the calculator so it adds two whole numbers correctly.
3. Modify it to accept decimal numbers, such as `2.5` and `3.75`.
4. Show the data types before and after the conversion.

**Bonus:** Add subtraction, multiplication, and division. For division, test with a nonzero second number.

### Task 3 — The Space Mission 🚀

**Topics:** `float`, arithmetic operators, `round()`, formatted output  
**Difficulty:** Easy

Your team is preparing a mission to the Moon. You need to calculate an astronaut's **weight** under different gravitational conditions.

| Place | Gravity |
|---|---:|
| Earth | 9.81 m/s² |
| Moon | 1.62 m/s² |

Use the formula: **weight (newtons) = mass (kg) × gravity (m/s²)**.

**Your mission:**
1. Ask the astronaut to enter their mass in kilograms.
2. Store the two gravitational values as variables.
3. Calculate their weight on Earth and on the Moon.
4. Display each result to **two decimal places**.
5. Explain why `float` is an appropriate type for this problem.

**Test input:** `60` kg.

**Bonus:** Calculate the percentage reduction in weight on the Moon. Does the astronaut's mass change?

### Task 4 — The Secret Message Machine 🔐

**Topics:** `str`, indexing, slicing, `len()`, concatenation  
**Difficulty:** Medium

A secret message is hidden in this text:

```python
message = "PROGRAMMING"
```

**Your mission:** Write code that displays:
1. The first 3 characters.
2. The last 3 characters.
3. The whole text in reverse order.
4. Every second character, starting with the first.
5. The total number of characters.

**Rules:** Do not manually type the answer strings in your `print()` statements. Derive them from `message`.

**Bonus:** Create a new string by joining the first 3 and last 3 characters. Then test your solution with another word.

### Task 5 — The Robot Entry Test 🤖

**Topics:** `bool`, comparisons, `and`, `not`  
**Difficulty:** Medium

A robot can enter a restricted laboratory only when:
- Its battery level is **at least 50%**, **and**
- Its access code is exactly `ROBOT123`.

Start with:

```python
battery = 75
access_code = "ROBOT123"

# Create these Boolean variables:
enough_battery = ...
correct_code = ...
access_granted = ...
```

**Your mission:**
1. Replace the `...` placeholders with Boolean expressions.
2. Print the three results (`True` or `False`).
3. Test what happens when the battery is `49`.
4. Test what happens when the access code is incorrect.
5. Explain why `and` is needed.

**Bonus:** Introduce `maintenance_mode = True`. Update the rule so access is denied whenever maintenance mode is active.

### Task 6 — The Data Type Trap ⚡

**Topics:** `bool()`, `int()`, `float()`, `str()`, truthiness  
**Difficulty:** Medium

Predict the output of each statement **before running it**:

```python
print(bool(0))
print(bool(1))
print(bool(""))
print(bool("False"))
print(int(8.9))
print(float("12.5"))
print(str(10) + str(20))
print("Ha" * 3)
```

**Your mission:**
1. Record your prediction for each line.
2. Run the code and check your answers.
3. Explain each result in one sentence.
4. Identify which examples demonstrate **conversion** and which demonstrate **operators**.

**Bonus:** Explain why `bool("False")` and `bool(False)` are not the same.

---

## Round 2 — Collection Data Types (Optional Extension)

### Task 7 — The Lost Treasure Inventory 🎒

**Topic:** `list`  
**Difficulty:** Medium

A game character carries this inventory:

```python
inventory = ["Sword", "Shield", "Potion", "Gold"]
```

**Your mission:**
1. Print the first item.
2. Replace `Potion` with `Magic Potion`.
3. Add `Diamond` to the end.
4. Remove `Shield`.
5. Print the updated inventory and the number of items.

**Bonus:** Use the `in` operator to check if `Diamond` is in the inventory.

### Task 8 — The GPS Mystery 📍

**Topic:** `tuple`  
**Difficulty:** Medium

A robot's position is stored as:

```python
location = (12, 8)
```

**Your mission:**
1. Print the X and Y coordinates separately.
2. Predict what happens if you run `location[0] = 15`.
3. Try it and describe the error.
4. Create a **new tuple** with position `(15, 8)` without changing the original.
5. Explain how a tuple differs from a list.

**Bonus:** Store three different locations as tuples.

### Task 9 — The Party Guest Mystery 🎉

**Topic:** `set`  
**Difficulty:** Medium

A party registration system contains duplicate names:

```python
guests = ["Ali", "Madina", "Ali", "Sardor", "Madina", "Aziza"]
```

**Your mission:**
1. Count the total registrations.
2. Convert the names into a set.
3. Count the number of **unique** guests.
4. Display the unique names (their order may vary).
5. Explain why a set is useful here.

**Bonus:** Create a set of VIP names and identify guests who appear in **both** sets.

### Task 10 — Build a Digital Pet 🐱

**Topic:** `dict` with `str`, `int`, `float`, and `bool` values  
**Difficulty:** Medium

Your digital pet has the following profile:

```python
pet = {
    "name": "Pixel",
    "age": 2,
    "weight": 3.5,
    "hungry": True,
    "energy": 80
}
```

**Your mission:**
1. Print the pet's name.
2. Increase its energy by `10`.
3. Set its hungry status to `False`.
4. Add a new key called `favourite_food`.
5. Print the updated dictionary.
6. Identify the type of each value in the dictionary.

**Bonus:** Create a second digital pet and compare their ages, weights, and energy levels using Boolean expressions.

---

## Final Challenge — Student ID Generator 🪪

**Topics:** Combining `str`, `int`, `float`, `bool`, slicing, type conversion, and comparisons  
**Difficulty:** Medium

Build a program that asks for:
- First name
- Surname
- Birth year
- Test score (which may be a decimal)

It must generate a student ID using:
1. The first **2 letters** of the first name, in uppercase.
2. The first **2 letters** of the surname, in uppercase.
3. The last **2 digits** of the birth year, including a leading zero when needed.

It must also print whether the student **passed** (`True` if score is at least `60`, otherwise `False`).

**Example input:** First name `Ali`, surname `Karimov`, birth year `2007`, score `85.5`.

**Example output format:**

```text
Student ID: ALKA07
Passed: True
Score: 85.5
```

**Bonus:** Extend the ID by adding the length of the student's full name (excluding the space).

---

## Quick Prediction Quiz (No Computer First!)

Write down your predictions, then run each expression in Python to verify.

1. What does `"5" + "5"` produce?
2. What is the type of `10 / 2`?
3. What does `bool("False")` produce?
4. What does `17 // 5` produce?
5. Which is mutable: `(1, 2)`, `"Python"`, `[1, 2]`, or `10`?
6. What does `len(set([1, 1, 2, 3]))` produce?
7. What happens when you run `int("12.5")`?

---

## Submission Instructions

1. Save your solutions as `task01.py`, `task02.py`, and so on.
2. At the top of each file, add a comment with the task title.
3. Run each program and test at least two different values when the task accepts input.
4. Be prepared to explain which data types you used.
5. Submit your `.py` files using the method provided by your club leader.

### Optional Club Scoring

| Achievement | Points |
|---|---:|
| Correct output | 5 |
| Correct use of data types | 3 |
| Explanation of solution | 2 |
| Bonus challenge completed | +3 |

**Remember:** The aim is to understand *why* Python produces an output, not just to make the code run. Happy coding! 🚀
