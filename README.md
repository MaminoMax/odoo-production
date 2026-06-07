# 🚀 Odoo 17 Production Setup

![Odoo](https://img.shields.io/badge/Odoo-17-purple?style=for-the-badge&logo=odoo)
![Docker](https://img.shields.io/badge/Docker-Compose-blue?style=for-the-badge&logo=docker)
![Nginx](https://img.shields.io/badge/Nginx-green?style=for-the-badge&logo=nginx)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Server-orange?style=for-the-badge&logo=ubuntu)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue?style=for-the-badge&logo=postgresql)

> A fully production-ready Odoo 17 ERP deployment on a real Ubuntu Server, with complete security layers, automated monitoring, and backup system.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Deployment Stages](#deployment-stages)
- [Architecture](#architecture)
- [Technologies](#technologies)
- [Security](#security)
- [Monitoring](#monitoring)
- [Backup](#backup)
- [Screenshots](#screenshots)

---

## 🧩 Overview

This project is a complete, professional **Odoo 17 ERP** production setup built from scratch on a bare Ubuntu Server. Every layer — from containerization to security hardening and monitoring — was manually configured and tested.

---

## 🗺️ Deployment Stages

| # | Stage | Description |
|---|-------|-------------|
| 1 | Ubuntu Server | OS installation and initial configuration |
| 2 | Docker + Docker Compose | Service isolation with containers |
| 3 | Project Structure | Organized /opt/odoo directory layout |
| 4 | odoo.conf | Odoo configuration file setup |
| 5 | Docker Compose + Launch | Bringing up all services |
| 6 | iptables Firewall | Port-level network protection |
| 7 | Nginx | Reverse proxy configuration |
| 8 | SSL Self-Signed | ⚠️ SSL is self-signed (Let's Encrypt will be added with domain)|
| 9 | Nginx + HTTPS | Full HTTPS setup and HTTP redirect |
| 10 | Backup System + Cron | Automated daily backups |
| 11 | Fail2ban | Brute force attack protection |
| 12 | Monitoring Stack | Full observability with Grafana & Prometheus |

---

## 🏗️ Architecture

```
Internet
    │
    ▼
[ Nginx :443 HTTPS ]
    │
    ▼
[ Odoo 17 :8069 ]
    │
    ▼
[ PostgreSQL 15 :5432 ]
```

**Monitoring Stack:**
```
[ cAdvisor ]       ──┐
[ Node Exporter ]  ──┼──► [ Prometheus ] ──► [ Grafana ]
[ Odoo Metrics ]   ──┘
```

---

## 🛠️ Technologies

| Technology | Purpose |
|-----------|---------|
| Ubuntu Server 22.04 | Operating System |
| Docker + Docker Compose | Container Management |
| Odoo 17 | ERP Application |
| PostgreSQL 15 | Database |
| Nginx | Reverse Proxy |
| SSL Self-Signed | HTTPS Encryption |
| iptables | Firewall |
| Fail2ban | Intrusion Prevention |
| Prometheus | Metrics Collection |
| Grafana | Data Visualization |
| cAdvisor | Container Monitoring |
| Node Exporter | Server Resource Monitoring |
| Bash + Cron | Automated Backup |

---

## 🔒 Security

- **HTTPS** — All traffic is encrypted via SSL
- **Nginx Reverse Proxy** — Internal services are not directly exposed
- **iptables** — Only necessary ports are open
- **Fail2ban** — Automatic IP banning after failed login attempts
- **PostgreSQL** — Isolated inside Docker with no external port exposure
- **Separate Docker Volumes** — Data persists safely across restarts

---

## 📊 Monitoring

| Service | Description |
|---------|-------------|
| Grafana | Interactive dashboards and visualization |
| Prometheus | Metrics collection and storage |
| cAdvisor | Docker container performance metrics |
| Node Exporter | Server resources: CPU, RAM, Disk, Network |

---

## 💾 Backup System

- Automated daily backups via **Cron Job**
- Covers: PostgreSQL database + Odoo filestore + config files
- Stored locally with option to push to cloud storage

---

## 🖥️ Screenshots

### Odoo Dashboard
![Odoo Dashboard](screenshots/odoo-dashboard.png)

### Grafana Monitoring
![Grafana](screenshots/grafana.png)

### Prometheus Targets
![Prometheus](screenshots/prometheus.png)

### Docker Containers
![Docker](screenshots/docker-ps.png)
---

## 👤 Author

**Your Name**
- 📍 Algeria 🇩🇿
- 💼 LinkedIn: [linkedin.com/in/mohamed-amine-gheddab-0b9478252](#)
- 🐙 GitHub: [github.com/MaminoMax](#)

---

⭐ If you found this useful, please give it a star!
