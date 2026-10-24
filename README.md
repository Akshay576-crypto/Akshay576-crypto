<div align="center">

# Akshay Sapariya

### Machine Learning · Data Science · Agentic AI · GenAI

Building ML systems, data pipelines, and multi-agent applications—with a focus on how they work beyond a notebook.

[LinkedIn](https://www.linkedin.com/in/akshay-sapariya-438747375/) · [Technical Writing](https://hashnode.com/@akshay0884) · [Email](mailto:ak.56sapariya@gmail.com)

</div>

---

## About

I focus on **Machine Learning and Data Science**, particularly model evaluation, data quality, changing data distributions, and the engineering around ML applications.

I also build with **Generative AI and agentic workflows**. Through Cognexa, I explore how multiple agents can pass shared memory and findings between steps, use tools to investigate a problem, and build on previous work instead of treating every prompt as an isolated task.

This GitHub is where I share the systems I build, the experiments behind them, and what I learn along the way.

## Technology Stack

### ML & Data Science

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)

### GenAI & Agentic Systems

![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=chainlink&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square)
![Sentence Transformers](https://img.shields.io/badge/Sentence_Transformers-5A45FF?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-Retrieval%20%26%20Generation-7057FF?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square)

### Backend, Testing & Infrastructure

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

---

## Selected Systems

## Cognexa — Multi-Agent Research, Consulting & Intelligence Platform

**Core idea: agents pass shared memory and findings from one step to another.**

Cognexa uses a LangGraph-based workflow to coordinate agents around research and business problems. Findings from one step become shared context for the next agent, allowing the workflow to build on earlier research instead of treating every LLM call as a separate, context-free prompt.

The system can combine research, retrieval, and tool execution. For example, web-search and Yahoo Finance tools help investigate current information; the document workflow uses Qdrant-backed retrieval for PDF question answering and research-paper validation, cross-checking claims against external sources and highlighting potential issues in an analysis.

A reporting workflow turns findings into PDF reports, PowerPoint presentations, and a KPI dashboard. The project also includes a FastAPI backend with JWT authentication.

**What I worked with**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

The project includes 190 Pytest tests. In the project work, API response time was reduced from approximately 30 seconds to 15 seconds.

[**Source Code →**](https://github.com/Akshay576-crypto/Cognexa) · [**Live UI Showcase →**](http://cognexa-static.s3-website.eu-north-1.amazonaws.com/)

> RAG is one capability within Cognexa—not the whole project. The broader focus is coordinating agents, passing context between steps, using tools, and producing useful outputs from the combined workflow.

---

## FraudOPS — UPI Fraud Detection, Drift Evaluation & Monitoring

I built FraudOPS to explore what happens when transaction patterns change after a fraud model has been trained.

The Random Forest model was trained on **15,000+ synthetic UPI transactions**. I evaluated its baseline performance, introduced a simulated drift scenario, and compared the results with a retrained model.

| Experiment | F1 Score | PR-AUC |
|:---|---:|---:|
| Initial model | 0.8093 | 0.9121 |
| Simulated drift | 0.5366 | 0.4692 |
| Retrained model | 0.9965 | 1.0000 |

> **Experiment context:** The dataset and drift scenarios are synthetic. The retrained result represents recovery within this controlled experiment, not expected performance on real-world financial transactions.

The FastAPI prediction endpoint returns a fraud probability and risk decision. The frontend is hosted on AWS S3, while the API runs separately on Render.

**CI/CD in practice:** GitHub Actions runs automated tests when changes are pushed to the repository. Tests cover prediction behavior, request validation, error handling, and model status.

[![FraudOPS Tests](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml/badge.svg)](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml)

![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

[**Source Code →**](https://github.com/Akshay576-crypto/upi-fraud-mlops) · [**Live Demo →**](http://upi-fraud-mlops.s3-website.eu-north-1.amazonaws.com/)

---

## DQM — ML Pipeline Data Quality Monitoring

DQM adds a validation layer before poor-quality data reaches downstream analytics or ML processing. It profiles incoming datasets, identifies missing values and duplicates, detects unusual records, calculates a quality score, and stores run history.

The pipeline uses Isolation Forest for anomaly detection and includes a FastAPI backend, MySQL persistence, dashboard trends, and PDF quality reports.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

[**Explore DQM →**](https://github.com/Akshay576-crypto/ML-Pipeline-DQM)

---

## Backend & Data Engineering

### Athere — FastAPI Chat Application

A chat application built while exploring API routing, authentication, database-backed application logic, and separation of backend responsibilities.

**Stack:** Python · FastAPI · REST APIs · Authentication · MySQL

[**Explore Athere →**](https://github.com/Akshay576-crypto/chatting-app-FastAPI)

### Self-Healing ETL Pipeline

A data-engineering experiment focused on identifying problematic records during a pipeline run, separating them from clean records, and keeping run history for troubleshooting.

**Stack:** Python · Pandas · SQLite · Streamlit

[**View Live Dashboard →**](https://selfhealingpipelinedashboard-et3gyntpk5eyzm28x9rkgc.streamlit.app/)

[**Explore All Repositories →**](https://github.com/Akshay576-crypto?tab=repositories)

---

## Technical Writing

I write to strengthen my understanding of ML concepts and explain the reasoning behind model evaluation and ML system behavior.

- **[Self-Learning ML Systems](https://self-trainig-ml-model.hashnode.dev/self-learning-ml-model)** — Data quality, drift, monitoring, and retraining across an ML lifecycle.
- **[Understanding Confusion Matrix, MSE & RMSE](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-mse-rmse-explained-like-you-re-5)** — Evaluation concepts explained through intuition, formulas, and examples.
- **[Precision, Recall & F1](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-pt-2)** — How classification thresholds affect precision, recall, and F1.
- [**More writing on Hashnode →**](https://hashnode.com/@akshay0884)

---

---

## Connect

If you’d like to discuss Machine Learning, Data Science, agentic workflows, or one of the systems above:

- [LinkedIn](https://www.linkedin.com/in/akshay-sapariya-438747375/)
- [Technical Writing on Hashnode](https://hashnode.com/@akshay0884)
- [GitHub Repositories](https://github.com/Akshay576-crypto?tab=repositories)
- [Email](mailto:ak.56sapariya@gmail.com)

<div align="center">

**Build · Evaluate · Improve**

Machine Learning · Data Science · Agentic AI · GenAI

</div>
