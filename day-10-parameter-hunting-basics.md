# 🎯 Day 10 – Parameter Hunting Basics (Beginner Friendly)

Aaj hum seekhenge *Parameter Hunting* —  
bug bounty me bugs nikalne ka ek super important step 🧠🐞

Parameter ka matlab hota hai:
> URL / request me wo value jo server ko data bhejti hai

---

## 🔥 Parameter kya hota hai?
Example URL:
https://example.com/product?id=101
Yaha:
- id = parameter name
- 101 = parameter value

➡️ Parameters se website decide karti hai ki kya data show karna hai.

---

## 🧠 Bug Bounty me Parameters kyu important hote hain?
Kyuki vulnerabilities mostly *input points* par milti hain.

Parameters se bugs mil sakte hain:
- 🆔 IDOR (most common)
- 🔓 Broken Access Control
- 🐞 XSS
- 💉 SQLi (agar backend unsafe ho)
- 📂 Sensitive info exposure

---

## 🗂️ Parameters kaha milte hain?
### 1️⃣ URL Parameters (GET)
Example:
/profile?user=name /order?id=555 /search?q=termux


### 2️⃣ Form Parameters (POST)
Example:
- login form: username, password
- signup form: email, phone

### 3️⃣ API Parameters
Example:
- JSON body me:
```json
{
  "userId": 10,
  "role": "user"
}
🔍 Common High-Value Parameters (Bug Bounty)
Ye parameters mostly sensitive hote hain:
id
user
user_id
account
account_id
profile
email
role
admin
redirect
next
return
file
path
🧠 Pro Tip:
Jaha id / userId hoga, waha IDOR ka chance hota hai 😈
🧪 Parameter Hunting ka Simple Method (No Tools Needed)
✅ Step 1: Website flow samjho
Login
Profile
Settings
Orders
Dashboard
✅ Step 2: URLs observe karo
Check:
URL me ? hai?
= hai?
multiple params & se?
Example:
Copy code

/product?id=10&ref=home
✅ Step 3: Notes banate jao
Create file: params-notes.md
Example:
Copy code
Txt
/profile?user=
/order?id=
/search?q=
/download?file=
/redirect?next=
🧠 Attack Surface Thinking (Parameter Edition)
Agar parameter:
data fetch kar raha hai → IDOR chance
redirect kar raha hai → open redirect chance
file/path handle kar raha hai → path traversal chance
search/input accept kar raha hai → XSS/SQLi chance
⚠️ Safe Testing Reminder
❌ Random websites par testing mat karo
✅ Sirf:
Bug bounty scope
Practice labs
Legal targets
📌 Key Takeaway
Parameters = entry points
Entry points = bugs ke chances 🔥
🚀 Next Day Preview
➡️ Day 11 – IDOR Basics (Most Common Bug in Bug Bounty) 🆔🐞
🧑‍💻 Maintained by: Arnav
