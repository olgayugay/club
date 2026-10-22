# 🐍 Python Club — Level 2: Data Types Challenge Lab

**Level:** Beginner → Intermediate  
**Topics:** Variables, `int`, `float`, `str`, `bool`, type conversion, string methods, arithmetic and logical operators, lists, tuples, sets, and dictionaries  
**Estimated time:** 90–120 minutes (or select 5–6 challenges for one meeting)  
**Format:** Work individually or in pairs  
**Deliverable:** One `.py` file per task

> **Mission:** Go beyond printing values. Use Python's data types to clean messy information, build codes, protect data, manage games, and make decisions.
>
> **Student version:** This worksheet contains **tasks and test cases, but no solutions**.

## Club rules

1. Save your answers as `level2_task01.py`, `level2_task02.py`, etc.
2. Use **meaningful variable names** and a short comment explaining important calculations.
3. Do not simply print the expected answer. Your code must **calculate or construct it** from the supplied variables.
4. Try the starter values first, then change them to check whether the program still works.
5. Most core tasks can be completed **without loops or `if` statements**. You may use them for bonus challenges if you already know them.
6. For every task, be prepared to answer: **Which data types did you use, and why?**

---

## Round 1 — Strings, Numbers, and Boolean Logic

### Challenge 1 — Rescue a Corrupted Registration 🧹

**Focus:** `str`, `int`, `float`, `bool`, `.strip()`, `.title()`, `.lower()`, type conversion  
**Difficulty:** ★★☆

A club registration form has submitted everything as messy **text**:

```python
name_raw = "  mAliKa   "
age_raw = "019"
score_raw = "86.75"
member_raw = " YES "
```

**Your mission:**

1. Clean the name so that it displays as `Malika`.
2. Convert age to an integer and score to a floating-point number.
3. Convert the membership response to an actual Boolean (`True` for `"yes"`, ignoring spaces and letter case).
4. Create a Boolean variable `eligible` that is `True` **only if** the person is at least 18, has a score of at least 80, and is a member.
5. Display a neat registration summary and the resulting data type of each cleaned value.

**Test case:** The supplied registration should be eligible.

**Bonus:** Test `member_raw = " no "`, `age_raw = "017"`, and `score_raw = "79.9"` separately. Explain what changes.

---

### Challenge 2 — Generate an Event Ticket ID 🎟️

**Focus:** String slicing, uppercase, `.split()`, `.zfill()`, converting numbers to strings  
**Difficulty:** ★★☆

Create unique-looking ticket IDs for a Python Club event.

```python
first_name = "Sardor"
last_name = "Karimov"
event = "Python Club"
seat = 7
year = 2026
```

**Ticket format (no spaces):**

- First **2 letters** of the first name
- First **3 letters** of the surname
- Initials of the **two words** in the event name
- Seat number written with **3 digits** (`7` → `007`)
- Last **2 digits** of the year
- The full result in **UPPERCASE**

**Your mission:** Produce the ticket automatically from the variables. Do not type its complete value manually.

**Example format:** `AA BBB XX 007 26` (shown with spaces only to explain its parts).

**Bonus:** Make the code work when the name is entered in lowercase or has spaces at the beginning or end.

---

### Challenge 3 — The Impossible Bill Split 💸

**Focus:** `int`, `//`, `%`, comparisons, arithmetic operators  
**Difficulty:** ★★☆

Six club members must split a bill of **287,000 UZS**, but payments must be made in whole som (no fractional amounts).

```python
total_bill = 287_000
people = 6
```

**Your mission:**

1. Calculate the amount everyone can pay **equally**, as a whole number.
2. Find the amount left over.
3. Explain how many people need to pay **1 extra som** so that the full bill is covered.
4. Verify with a Boolean expression that the collected amounts add up to the original bill.
5. Test again with `total_bill = 100_000` and `people = 3`.

**Test case:** With 287,000 UZS and 6 people, the standard share is **47,833 UZS** and **2 UZS** remain to distribute.

**Bonus:** Ask the user to enter the bill and number of people. Assume the number of people is greater than zero.

---

### Challenge 4 — Decode the Mission Countdown ⏱️

**Focus:** `int`, `//`, `%`, arithmetic, f-strings  
**Difficulty:** ★★☆

A mission timer stores time as one large number of seconds.

```python
total_seconds = 98765
```

**Your mission:** Convert the number into:

