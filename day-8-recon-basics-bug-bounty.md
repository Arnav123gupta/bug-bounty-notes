# 🔍 Day 8 – Recon Basics (Bug Bounty)

Aaj hum seekhenge **Reconnaissance (Recon)** —  
bug bounty ka sabse important step 🧠🐞

Recon ka matlab hota hai:
> Target ke baare me info collect karna (legal scope me)  
taaki vulnerabilities dhundhna easy ho jaye ✅

---

## 🎯 Recon ka Goal
Recon ka main goal:
- 🌐 Target ka **attack surface** samajhna
- 🔎 Hidden endpoints / pages discover karna
- 🧩 Parameters & features identify karna
- 🐛 Testing ke liye best areas choose karna

---

## 🧠 Recon = Bug Bounty ka Foundation
Agar recon strong hai → bug finding chances high 📈  
Agar recon weak hai → tum random testing karoge 😵

---

## 🗂️ Recon ke 2 Types

### 1️⃣ Passive Recon (Safe & Quiet) 🕵️‍♂️
Passive recon me tum target ko directly hit nahi karte.

Examples:
- Public URLs & pages
- Old subdomains info
- Public docs / help pages
- JS file hints (frontend analysis)
- Public leaks / mentions (within legal limits)

✅ Beginner ke liye best  
✅ Low risk  
✅ Easy to start

---

### 2️⃣ Active Recon (Direct Interaction) ⚙️
Active recon me tum target ke endpoints ko request bhejte ho.

Examples:
- Directory discovery
- Parameter discovery
- Endpoint enumeration
- Response analysis

⚠️ Always scope + rules follow karo  
⚠️ Rate limit ka dhyan rakho

---

## 🧩 What to Collect in Recon? (Checklist) ✅

### 🌐 Assets
- Main domain
- Subdomains (in-scope)
- APIs (if mentioned)
- Web apps / panels

### 🧭 Important Features
- Login / Signup
- Password reset
- Profile settings
- File upload
- Search
- Payments / orders (if exists)

### 🔗 Endpoints & Params
- `/search?q=`
- `/profile?id=`
- `/product?id=`
- `/api/v1/...`

---

## 📌 Recon Notes Kaise Maintain Kare? 📝
Pro hunters always notes maintain karte hain.

Create files like:
- `recon-notes.md`
- `endpoints.txt`
- `params.txt`

Example format:
```txt
/login
/signup
/reset-password
/search?q=
/product?id=
/profile?user=

🐞 Bug Bounty Tip (Gold) 💡

Recon ke baad direct “sab kuch test” mat karo.

✅ Pick 1 feature
✅ Deep test karo
Example:

Password reset flow

File upload

Search feature

Deep testing = more real bugs 🔥

⚠️ Legal Reminder

❌ Random websites test mat karo
✅ Sirf allowed scope & labs me practice karo

📌 Key Takeaway

Recon jitna strong hoga, bugs utne jaldi milenge.

🚀 Next Day Preview

➡️ Day 9 – Subdomain Basics + Attack Surface Thinking 🌐

🧑‍💻 Maintained by: Arnav
⭐ Daily 1 commit = strong GitHub profile 💚
