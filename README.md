# 🏦 SpringBoot BankApp – AI‑Integrated Banking Application

## 🚀 Overview
SpringBoot BankApp is a **containerized banking application** built with **Spring Boot** and **MySQL**, orchestrated using **Docker Compose**.  
It integrates **Ollama**, an AI LLM chat model, directly inside the backend to provide **transaction intelligence** and conversational banking features.

This project demonstrates:
- **Backend (Spring Boot)** → Core banking logic & REST APIs  
- **Database (MySQL)** → Persistent storage  
- **AI Integration (Ollama)** → Embedded LLM that enhances banking operations with natural language insights  

---

## 🏗️ Architecture
Spring Boot Backend (Banking + Ollama AI) → MySQL Database

Code

👉 Ollama runs inside the backend, making the application **AI‑powered** rather than just a standard CRUD service.

---

## 🛠️ Tech Stack
- **Backend:** Java 21, Spring Boot 3, Hibernate/JPA  
- **Database:** MySQL 8.0  
- **AI Integration:** Ollama (LLM chat model embedded in backend)  
- **DevOps:** Docker, Docker Compose  

---

## 📂 Project Structure
.
├── src/                  # Spring Boot source code
├── pom.xml               # Maven dependencies
├── Dockerfile            # Backend container build
├── docker-compose.yaml   # Multi-service orchestration
└── README.md             # Documentation

Code

---

## ⚙️ Setup & Run

### 1. Clone the repository

git clone https://github.com/nikscool24/SpringBoot-BankApp.git
cd SpringBoot-BankApp

2. Build and start services
docker-compose up -d --build

3. Verify containers
docker ps

You should see:

bankapp → Spring Boot backend (with Ollama integrated) on port 8080

bankapp-mysql → MySQL DB on port 3306

4. Access the app
Backend API → http://localhost:8080/api/...

MySQL → localhost:3306 (user: root, password: Test@123)

🧪 Health Checks
MySQL service includes a healthcheck using mysqladmin ping to ensure DB readiness.

Backend waits for MySQL to be healthy before initialization.

🧠 Ollama AI Integration
Ollama is an AI‑integrated LLM chat model that runs inside the banking app.
It provides transaction insights and allows users to interact with their account using natural language.

🔎 Capabilities
Balance Queries: Responds with your current account balance.

Transaction Origins: Explains where incoming money comes from (e.g., identifies the sender).

Outgoing Transfers: Tracks when you send money and identifies the recipient.

Conversational Banking: Enables natural language queries about balances, transactions, and transfers.

📌 Example Usage
“What’s my current balance?” → Ollama responds with your account balance.

“Who sent me ₹5,000 yesterday?” → Ollama identifies the sender.

“I transferred money to Rahul — confirm the details.” → Ollama confirms the recipient and transaction.

📖 Features
Banking operations via Spring Boot REST API

Persistent MySQL storage with Docker volumes

Environment‑driven configuration (MYSQL_HOST, MYSQL_PORT, etc.)

AI‑powered transaction assistant with Ollama integrated directly into backend



📌 How to Showcase on CV
You can describe this project as:

“Developed a containerized Spring Boot banking application with MySQL using Docker Compose. Integrated Ollama LLM chat model directly into the backend to provide AI‑powered transaction intelligence, enabling natural language queries for balances, transaction origins, and transfers. Implemented health checks, persistent volumes, and environment‑based configuration for reliable orchestration.”