- Full days
- Remaining hours (0–23)
- Remaining minutes (0–59)
- Remaining seconds (0–59)

Display the result as: `X days, HH hours, MM minutes, SS seconds`.

**Test cases:**

| Input | Expected breakdown |
|---|---|
| `98765` | 1 day, 3 hours, 26 minutes, 5 seconds |
| `3605` | 0 days, 1 hour, 0 minutes, 5 seconds |
| `59` | 0 days, 0 hours, 0 minutes, 59 seconds |

**Bonus:** Use f-string formatting to display each of hours, minutes and seconds as **two digits**, for example `03:26:05`.

---

### Challenge 5 — The Robot's Complicated Access Rules 🤖

**Focus:** `bool`, `and`, `or`, `not`, `==`, `!=`, parentheses  
**Difficulty:** ★★★

A robot guards the club's equipment room. Entry is granted **only when**:

- The visitor is **staff OR VIP**;
- They have completed registration (`registered == True`);
- They are **not banned**.

```python
is_staff = False
is_vip = True
registered = True
is_banned = False

# TODO: Make one Boolean expression called access_granted.
```

**Your mission:**

1. Create `access_granted` using a **single Boolean expression**.
2. Print the result.
3. Change the values to test a registered non-VIP visitor, a banned VIP, and an unregistered staff member.
4. Explain why parentheses matter in a compound logical expression.

**Bonus — Exclusive entry:** Add `exclusive_role`, which should be `True` when the person is **either staff or VIP, but not both**. Can you solve it using `!=` on two Boolean variables?

---

### Challenge 6 — Python's Most Surprising Outputs ⚡

**Focus:** Numeric and Boolean types, operator precedence, string operations, truthiness  
**Difficulty:** ★★★

**Do not run the code immediately.** Predict both the **value** and **data type** of each expression:

```python
print(True + True)
print("7" * 2)
print(-7 // 3)
print(-7 % 3)
print(bool("0"))
print(bool([]))
print(int(9.99))
print("Python".find("z"))
print(round(2.5))
print(2 ** 3 ** 2)
```

**Your mission:**

1. Write down predictions for all 10 expressions.
2. Run them and mark which predictions were correct.
3. Explain **at least five** surprising results.
4. Identify examples involving conversion, arithmetic operators, string methods, or Boolean logic.

**Bonus:** Explain why `int(-2.9)` and `-7 // 3` do not follow the same rule for handling negative results.

---

## Round 2 — Collections and Mixed Data Types

### Challenge 7 — Repair the Gaming Leaderboard 🏆

**Focus:** Lists, indexing, mutation, `sorted()`, slicing, `max()`, `sum()`, `count()`  
**Difficulty:** ★★☆

A gaming competition has recorded five scores:

```python
scores = [52, 96, 73, 96, 41]
```

**Your mission:**

1. Find the highest score and the average score.
2. Create a **new** list containing scores in descending order (do not change the original yet).
3. Show the **top three scores** using slicing.
4. Count how many players achieved exactly 96 points.
5. Correct the last score from 41 to 82.
6. Check whether **at least one** score is 100 using the `in` operator.
7. Count the number of **distinct** scores using a set.

**Bonus:** Store each player's name with their score using a collection of your choice. Describe how that changes the representation of the leaderboard.

---

### Challenge 8 — Two Clubs, One Campus 🤝

**Focus:** Sets, `&`, `|`, `-`, `^`, membership  
**Difficulty:** ★★☆

Students may join the Python Club, the Data Analytics Club, or both.

```python
python_club = {"Ali", "Malika", "Sardor", "Aziza"}
analytics_club = {"Malika", "Temur", "Aziza", "Madina"}
```

**Your mission:**

1. Find students in **both** clubs.
2. Find students in **at least one** club.
3. Find students in the Python Club **only**.
4. Find students in the Analytics Club **only**.
5. Find students belonging to **exactly one** club.
6. Check whether `"Aziza"` is in both clubs using a Boolean expression.
7. Print the number of unique students participating across the clubs.

**Note:** Sets do not guarantee a particular display order.

**Bonus:** A new student, `"Jasur"`, joins both clubs. Update both sets and recalculate the results.

---

### Challenge 9 — The Privacy Masking Lab 🕶️

**Focus:** String slicing, `.split()`, string multiplication, concatenation, Booleans  
**Difficulty:** ★★★

