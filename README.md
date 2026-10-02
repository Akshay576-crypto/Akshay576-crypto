<h1 align="center">Akshay Sapariya</h1>

<p align="center">
  <b>Machine Learning • Data Science • ML Systems • MLOps</b>
</p>

<p align="center">
  I build ML systems with an interest in what happens beyond model training —
  when data changes, models degrade, and systems need to be monitored, evaluated, and improved.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/akshay-sapariya-438747375/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:ak.56sapariya@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact-EA4335?logo=gmail&logoColor=white" />
  </a>
  <a href="https://hashnode.com/@akshay0884">
    <img src="https://img.shields.io/badge/Hashnode-Technical%20Writing-2962FF?logo=hashnode&logoColor=white" />
  </a>
</p>

---

## About

My main focus is **Machine Learning and Data Science**, especially the parts that become important after a model leaves the notebook.

Most of my recent work has involved **fraud detection, data quality, model evaluation, data drift, retraining, monitoring, and deployment**.

I like understanding not only why a model makes a prediction, but what happens to the complete system when new data arrives and the assumptions used during training start changing.

Alongside ML, I explore **RAG, semantic retrieval, and agentic workflows** through Cognexa.

---

## Tech I Work With

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-4479A1?logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white" />
</p>

---

## Selected Systems

### FraudOPS — UPI Fraud Detection & MLOps

[![FraudOPS Tests](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml/badge.svg)](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml)

An ML system I built to understand what happens when a fraud model encounters changing transaction patterns.

Instead of stopping after training the first model, I created drift scenarios, measured how performance changed, analyzed where the model failed, and retrained it using newer data.

| Stage | F1 Score |
|:---|---:|
| Initial Model | **0.8093** |
| Drift Scenario | **0.5366** |
| Retrained Model | **0.9965** |

**What I worked with**

`Fraud Detection` · `Feature Engineering` · `Random Forest` · `PR-AUC` · `Drift Analysis` · `Retraining` · `FastAPI`

The API now also has an automated test suite covering model/API behavior and request validation, executed through **GitHub Actions CI** on pushes and pull requests to `main`.

#### Deployment

I separated the static frontend from the ML inference backend:

```text
User
 │
 ▼
AWS S3 Static Frontend
 │
 ▼
FastAPI Backend — Render
 │
 ▼
ML Model
 │
 ▼
Fraud Probability / Risk Decision
```

This keeps the static frontend on object storage while the backend handles the part that actually requires computation.

**[Source Code](https://github.com/Akshay576-crypto/upi-fraud-mlops)** · **[Live Demo](http://upi-fraud-mlops.s3-website.eu-north-1.amazonaws.com/)**

---

### DQM — ML Pipeline Data Quality Monitoring

A monitoring system built around a simple question:

> **What happens if poor-quality data reaches an ML pipeline before anyone notices it?**

DQM analyzes incoming datasets before they move further through the pipeline.

**What it includes**

- Automatic data profiling
- Missing-value and duplicate detection
- Isolation Forest based anomaly detection
- Data-quality scoring
- Pipeline-run history
- MySQL persistence
- FastAPI backend
- PDF quality reports

`Data Quality` · `Anomaly Detection` · `Isolation Forest` · `FastAPI` · `MySQL`

**[Explore DQM](https://github.com/Akshay576-crypto/ML-Pipeline-DQM)**

---

### Cognexa — Research & Retrieval System

Cognexa is where I explore another side of intelligent systems: **retrieval, semantic search, RAG, and agentic workflows**.

My work around Cognexa includes:

- Retrieval-Augmented Generation
- Semantic retrieval
- Vector search
- Qdrant
- Sentence Transformers
- FastAPI
- LLM integration
- Agentic workflows
- Tool routing

I treat these as additional tools for solving problems rather than replacements for strong Machine Learning fundamentals.

`RAG` · `Vector Search` · `Qdrant` · `Semantic Retrieval` · `Agentic AI`

**[Explore Cognexa](https://github.com/Akshay576-crypto/Cognexa)**

---

## More Engineering Work

I also use this GitHub to explore **data pipelines, backend systems, ML experiments, and engineering ideas**.

One example is my **Self-Healing ETL Pipeline**, built around detecting and handling data-pipeline problems while maintaining pipeline-run history.

**[View Live ETL Dashboard](https://selfhealingpipelinedashboard-et3gyntpk5eyzm28x9rkgc.streamlit.app/)**

**[Explore All Repositories](https://github.com/Akshay576-crypto?tab=repositories)**

---

## Technical Writing

I write about concepts I'm learning and problems I encounter while building ML systems.

### Self-Learning ML Models

How data quality, drift, retraining, and monitoring connect across an ML lifecycle.

**[Read on Hashnode](https://self-trainig-ml-model.hashnode.dev/self-learning-ml-model)**

### Understanding Confusion Matrix, MSE & RMSE

Breaking down model-evaluation concepts using intuition, mathematics, and small examples.

**[Read on Hashnode](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-mse-rmse-explained-like-you-re-5)**

### Precision, Recall & F1

Understanding how these classification metrics depend on each other and how decision thresholds affect their trade-offs.

**[Read on Hashnode](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-pt-2)**

**[Explore More Technical Writing](https://hashnode.com/@akshay0884)**

---

## Currently Going Deeper Into

<p>
  <img src="https://img.shields.io/badge/Deep%20Learning-Foundations-6A5ACD" />
  <img src="https://img.shields.io/badge/TensorFlow-Learning-FF6F00?logo=tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Statistics-%26%20Probability-4B8BBE" />
  <img src="https://img.shields.io/badge/ML%20System%20Design-Learning-555555" />
</p>

I'm currently strengthening my foundations in **Deep Learning, TensorFlow, statistics, probability, and ML system design** while continuing to build with classical Machine Learning.

---

## Connect

<p>
  <a href="https://www.linkedin.com/in/akshay-sapariya-438747375/">
    <img src="https://img.shields.io/badge/LinkedIn-Akshay%20Sapariya-0A66C2?logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:ak.56sapariya@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-ak.56sapariya%40gmail.com-EA4335?logo=gmail&logoColor=white" />
  </a>
  <a href="https://hashnode.com/@akshay0884">
    <img src="https://img.shields.io/badge/Hashnode-%40akshay0884-2962FF?logo=hashnode&logoColor=white" />
  </a>
</p>