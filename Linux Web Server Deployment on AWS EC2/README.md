# 🚀 AWS EC2 Nginx Website Deployment

## 📌 Project Overview

This project demonstrates the deployment of a custom website on an **AWS EC2 instance** running **Red Hat Enterprise Linux**. Nginx was installed and configured as the web server, and the custom website was hosted using the EC2 instance's public IP.

## 🏗️ Architecture

```text
                    Internet
                       │
                       │ HTTP :80
                       ▼
              ┌─────────────────┐
              │ Security Group  │
              │                 │
              │ SSH :22 → My IP │
              │ HTTP :80        │
              │ HTTPS :443      │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │   AWS EC2       │
              │                 │
              │ Red Hat Linux   │
              │                 │
              │     Nginx       │
              │       │         │
              │       ▼         │
              │   index.html    │
              └─────────────────┘
                       │
                       ▼
                Custom Website
