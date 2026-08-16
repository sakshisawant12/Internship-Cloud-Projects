# ☁️ AWS S3 Static Website Hosting — Cloud Engineer Portfolio

## 📌 Project Overview

This project demonstrates the deployment of a personal **AWS Cloud Engineer Portfolio Website** using **Amazon S3 Static Website Hosting**.

The portfolio was designed using HTML5 and CSS3 and deployed as a static website through Amazon S3.

The website contains:

- 👩‍💻 Personal profile
- ☁️ AWS Cloud Engineer career focus
- 🛠️ Technical skills
- 🚀 AWS Cloud projects
- 🎓 Learning credentials
- 🌐 Networking and Linux knowledge
- 🔗 GitHub and LinkedIn links

---

# 🎯 Project Objective

The main objective of this project was to understand how Amazon S3 can be used to host a publicly accessible static website.

Through this project, I practiced:

- Creating an S3 bucket
- Uploading website files
- Configuring public access
- Creating an S3 bucket policy
- Enabling static website hosting
- Configuring an index document
- Deploying a real portfolio website
- Testing the website through the S3 website endpoint

---

# 🏗️ Architecture

```text
                         🌐 Internet
                              │
                              ▼
                  ┌─────────────────────┐
                  │      Amazon S3      │
                  │  Static Website     │
                  │      Hosting        │
                  └──────────┬──────────┘
                             │
                    ┌────────┴────────┐
                    │                 │
                    ▼                 ▼
               index.html        profile.jpg
                    │
                    ▼
           AWS Cloud Engineer
                Portfolio
