# End-to-End SMS & Email Spam-Ham Classifier

[![Live Demo](https://img.shields.io/badge/Live_Demo-Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)](https://spam-ham-classifier-6yu2.onrender.com/)
[![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/r/sanjaysahu121/spam-ham-app)
[![FastAPI](https://img.shields.io/badge/FastAPI-Production_Ready-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

An end-to-end NLP-driven Machine Learning web application designed to classify incoming text, SMS, or email messages as **Spam** or **Ham** in real time. Built with **FastAPI**, containerized using **Docker**, and deployed live in production on **Render**.

---

## 🌐 Live Application & Access

The application is deployed and publicly accessible 24/7:

* **Production URL:** [https://spam-ham-classifier-6yu2.onrender.com/](https://spam-ham-classifier-6yu2.onrender.com/)
* **Container Registry:** [Docker Hub Image Repository](https://hub.docker.com/r/sanjaysahu121/spam-ham-app)

---

## 📌 Problem Statement

Unsolicited communications (phishing scams, fraudulent promotions, financial deception) create significant security risks and operational noise across communication channels. This project provides a scalable, automated machine learning pipeline engineered to ingest raw unstructured text, extract meaningful linguistic patterns, and classify messages with extreme precision—prioritizing zero false positives on legitimate (Ham) messages.

---

## 🏗️ Architecture & Pipeline Components

The application follows modular, production-grade MLOps architectural principles:

* **Data Ingestion:** Automated data retrieval, train-test splitting, and feature separation.
* **Data Validation:** Schema auditing, domain drift detection, and data-integrity verification.
* **Data Transformation:** Text preprocessing (tokenization, stopword filtering, lemmatization) and TF-IDF matrix generation.
* **Model Training & Hyperparameter Tuning:** Systematic hyperparameter optimization across multiple algorithms using `GridSearchCV`.
* **Model Evaluation:** Performance assessment focusing on Precision, Recall, and F1-Score to protect legitimate communications.
* **Model Pusher & Artifact Registry:** Serialized storage of trained weights and vectorizers for low-latency inference.
* **Logging & Exception Handling:** Centralized logging module and custom exception handlers for robust monitoring and debugging.

---

## ⚙️ Tech Stack & Infrastructure

* **Language:** Python
* **Web Framework:** FastAPI, Uvicorn, Jinja2 Templates
* **Machine Learning:** Scikit-Learn (`scikit-learn==1.8.0`), NumPy, Pandas
* **Containerization:** Docker (`sanjaysahu121/spam-ham-app:latest`)
* **Deployment & Cloud:** Render Web Services, AWS EC2 (tested & verified)
* **Database & Storage:** MongoDB Atlas

---

## 🤖 Models Benchmarked

The pipeline trains and benchmarks multiple algorithmic approaches:

* **Multinomial Naive Bayes (`MultinomialNB`)** — Baseline model optimized for discrete word frequency distributions.
* **Gaussian Naive Bayes (`GaussianNB`)** — Evaluation across continuous feature representations.
* **Support Vector Classifier (`SVC`)** — High-dimensional hyperplane optimization for complex semantic embeddings.

*The model demonstrating the highest precision and cross-validated F1-score is automatically packaged into the production container for live scoring.*

---

## 🚀 How to Launch & Run Locally

### Method 1: Launch via Docker (Fastest)

Pull and start the pre-built production container directly from Docker Hub:

```bash
docker pull sanjaysahu121/spam-ham-app:latest
docker run -d -p 5000:5000 --name spam_detector sanjaysahu121/spam-ham-app:latest

```


### Method 2: Launch from Source Code

Clone the repository:

```bash
git clone [https://github.com/sanjaysahu121/Spam-Ham-Detection-FastAPI.git](https://github.com/sanjaysahu121/Spam-Ham-Detection-FastAPI.git)
cd Spam-Ham-Detection-FastAPI

```

Create and activate a virtual environment:

```bash
python -m venv myvenv

# Windows:
myvenv\Scripts\activate

# Linux/macOS:
source myvenv/bin/activate

```

Install dependencies:

```bash
pip install -r requirements.txt

```

Launch the FastAPI application:

```bash
uvicorn app:app --host 0.0.0.0 --port 5000 --reload

```

Open your browser and navigate to:

```text
http://localhost:5000

```

---

## 👤 Author & Project Metadata

* **Author:** Sanjay Kumar
* **Role:** Machine Learning & Data Science Engineer
* **Live Demo:** [https://spam-ham-classifier-6yu2.onrender.com/](https://spam-ham-classifier-6yu2.onrender.com/)
* **Docker Registry:** [Docker Hub Repository](https://www.google.com/url?sa=E&source=gmail&q=https://hub.docker.com/r/sanjaysahu121/spam-ham-app)
* **Year:** 2026

```

```
