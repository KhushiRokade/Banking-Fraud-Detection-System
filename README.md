# 🚀 Digital Banking Fraud Detection & Simulation Engine

## 📌 Project Overview

The **Digital Banking Fraud Detection & Simulation Engine** is an AI-powered system designed to simulate banking transactions and detect fraudulent activities in real-time.

It integrates **rule-based detection** with **machine learning models** to identify suspicious patterns, generate alerts, and provide insights through dashboards.

Fraud detection systems are essential in modern banking due to increasing financial crimes and evolving fraud patterns, requiring intelligent and adaptive solutions.

---

## 🎯 Objectives

* Simulate real-world banking transactions (normal + fraudulent)
* Detect fraud using **rule-based logic**
* Integrate **Machine Learning models** for prediction
* Generate **risk scores and alerts**
* Provide **real-time monitoring dashboard**
* Enable **API-based transaction processing**

---

## 🏗️ System Architecture

```
Simulation Engine
        │
        ▼
API Gateway (Transaction Ingestion)
        │
        ▼
Anomaly Detection Core (Rules + ML)
        │
        ▼
Alert & Risk Management Service
        │
        ▼
Dashboard & Monitoring Hub
```

---

## 🔄 Data Flow

1. Transaction generated (simulation or external source)
2. API Gateway receives transaction
3. Transaction stored in database
4. Detection Core evaluates risk
5. Fraud detected → Alert generated
6. Dashboard displays alerts & analytics

---

## 🧩 Modules

### 🔹 1. Transaction Simulation Engine

* Generates synthetic transactions
* Supports fraud scenarios:

  * High Amount (> ₹100000)
  * Impossible Travel
  * Rapid Transactions
  * High-risk categories (Crypto, Gambling)
  * New Device detection

---

### 🔹 2. Transaction API Gateway

* Entry point of the system
* Validates and stores transactions
* Exposes REST APIs

**Endpoint:**

```
POST /api/v1/transactions
```

---

### 🔹 3. Anomaly Detection Core

* Applies rule-based detection
* Integrates ML model
* Calculates risk score

**Risk Formula:**

```
Final Risk = (Rule Score × 0.7) + (ML Score × 0.3)
```

---

### 🔹 4. Alert & Analytics Service

* Stores fraud alerts
* Provides monitoring APIs

**Endpoints:**

```
GET /api/v1/alerts
GET /api/v1/alerts/high-risk
GET /api/v1/alerts/by-account/{accountId}
GET /api/v1/metrics
```

---

### 🔹 5. ML Plugin Service

* Trains fraud detection model
* Predicts fraud probability

**Endpoint:**

```
POST /ml/predict
```

**Response:**

```json
{
  "fraudProbability": 0.82
}
```

---

## 📊 Features

* Fraud simulation engine
* Rule-based anomaly detection
* ML-based fraud prediction
* Real-time fraud alerts
* Dashboard visualization
* REST API integration
* Risk scoring system

---

## 🗂️ Transaction Data Model

```json
{
  "transactionId": "STRING",
  "accountId": "STRING",
  "customerId": "STRING",
  "transactionType": "DEBIT/CREDIT",
  "channel": "MOBILE_APP/WEB/ATM",
  "amount": 0.0,
  "currency": "INR/USD",
  "merchantId": "STRING",
  "merchantCategory": "STRING",
  "merchantCountry": "STRING",
  "customerCountry": "STRING",
  "deviceId": "STRING",
  "ipAddress": "STRING",
  "timestamp": "YYYY-MM-DDTHH:MM:SS"
}
```

---

## 🛠️ Tech Stack

| Layer      | Technology                     |
| ---------- | ------------------------------ |
| Backend    | Spring Boot (Java)             |
| Database   | MySQL                          |
| ML Service | Python (FastAPI, Scikit-learn) |
| Frontend   | React.js                       |
| Tools      | Postman, Git, VS Code          |

---

## 📅 Project Milestones

| Milestone | Description                        |
| --------- | ---------------------------------- |
| Week 1–2  | Setup & Data Modeling              |
| Week 3–4  | Simulation Engine & Detection Core |
| Week 5–6  | Dashboard & API Integration        |
| Week 7–8  | ML Integration & Deployment        |

---

## ⚙️ Setup & Installation

### 🔹 Clone Repository

```bash
git clone https://github.com/KhushiRokade/Banking-Fraud-Detection-System.git
cd Banking-Fraud-Detection-System
```

---

### 🔹 Backend Setup (Spring Boot)

```bash
cd backend
mvn clean install
mvn spring-boot:run
```

---

### 🔹 ML Service (FastAPI)

```bash
cd ml-service
pip install -r requirements.txt
uvicorn app:app --reload
```

---

### 🔹 Frontend Setup

```bash
cd frontend
npm install
npm start
```

---

## 🧪 Testing

* Use **Postman** for API testing
* Simulate transactions using Simulation Engine
* Monitor alerts in dashboard

---

## 📈 Future Enhancements

* Real-time streaming using Kafka
* Deep Learning-based fraud detection
* Cloud deployment (AWS/Azure)
* Multi-bank integration

---

## 👨‍💻 Author

**Khushi Rokade**
B.Tech Final Year
Full-Stack & ML Enthusiast
