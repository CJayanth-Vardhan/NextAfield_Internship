# ⚡ Cross-Site Scripting (XSS) – OWASP Juice Shop

## 📌 Overview
In this task, I performed Cross-Site Scripting (XSS) attacks on OWASP Juice Shop.  
The goal was to test how user input is handled and check if JavaScript code can run in the browser.

---

## 🎯 Target
- Application: OWASP Juice Shop  
- URL: http://localhost:3000  

---

## 🔸 Reflected XSS

### 🧪 Steps

#### 🔹 Step 1: Open Application
- Open Juice Shop  
- Use the search bar  

---

#### 🔹 Step 2: Try Basic Payload (Blocked)

<script>alert('XSS')</script>

- This payload was blocked by the application  

---

#### 🔹 Step 3: Use Bypass Payload (Successful)

<img src=x onerror=alert('XSS')>

- Alert popup appeared  
- JavaScript executed successfully  

---

## ✅ Result
- XSS vulnerability confirmed  
- Application is not properly filtering input  

---

## 🛠️ Tools Used
- OWASP Juice Shop  
- Web Browser  
