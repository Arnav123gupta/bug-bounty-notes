# 🧨 Day 4 – SQL Injection (SQLi) Basics

👋 Aaj hum seekhenge **SQL Injection** ke basics – ek **high-impact & common bug bounty vulnerability**.

---

## 🔐 What is SQL Injection?
SQL Injection ek vulnerability hoti hai jisme attacker **user input ke through database query ko manipulate** kar deta hai.

👉 Simple words me:  
Agar website user ke input ko **properly validate / sanitize** nahi karti, to database ke saath cheating ho sakti hai 😬

---

## 🧠 Why SQL Injection is Dangerous?
SQLi se attacker:
- 📂 Sensitive data read kar sakta hai (users, passwords, emails)
- ✏️ Database data change / delete kar sakta hai
- 🔑 Kabhi-kabhi admin access bhi mil jata hai
- 💥 Poor security wali sites puri compromise ho sakti hain

Isliye ye **Critical severity** mana jata hai.

---

## 🧩 How SQL Injection Happens (Concept)
1. Website user se input leti hai (login, search, form etc.)
2. Ye input directly SQL query me use hota hai
3. Agar input validate nahi hua → SQL Injection possible ❌

⚠️ Ye tab hota hai jab:
- Input sanitization na ho
- Prepared statements use na kiye gaye ho

---

## 🗂️ Common Places Where SQLi Found
- 🔑 Login forms
- 🔍 Search boxes
- 📝 Contact / feedback forms
- 🔗 URL parameters (id=, user= etc.)

---

## 🧪 Types of SQL Injection (Intro)
- **Classic SQL Injection**
- **Blind SQL Injection**
- **Error-based SQL Injection**
- **Time-based SQL Injection**

👉 Inko hum **next days me detail me** cover karenge 👀

---

## 🛡️ How Developers Prevent SQL Injection
(Defensive knowledge – very important 👇)
- ✅ Prepared Statements
- ✅ Parameterized Queries
- ✅ Input Validation
- ✅ ORM usage

---

## 🐞 SQL Injection in Bug Bounty
- SQLi abhi bhi **real programs me milta hai**
- Proper proof + clean report = 💰 rewards
- Beginners ke liye **must-learn vulnerability**

---

## 📌 Key Takeaway
> SQL Injection tab hota hai jab user input ko blindly database me trust kar liya jata hai.

---


🧑‍💻 Maintained by: **Arnav**  
⭐ Repo ko star karna mat bhoolna (self-motivation 😄)
