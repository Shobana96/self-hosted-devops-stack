# 🛠️ Self-Hosted DevOps Stack

This project sets up a complete self-hosted DevOps environment using:

- **Gitea** – Lightweight Git service
- **Grafana** – Metrics visualization and monitoring
- **Authelia** – Single Sign-On (SSO) authentication portal
- **Caddy/Nginx** – Reverse proxy for HTTPS and routing
- **Docker Compose** – Service orchestration
- **Terraform** – Infrastructure automation (optional)

---

**Architecture:**

Browser --> Caddy --> Authelia --> Gitea --> Grafana --> Access

## 📦 Tech Stack

| Tool       | Purpose                                 |
|------------|-----------------------------------------|
| Gitea      | Git repository management               |
| Grafana    | Monitoring dashboards                   |
| Authelia   | Authentication & SSO                    |
| Nginx/Caddy| Reverse proxy with TLS                  |
| Docker     | Containerization                        |
| Terraform  | Infrastructure as code (optional setup) |

---

## 📁 Project Structure

project-root/
├── docker-compose.yml
├── .env
├── reverse-proxy/
│ └── nginx/
│ └── nginx.conf
├── gitea/
│ └── config/
├── grafana/
│ └── provisioning/
├── authelia/
│ ├── configuration.yml
│ ├── users_database.yml
├── terraform/
│ ├── main.tf
│ ├── variables.tf
│ └── outputs.tf


---

## 🚀 Getting Started

### Prerequisites

- macOS with:
  - Docker Desktop
  - Terraform installed
- Basic knowledge of:
  - Docker & Linux CLI
  - SSO concepts
  - Reverse proxies (TLS, HTTPS)

---

## 🛠️ Setup Instructions

### 1. Gitea

```bash
docker run --rm -it -p 3001:3000 gitea/gitea:1.19

├── README.md
└── report.md

Visit: http://localhost:3001

Use SQLite, set App URL, and admin credentials


2. Grafana
docker run -d \
  --name=grafana \
  -p 3000:3000 \
  -v /path/to/grafana.ini:/etc/grafana/grafana.ini \
  grafana/grafana

Make sure grafana.ini is a valid file, not a folder

Visit: http://localhost:3000

3. Authelia + Reverse Proxy
docker run -d \
  --name authelia \
  -v ~/authelia-config:/config \
  -p 9091:9091 \
  authelia/authelia:latest

Ensure configuration.yml and users_database.yml are in place

Error to fix: "unable to retrieve session cookie domain..."

Troubleshooting

Grafana
Ensure config path is shared:
Docker > Preferences > Resources > File Sharing

Authelia
Validate config:
docker run --rm -v ~/authelia-config:/config authelia/authelia:latest authelia validate-config
Session cookie error pending resolution.

👤 Author
Shobana Raghu
https://www.linkedin.com/in/shobanaraghu/






