# 🔐 Password Generator (Day 15)

A secure password generator written in Python.  
Set the desired length, get a random password, and see its **strength rating**.

---

## 📌 Features
- Length limits: **6–32**
- Character set: **letters (a–z, A–Z), digits, punctuation**
- Random generation with `random.choice`
- Simple strength indicator: **Weak / Medium / Strong**

---

## ▶️ Example run
=== Password Generator ===
Enter password length (6-32): 12
Generated password: a9&KzP1#X!tQ
Password strength: Medium ⚠️

lua
Copy code

---

## 💻 Code (main)
```python
import random
import string

length = int(input("Enter password length (6-32): "))
if length < 6 or length > 32:
    print("Error: length must be between 6 and 32 characters.")
else:
    characters = string.ascii_letters + string.digits + string.punctuation
    password = "".join(random.choice(characters) for _ in range(length))
    print("Generated password:", password)

    if length < 8:
        print("Password strength: Weak ❌")
    elif 8 <= length < 12:
        print("Password strength: Medium ⚠️")
    else:
        print("Password strength: Strong ✅")
🚀 Future improvements
Enforce at least one uppercase, lowercase, digit, and special character

Add option to exclude similar chars (O, 0, l, 1)

Copy to clipboard automatically

GUI version (Tkinter) or web version (Flask/FastAPI)

✨ This project is part of my Python learning journey (Day 15).
