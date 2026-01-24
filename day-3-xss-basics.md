# 🗓️ Day 3 – Cross-Site Scripting (XSS) Basics

 
🛡️ Ethical Hacker | 🐞 Bug Bounty Learner | CEH Aspirant  

---

## 🔐 What is XSS?
XSS (Cross-Site Scripting) ek **web vulnerability** hai jisme attacker  
malicious JavaScript inject karta hai website ke andar.

👉 Jab victim user website open karta hai,  
toh injected script **browser me execute ho jati hai** 😨

---

## 🧠 Simple Words Me
- Website user ka input sahi se **validate / sanitize nahi karti**
- Attacker JavaScript inject karta hai
- User ka data steal ho sakta hai 🍪📸

---

## 🧪 Types of XSS

### 1️⃣ Reflected XSS
- Input URL / form se aata hai
- Response me turant reflect hota hai
- Mostly phishing links me use hota hai 🎯

### 2️⃣ Stored XSS
- Payload database me save ho jata hai
- Har user ke liye execute hota hai
- **High impact vulnerability** 💣

### 3️⃣ DOM-Based XSS
- Client-side JavaScript ki wajah se hota hai
- Server involve nahi hota
- JS DOM manipulation ke kaaran trigger hota hai ⚙️

---

## ⚠️ XSS Se Kya Risk Hota Hai?
- 🍪 Session hijacking  
- 🔑 Cookie / token steal  
- 🧑‍💻 Account takeover  
- 📤 Phishing attacks  

---

## 🧰 Common XSS Payload Examples (Learning Only)
```html
<script>alert(1)</script>
<img src=x onerror=alert(1)>
"><script>alert(document.domain)</script>
