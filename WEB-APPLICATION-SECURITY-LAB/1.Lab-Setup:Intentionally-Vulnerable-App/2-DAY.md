# 🔐 Burp Suite Proxy Configuration Guide

## 📌 Overview
This guide explains how to configure **Burp Suite** as an HTTP proxy and connect it with the Firefox browser. It also covers installing the Burp CA certificate and verifying the setup using a test application.

---

## ⚙️ Step 1: Configure Burp Suite (HTTP Proxy)

1. Launch **Burp Suite Community Edition**  
2. Navigate to the **Proxy** tab  
3. Turn **Intercept ON**  

<img width="1598" height="837" alt="image" src="https://github.com/user-attachments/assets/ea3f21b2-20e7-45ff-93ec-b5954283ee83" />

---

---

## 🌐 Step 2: Configure Browser Proxy (Firefox)

1. Open **Firefox Settings**  
2. Go to **Network Settings**  
3. Select **Manual Proxy Configuration**  
4. Enter the following details:
   - **HTTP Proxy:** 127.0.0.1  
   - **Port:** 8080  
5. Enable **“Use this proxy server for all protocols”**  

<img width="759" height="688" alt="image" src="https://github.com/user-attachments/assets/a6870021-94b4-402e-b6a1-4938f20c1a28" />


---

## 🔒 Step 3: Install Burp CA Certificate

1. Open browser and go to: `http://burp`  
2. Download the **CA Certificate**  

### Import Certificate in Firefox:
1. Go to **Settings → Privacy & Security**  
2. Scroll to **Certificates**  
3. Click **View Certificates → Import**  
4. Select the downloaded certificate  

<img width="1718" height="795" alt="image" src="https://github.com/user-attachments/assets/7e93e126-54d2-405c-bda1-040994506f9c" />


---

## ✅ Step 4: Verification

1. Open a test web application (e.g., DVWA)  
2. Perform any action in the browser  
3. Check Burp Suite → Proxy → Intercept  

✔️ The HTTP request should be captured successfully  

<img width="1597" height="477" alt="image" src="https://github.com/user-attachments/assets/b460a908-2177-40bb-8387-81a074a5f802" />

---

## 🎯 Result

- Burp Suite proxy is successfully configured  
- Browser traffic is routed through Burp  
- HTTPS interception is enabled using CA certificate  

---

## 🛠️ Tools Used

- Burp Suite Community Edition  
- Mozilla Firefox  
- DVWA (Damn Vulnerable Web Application)  
