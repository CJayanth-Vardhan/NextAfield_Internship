# 🔐 Burp Suite Proxy Configuration Guide

## 📌 Overview
This guide explains how to configure **Burp Suite** as an HTTP proxy and connect it with the Firefox browser. It also covers installing the Burp CA certificate and verifying the setup using a test application.

---

## ⚙️ Step 1: Configure Burp Suite (HTTP Proxy)

1. Launch **Burp Suite Community Edition**  
2. Navigate to the **Proxy** tab  
3. Turn **Intercept ON**  

📸 *Screenshot: Burp Suite proxy intercept enabled*

---

## 🌐 Step 2: Configure Browser Proxy (Firefox)

1. Open **Firefox Settings**  
2. Go to **Network Settings**  
3. Select **Manual Proxy Configuration**  
4. Enter the following details:
   - **HTTP Proxy:** 127.0.0.1  
   - **Port:** 8080  
5. Enable **“Use this proxy server for all protocols”**  

📸 *Screenshot: Firefox proxy configuration settings*

---

## 🔒 Step 3: Install Burp CA Certificate

1. Open browser and go to: `http://burp`  
2. Download the **CA Certificate**  

### Import Certificate in Firefox:
1. Go to **Settings → Privacy & Security**  
2. Scroll to **Certificates**  
3. Click **View Certificates → Import**  
4. Select the downloaded certificate  

📸 *Screenshot: Burp certificate download page*  
📸 *Screenshot: Firefox certificate import window*

---

## ✅ Step 4: Verification

1. Open a test web application (e.g., DVWA)  
2. Perform any action in the browser  
3. Check Burp Suite → Proxy → Intercept  

✔️ The HTTP request should be captured successfully  

📸 *Screenshot: HTTP request intercepted in Burp Suite*

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
