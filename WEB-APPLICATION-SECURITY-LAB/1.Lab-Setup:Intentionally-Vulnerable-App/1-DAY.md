# 🔐 Web Application Security Lab  

## 📌 Project Overview  
I built a hands-on web application security lab using intentionally vulnerable applications to understand real-world security issues. The goal of this project is to learn how vulnerabilities work, how to safely exploit them, and how to think like both an attacker and a defender.  

All testing is done in a controlled local environment using Docker.  

---

## Lab Setup  

### Environment  
- OS: Kali Linux  
- Tools Used:  
  - Docker & Docker Compose  
  - Burp Suite (installed)  
  - SQLMap (installed)  

---

### Applications Deployed  
Using Docker Compose, I deployed the following vulnerable applications:  

- DVWA (Damn Vulnerable Web Application)  
- OWASP Juice Shop  
- OWASP WebGoat  

---

### Docker Setup  

```bash
mkdir web-security-lab
cd web-security-lab
```

Created `docker-compose.yml`:  

```yaml
services:
  dvwa:
    image: vulnerables/web-dvwa
    ports:
      - "8081:80"

  juice-shop:
    image: bkimminich/juice-shop
    ports:
      - "3000:3000"

  webgoat:
    image: webgoat/webgoat-8.0
    ports:
      - "8082:8080"
```

---

### Run Containers  

```bash
docker compose up -d
```

---

### Access URLs  
- DVWA → http://localhost:8081  
- Juice Shop → http://localhost:3000  
- WebGoat → http://localhost:8082/WebGoat  

---

### Verification Steps  

Check running containers:  

```bash
docker ps
```

---

### Key Learnings  
- Understanding Docker port mapping (host vs container ports)  
- Debugging container issues using logs  
- Identifying service startup problems  
- Fixing real-world configuration mistakes  
