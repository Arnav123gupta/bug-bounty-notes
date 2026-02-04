# ✅ Day 12 – IDOR Testing Checklist (Beginner Friendly)

Aaj hum banayenge **IDOR testing checklist**  
jisse tum bug bounty me IDOR ko systematically test kar pao 🆔🐞

⚠️ Always test only in **allowed scope**.

---

## 🎯 IDOR ka Simple Meaning
IDOR = jab tum **ID change karke** kisi aur ka data access kar pao  
because server proper authorization check nahi karta ❌

---

## 🧠 IDOR Testing Checklist ✅

### 1️⃣ Find “ID” Based Features 🔍
Check these areas:
- 👤 Profile
- 🛒 Orders / invoices
- 🎟️ Tickets / support
- 📦 Bookings
- 📂 Documents / downloads
- 🏦 Wallet / transactions

---

### 2️⃣ Spot Parameters & IDs 🎯
Look for:
- `id`
- `user_id`
- `account_id`
- `order_id`
- `ticket_id`
- `doc_id`

Example URLs:
/profile?id=1001
/order?id=555
/ticket?id=77
/download?doc_id=9

---

### 3️⃣ Check if ID is Predictable 🔢
Predictable IDs:
- 1,2,3,4…
- 1001,1002,1003…

If IDs are predictable → IDOR chances high 📈

---

### 4️⃣ Change the ID (Safe Observation) 👀
Try:
- +1 / -1
- random valid-looking number

Example:
/order?id=555 -> /order?id=556

Check response:
- ❌ Access denied? (good security)
- ✅ Data visible? (possible IDOR)

---

### 5️⃣ Test With Two Accounts (Best Method) 👥
IDOR confirm karne ka best way:

✅ Account A (your account)  
✅ Account B (second test account)

Steps:
1. Account A se object open karo (order/ticket)
2. Uska ID note karo
3. Account B se same ID access try karo
4. Agar access mil gaya → IDOR strong proof 🚨

---

### 6️⃣ Check Read vs Write IDOR ✏️
IDOR 2 types me hota hai:

#### 🔹 Read IDOR (View)
- dusre ka profile/order view ho jaye

#### 🔹 Write IDOR (Edit/Delete)
- dusre ka data update/delete ho jaye

Write IDOR = **higher severity** 💥

---

### 7️⃣ Test API Endpoints (If In Scope) 🔗
Sometimes IDOR UI me nahi hota  
but API me hota hai.

Check:
- `/api/user/123`
- `/api/orders/555`

🧠 Tip:
> API IDOR bug bounty me frequently milta hai.

---

### 8️⃣ Check Role Based Access 👑
Example:
- Normal user
- Admin user

If normal user can access admin objects → big issue 🚨

---

## 🛡️ What a Secure App Should Do
If you change ID:
- server should return `403 Forbidden`
- OR “Not authorized”
- OR no data

---

## 📌 Severity Guide (Easy)
- Only viewing small data → Medium/High
- Viewing sensitive data → High
- Editing/deleting data → High/Critical 💣

---

## ⚠️ Legal Reminder
❌ Out-of-scope targets test mat karo  
❌ Real users ka data access mat karo  
✅ Always use your own test accounts

---

## 📌 Key Takeaway
> IDOR ka main test = **ID change + authorization check fail** 🆔🔥

---

### 🚀 Next Day Preview
➡️ **Day 13 – Broken Access Control (BAC) Basics** 🔓🐞

---

🧑‍💻 Maintained by: **Arnav**  
⭐ Consistency = Success 💚
