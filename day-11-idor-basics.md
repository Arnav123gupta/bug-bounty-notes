# 🆔 Day 11 – IDOR Basics (Most Common Bug in Bug Bounty)

Aaj hum seekhenge **IDOR (Insecure Direct Object Reference)** —  
ye bug bounty me sabse common aur high-impact vulnerability hai 🐞🔥

---

## 🔐 What is IDOR?
IDOR tab hota hai jab website/app:
- kisi object (data) ko access karne ke liye direct **ID** use karti hai  
- aur server proper authorization check nahi karta ❌

👉 Simple words me:
> “Mujhe sirf apna data dekhna chahiye,  
lekin main ID change karke dusre ka data dekh pa raha hoon” 😈

---

## 🧠 Easy Example
Agar tumhara profile URL hai:
/profile?id=1001


Aur tum `id=1002` kar do  
aur dusre user ka profile open ho jaye…

✅ That is IDOR (if not allowed) 🚨

---

## 🎯 Why IDOR is Dangerous?
IDOR se attacker:
- 📂 dusre users ka data dekh sakta hai
- ✏️ data edit / delete kar sakta hai
- 🛒 orders cancel/modify kar sakta hai
- 💳 payments info access kar sakta hai (worst case)

Isliye IDOR mostly **High severity** hota hai 💥

---

## 🗂️ IDOR kaha milta hai?
Common places:
- 👤 Profile pages
- 🛒 Orders / invoices
- 📦 Products / bookings
- 🏦 Wallet / transactions
- 📝 Support tickets
- 🗃️ Documents / downloads

---

## 🔍 Common IDOR Parameters
Ye parameters suspicious hote hain:
- `id`
- `user_id`
- `account_id`
- `order_id`
- `ticket_id`
- `invoice_id`
- `doc_id`

🧠 Pro Tip:
> Jaha ID hai, waha IDOR ka chance hai 😄

---

## 🧪 IDOR Testing Mindset (Safe & Legal)
IDOR test karne ka best way:
1. Apne account se login karo
2. Kisi object ka ID note karo
3. Check karo kya ID change ho sakta hai
4. Observe response (access deny hota hai ya allow)

⚠️ Sirf allowed scope me hi test karo.

---

## 🛡️ How Developers Prevent IDOR?
IDOR prevent karne ke liye:
- ✅ Proper authorization checks (server-side)
- ✅ Access control rules
- ✅ Don’t trust client-side validation
- ✅ Use random/unpredictable IDs (not enough alone)

---

## 📌 Key Takeaway
> IDOR = ID change karke unauthorized access mil jana  
> Root issue = **missing authorization**

---

### 🚀 Next Day Preview
➡️ **Day 12 – IDOR Testing Checklist (Beginner Friendly)** ✅🆔

---

🧑‍💻 Maintained by: **Arnav**  