An event organiser needs to show contact details on a public confirmation screen **without revealing the full values**. Use these **fictional** details:

```python
email = "malika.rahimova@university.edu"
phone = "998901234567"
```

**Your mission:**

1. Display only the **first 2 characters** of the email's username (before `@`), followed by `***`, followed by the original domain.
2. Display the phone number with **every digit except the last 4 replaced by `*`**.
3. Print the length of the original email and phone number.
4. Create Boolean checks showing whether the email contains `@` and whether the phone has at least 9 characters.
5. Do not print the original email or phone in the final public output.

**Target display:**

```text
Email: ma***@university.edu
Phone: ********4567
```

**Bonus:** Test with a shorter email username (for example, `al@university.edu`) and a different phone length. Make sure the masking logic still works.

> **Discussion:** Does masking a value on screen also protect the original data stored elsewhere? Why or why not?

---

### Challenge 10 — Manage the Club Merchandise Shop 🛍️

**Focus:** Nested dictionaries, `int`, arithmetic, updating values, Boolean comparisons  
**Difficulty:** ★★★

Your club sells badges, stickers, and notebooks. Product details are stored in nested dictionaries:

```python
shop = {
    "badge": {"price": 12000, "quantity": 8},
    "sticker": {"price": 4000, "quantity": 25},
    "notebook": {"price": 18000, "quantity": 5}
}
```

**Your mission:**

1. Print the price and quantity of each product by accessing the dictionary values.
2. Calculate the **total value of all stock**: price × quantity for each product, then add the results.
3. A customer buys **3 badges** and **2 notebooks**. Calculate the purchase total.
4. Update the quantities to reflect the sale.
5. Calculate the new total stock value.
6. Create a Boolean expression indicating whether notebooks have **low stock** (`quantity <= 3`).
7. Add a new product, `"keychain"`, priced at 15,000 UZS, with a quantity of 10.

**Rules:** Read prices and quantities from `shop` rather than copying the numbers into your formulas.

**Bonus:** Calculate the average price of the four product types. What data type do you obtain?

---

## Final Mini-Challenge — Student Hackathon Registration 🧩

**Focus:** Combining types, input conversion, strings, Boolean logic, dictionaries  
**Difficulty:** ★★★

Build a basic checker for registrations to a student hackathon. Each registration has:

- Full name (text)
- Team name (text)
- Number of team members (whole number)
- Proposed project score (decimal number)
- Agreement to the participation rules (`"yes"` or `"no"`)

**A registration is valid only if:**

- The team has **1 to 3 members** (inclusive).
- The score is at least **60.0**.
- The participant answered **yes** to the rules (ignore letter case and extra spaces).
- The team name is not empty after removing surrounding spaces.

**Your mission:**

1. Use `input()` to collect the five values.
2. Convert the values into appropriate data types.
3. Store the cleaned information in a dictionary.
4. Calculate a Boolean `is_valid` using logical operators.
5. Print a readable registration summary with the validation result.
6. Test these cases:

| Members | Score | Rules | Team name | Valid? |
|---:|---:|---|---|---|
| 3 | 80.5 | `yes` | `Data Ninjas` | True |
| 4 | 95.0 | `yes` | `Data Ninjas` | False |
| 2 | 59.5 | `yes` | `Data Ninjas` | False |
| 2 | 90.0 | `no` | `Data Ninjas` | False |
| 1 | 75.0 | ` YES ` | `   ` | False |

**Bonus:** Assign each valid entry a formatted reference code constructed from the team name and the member count.

---

## Submission instructions

Create the following files in your GitHub repository:

```text
python-club/
├── level2_task01.py
├── level2_task02.py
├── level2_task03.py
├── level2_task04.py
├── level2_task05.py
├── level2_task06.py
├── level2_task07.py
├── level2_task08.py
├── level2_task09.py
├── level2_task10.py
└── level2_final.py
```

For **each solution**, include:

- Your Python code.
- A short comment stating which data types you used.
- At least one additional test with changed values.

### Optional club scoring

| Criterion | Points |
|---|---:|
| Correct program behaviour | 5 |
| Appropriate data types and operators | 3 |
| Clear variables and readable code | 2 |
| Bonus challenge completed | +3 |

**Club discussion:** Which task became easier because you chose the *right data type*? What bugs appeared when a value was stored as the *wrong type*?
