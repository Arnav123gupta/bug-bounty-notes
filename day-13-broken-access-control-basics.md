# 🔓 Day 13 – Broken Access Control (BAC) Basics

Aaj hum seekhenge **Broken Access Control (BAC)** —  
ye OWASP Top vulnerabilities me se ek hai aur bug bounty me bahut common hai 🐞🔥

---

## 🔐 Access Control kya hota hai?
Access control decide karta hai:

👉 Kaun kya access kar sakta hai  
👉 Kaun kya modify kar sakta hai  
👉 Kaun kis feature ka use kar sakta hai  

Example:
- Normal user → apna profile
- Admin → sab users ka data

---

## ❌ Broken Access Control kya hota hai?
Jab system proper restrictions apply nahi karta:

> User wo actions kar paata hai jo usko allowed nahi hain 🚨

👉 Isi ko Broken Access Control kehte hain.

---

## 🧠 Simple Example
Agar normal user:
- admin panel open kar le 😈
- dusre user ka order cancel kar de
- kisi aur ka data edit kar de

➡️ Ye Broken Access Control hai.

---

## 🎯 BAC vs IDOR (Difference Samjho)

| Feature | IDOR | Broken Access Control |
|--------|------|----------------------|
| ID change se access | ✅ | Sometimes |
| Unauthorized actions | ❌ | ✅ |
| Role bypass | ❌ | ✅ |
| Permission issues | ❌ | ✅ |

👉 IDOR = missing authorization  
👉 BAC = permission system broken

---

## 🔍 Broken Access Control kaha milta hai?

### 👑 Role Based Access Issues
- Normal user admin page access kar le
- Admin-only feature sab use kar pa rahe ho

### 🔐 Forced Browsing
User directly restricted URL open kar le:
/admin
/dashboard/admin
/manage-users


### ✏️ Unauthorized Actions
- dusre ka password change
- dusre ka order cancel
- role change kar pana

### 🔗 API Authorization Failures
API request me role change possible:
```json
{
  "role": "admin"
}
🧪 BAC Testing Mindset

Testing ke waqt poochho:

✅ Kya normal user admin page dekh sakta hai?
✅ Kya restricted URL manually open ho raha hai?
✅ Kya user dusre ka data edit kar sakta hai?
✅ Kya role change possible hai?

🔥 Real World BAC Examples

User apna price change kar pa raha hai

Normal user premium features unlock kar raha hai

Role change karke admin access mil gaya

Restricted APIs access ho rahi hain

💥 Ye bugs companies ke liye serious risk hote hain.

🛡️ Developers BAC kaise prevent karte hain?

✅ Server-side authorization checks

✅ Role-based access control (RBAC)

✅ Deny-by-default permissions

✅ Sensitive actions verify karna

✅ Client-side validation par trust na karna

📌 Key Takeaway

Broken Access Control = system permissions fail
User unauthorized actions kar paata hai 🔓

🚀 Next Day Preview

➡️ Day 14 – Authentication vs Authorization (Easy Guide) 🔐🧠

🧑‍💻 Maintained by: Arnav
⭐ Learn → Practice → Earn 💚
