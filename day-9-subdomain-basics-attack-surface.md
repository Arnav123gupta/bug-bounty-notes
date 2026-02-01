# 🌐 Day 9 – Subdomain Basics + Attack Surface Thinking

Aaj hum seekhenge:
✅ Subdomain kya hota hai  
✅ Bug bounty me subdomains kyu important hote hain  
✅ Attack surface kaise sochte hain (pro mindset) 🧠🐞

---

## 🔥 What is a Subdomain?
Subdomain ek main domain ka part hota hai.

Example:
Main domain:
- `example.com`

Subdomains:
- `admin.example.com`
- `api.example.com`
- `dev.example.com`
- `staging.example.com`
- `blog.example.com`

👉 Subdomain ka use companies different services run karne ke liye karti hain.

---

## 🎯 Bug Bounty me Subdomains kyu important hote hain?
Kyuki:
- Har subdomain ka **security level same nahi hota**
- Kuch subdomains:
  - old / forgotten hote hain 🧟
  - misconfigured hote hain ⚙️
  - weak authentication rakhte hain 🔓

Isliye subdomains = **extra chances to find bugs** 📈

---

## 🧠 Attack Surface Thinking (Pro Mindset)
Attack surface ka matlab:
> Target me jitne entry points hain jaha se user interact kar sakta hai.

Attack surface me include hota hai:
- Login pages
- APIs
- Admin panels
- Upload forms
- Search features
- Subdomains
- Mobile endpoints

📌 Bug bounty me winner wo hota hai jo:
✅ “feature ko deeply samajhta hai”  
❌ “random payload spam nahi karta”

---

## 🔍 Common Interesting Subdomains (High Value)
Ye subdomains bug bounty me interesting hote hain:

- `admin.` 👑 (admin panel exposure)
- `api.` 🔗 (API endpoints & auth issues)
- `dev.` 🧪 (weak security / debug mode)
- `test.` 🧫 (testing environment leaks)
- `staging.` 🚧 (pre-production version)
- `old.` 🕰️ (outdated version)
- `beta.` 🧩 (new features, less tested)
- `cdn.` 📦 (assets, sometimes misconfig)

⚠️ Note: Har program me in-scope nahi hota  
Always scope check karo ✅

---

## 📝 Recon Notes Example (How to Save)
Create a file:
`subdomains-notes.md`

Example:
```txt
api.target.com  -> API
admin.target.com -> Admin Panel
staging.target.com -> Staging
blog.target.com -> Blog

🐞 Bug Types You Can Find on Subdomains

Subdomains par common bugs:

🔓 Broken Access Control

🆔 IDOR

🐞 XSS

⚙️ Misconfigurations

📂 Sensitive info exposure

🔑 Weak authentication / default creds (only legal scope)

💡 Pro Tip (Simple but Powerful)

Subdomain milne ke baad direct hacking mat start karo.

First do:

Open it in browser

Understand feature

Map endpoints

Identify inputs

Then test

“Understand first → test later” = pro rule 😎

⚠️ Legal Reminder

❌ Out-of-scope subdomains test mat karo
✅ Only allowed scope me hi test karo

📌 Key Takeaway

Subdomains increase attack surface,
aur attack surface badhega = bug chances badhenge 📈🔥

🚀 Next Day Preview

➡️ Day 10 – Parameter Hunting Basics (Beginner Friendly) 🎯

🧑‍💻 Maintained by: Arnav
⭐ Daily commits = strong profile 💚
