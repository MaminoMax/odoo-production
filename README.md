# 🚀 Odoo 17 Production-Ready Infrastructure

![Odoo](https://img.shields.io/badge/Odoo-17-purple?style=for-the-badge&logo=odoo)
![Docker](https://img.shields.io/badge/Docker-Compose-blue?style=for-the-badge&logo=docker)
![Nginx](https://img.shields.io/badge/Nginx-green?style=for-the-badge&logo=nginx)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Server-orange?style=for-the-badge&logo=ubuntu)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue?style=for-the-badge&logo=postgresql)

## 🎯 Project Overview

This project is a production-grade Odoo 17 ERP infrastructure deployed on a Ubuntu Server using Docker-based architecture.
It simulates a real-world enterprise environment by integrating:

- Secure reverse proxy (Nginx)
- Containerized ERP system (Odoo + PostgreSQL)
- Full monitoring stack (Prometheus + Grafana)
- Server security hardening (iptables + Fail2Ban)
- Automated backup and recovery system

👉 The goal is to demonstrate DevOps, System Administration, and Infrastructure Security skills in a real production-like setup.

---

## 💡 Project Goals

- Deploy a scalable and production-like ERP system
- Implement secure server architecture
- Automate infrastructure deployment using Docker
- Enable full system observability and monitoring
- Ensure data safety through automated backups

---

## 🏗️ Architecture

```
Internet
            │
            ▼
┌──────────────────────┐
│   Nginx (HTTPS 443)  │
└──────────────────────┘
            │
┌──────────────────────┐
│     Odoo 17 App      │
└──────────────────────┘
            │
┌──────────────────────┐
│  PostgreSQL Database  │
└──────────────────────┘
```

**Monitoring Stack:**

```
Node Exporter  ─┐
cAdvisor        ─┼──► Prometheus ───► Grafana Dashboard
Odoo Metrics    ─┘
```

---

## 🛠️ Tech Stack

| Layer            | Technology                    |
|------------------|-------------------------------|
| OS               | Ubuntu Server 22.04           |
| Containerization | Docker + Docker Compose       |
| ERP              | Odoo 17                       |
| Database         | PostgreSQL 15                 |
| Reverse Proxy    | Nginx                         |
| Monitoring       | Prometheus + Grafana + cAdvisor |
| Security         | iptables + Fail2Ban           |
| Automation       | Bash + Cron                   |
| SSL              | HTTPS (Self-signed for testing) |

---

## ⚙️ Deployment Steps

1. Install Ubuntu Server and update system
2. Install Docker & Docker Compose
3. Configure project structure in /opt/odoo
4. Set up Odoo configuration file (odoo.conf)
5. Deploy services using Docker Compose
6. Configure Nginx reverse proxy
7. Enable HTTPS (self-signed / production-ready upgrade planned)
8. Configure firewall rules using iptables
9. Implement Fail2Ban protection
10. Set up monitoring stack (Prometheus & Grafana)
11. Configure automated backups using cron jobs

---

## 🔒 Security Implementation

This project includes multiple security layers:

- 🔐 HTTPS encryption via SSL
- 🧱 Nginx reverse proxy hides internal services
- 🚫 iptables firewall restricts all unnecessary ports
- 🛡️ Fail2Ban protects against brute-force attacks
- 🔒 PostgreSQL is isolated in Docker network (no public exposure)
- 📦 Data persistence using Docker volumes

---

## 📊 Monitoring & Observability

The system is fully monitored using:

- **Grafana** → Visual dashboards for system metrics
- **Prometheus** → Metrics collection engine
- **Node Exporter** → CPU, RAM, disk monitoring
- **cAdvisor** → Container performance monitoring

👉 Provides real-time visibility of system health and performance.

---

## 💾 Backup & Recovery

- Automated daily backups using Cron jobs
- Backup includes:
  - PostgreSQL database
  - Odoo filestore
  - Configuration files
- Local storage backup system implemented
- Designed for easy extension to cloud storage

---

## 📸 Screenshots

### 🖥️ Odoo Dashboard
![Odoo Dashboard](screenshots/odoo-dashboard.PNG)

### 📊 Grafana Monitoring
![Grafana](screenshots/grafana.PNG)

### 📈 Prometheus Targets
![Prometheus](screenshots/permetheus.PNG)

### 🐳 Docker Containers
![Docker](screenshots/docker-ps.PNG)

---

## 🚀 Future Improvements

- [ ] Replace self-signed SSL with Let's Encrypt (production domain)
- [ ] Add CI/CD pipeline using GitHub Actions
- [ ] Implement centralized logging (ELK stack)
- [ ] Add high availability (multi-node architecture)
- [ ] Integrate alerting system in Grafana

---

## 🧑‍💻 Author

**Gheddab Mohamed Amine**

- 📍 Algeria 🇩🇿
- 🐙 GitHub: [github.com/MaminoMax](https://github.com/MaminoMax)
- 💼 LinkedIn: [linkedin.com/in/mohamed-amine-gheddab-0b9478252](https://linkedin.com/in/mohamed-amine-gheddab-0b9478252)

---

⭐ If you found this project useful or interesting, please consider giving it a ⭐ on GitHub.
