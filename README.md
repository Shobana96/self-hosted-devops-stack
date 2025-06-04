# 🛠️ Self-Hosted DevOps Stack

This project sets up a complete self-hosted DevOps environment using:

- **Gitea** – Lightweight Git service
- **Grafana** – Metrics visualization and monitoring
- **Authelia** – Single Sign-On (SSO) authentication portal
- **Caddy/Nginx** – Reverse proxy for HTTPS and routing
- **Docker Compose** – Service orchestration
- **Terraform** – Infrastructure automation (optional)

---

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
├── README.md
└── report.md
