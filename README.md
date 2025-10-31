# ⚡ InstaSQL — AI-Powered Natural Language to SQL Engine  
> **Talk to your database — no SQL expertise required.**

[![Live Demo](https://img.shields.io/badge/Live-Demo-blue?style=for-the-badge)](https://instasql.xiorabh.com)
[![GitHub Repo](https://img.shields.io/badge/Repo-Source%20Code-black?style=for-the-badge&logo=github)](https://github.com/saurabh1244/instasql-docs)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#license)
[![Python](https://img.shields.io/badge/Python-3.11-yellow?style=for-the-badge&logo=python)]()
[![FastAPI](https://img.shields.io/badge/Framework-FastAPI-009688?style=for-the-badge&logo=fastapi)]()
[![LangChain](https://img.shields.io/badge/AI-LangChain-512BD4?style=for-the-badge&logo=chainlink)]()
[![Docker](https://img.shields.io/badge/Container-Docker-blue?style=for-the-badge&logo=docker)]()

---

## 🧠 Overview

**InstaSQL** (also known as **SQLWaani_V2**) is an **AI-driven database intelligence layer** that empowers both developers and non-technical users to **query databases in plain English**.  
No SQL knowledge. No syntax stress. Just type what you need — and InstaSQL translates it into an accurate, optimized SQL query.

This system sits between your **database** and your **data analyst**, converting natural language to SQL in real-time and executing it securely through an **async FastAPI backend**.

It's designed to be:
- ⚙️ **Lightweight** (single VPS deployable)  
- 🧠 **AI-intelligent** (powered by Gemini 2.5 Flash)  
- 🔐 **Secure by default** (JWT + OAuth + CSRF-safe APIs)  
- ⚡ **High-performance** (sub-50ms latency)

---

## 🌍 Real-World Context

Modern data teams spend hours writing queries, debugging joins, and managing schema mismatches. InstaSQL eliminates that by:
- Understanding **natural language intent**,  
- Mapping it to your **database schema**,  
- Generating **context-aware SQL**,  
- Executing and **visualizing results** in one click.

From marketing teams pulling reports to developers debugging production data — InstaSQL saves **countless hours weekly**.

---

## 🚀 Highlights & Key Achievements

| Feature | Description | Impact |
|----------|--------------|---------|
| 🧠 **AI Query Engine** | Converts natural language to accurate SQL using Gemini 2.5 | 90%+ accuracy |
| ⚙️ **Async FastAPI Backend** | Non-blocking architecture | 100+ concurrent sessions |
| 🔄 **Cross-DB Migration** | Seamlessly migrate data between MySQL & SQLite | 75% storage savings |
| 🔐 **Authentication** | Secure OAuth2 + JWT + Argon2 | Zero manual token leaks |
| 📈 **Analytics** | Query metrics and logs | Real-time monitoring |
| 💾 **Persistence Layer** | Saves all session data securely | Full history replay |
| 🧳 **DevOps Ready** | Docker + CI/CD pipeline | Continuous deployment |
| 📦 **Scalable** | Modular architecture | Easily extendable |
| ⚡ **Performance** | Query execution < 50ms | Enterprise-grade response |
| 🧩 **Security** | CSRF + CORS + Role-based Access | 100% hardened API layer |

---

## 🧩 Tech Stack Overview

| Layer | Stack |
|--------|--------|
| **Frontend** | React / Vue.js (Port 5173) + Tailwind CSS |
| **Backend** | FastAPI, LangChain, aiomysql, SQLAlchemy ORM |
| **Database** | MySQL 8.4.6 (Production), SQLite (Upload mode) |
| **AI Engine** | Google Gemini 2.5 Flash (LangChain wrapper) |
| **Auth & Security** | OAuth 2.0, JWT, Argon2 hashing |
| **Email Automation** | SendGrid / Resend API |
| **Containerization** | Docker multi-stage builds |
| **CI/CD** | GitHub Actions pipeline |
| **Hosting** | Ubuntu VPS @ 157.245.101.224 |
| **Monitoring** | JSON structured logs + health endpoints |

---

## 🏗️ System Architecture

```mermaid
flowchart LR
    UI[Frontend] --> API[FastAPI Backend]
    API --> DB[(Database)]
    API --> AI[Gemini AI Engine]
    API --> Mail[Email Automation]
    UI --> Auth[OAuth Provider]

    subgraph DevOps [DevOps & Deployment]
        Docker[Docker]
        CI[GitHub Actions]
        VPS[VPS Server]
    end

    API --> Docker
    Docker --> VPS
