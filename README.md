<!-- =========================================================
     AKSHAY SAPARIYA — GITHUB PROFILE
     ========================================================= -->

<div align="center">

# Akshay Sapariya

### Machine Learning · Data Science · Agentic AI · GenAI

Building and learning through ML systems, data pipelines, retrieval,
agent workflows, and the engineering around them.

<br>

[LinkedIn](https://www.linkedin.com/in/akshay-sapariya-438747375/) &nbsp;·&nbsp;
[Technical Writing](https://hashnode.com/@akshay0884) &nbsp;·&nbsp;
[Email](mailto:ak.56sapariya@gmail.com)

</div>

<br>

---

## 01 / About

I spend most of my time working with **Machine Learning and Data Science**, particularly around model evaluation, data quality, changing data distributions, and deployment.

I've also worked with **RAG, Generative AI, and agentic systems** through Cognexa, where I experimented with semantic retrieval, vector search, routing, and tool-based workflows.

I'm interested in what happens around a model as much as the model itself — how data reaches it, how its behavior changes, how an application uses its output, and how the overall system can be evaluated and improved.

This GitHub is where I keep the systems I build, the experiments behind them, and notes on what I learn along the way.

---

## 02 / Stack

<table>
<tr>

<td width="33%" valign="top">

### ML & Data

`Python`

`SQL`

`Scikit-learn`

`Pandas`

`NumPy`

`Matplotlib`

`Seaborn`

`TensorFlow · Foundations`

</td>

<td width="33%" valign="top">

### GenAI & Agents

`RAG`

`LangChain`

`LangGraph`

`Qdrant`

`Sentence Transformers`

`Vector Search`

`LLM Integration`

`Tool Routing`

</td>

<td width="33%" valign="top">

### Engineering

`FastAPI`

`REST APIs`

`MySQL`

`Pytest`

`Docker`

`AWS S3`

`Render`

`Git / GitHub`

</td>

</tr>
</table>

---

# 03 / Selected Systems

## FraudOPS

### UPI Fraud Detection · Model Drift · Retraining · Deployment

I built FraudOPS to understand what happens when transaction patterns change after a fraud model has already been trained.

The first model was trained using **15,000 UPI transactions** with behavioral features around transaction activity, beneficiary behavior, authentication attempts, device changes, and account history.

Instead of stopping after the initial model, I introduced new transaction patterns and measured what happened when the assumptions learned during training no longer held.

| Experiment | F1 Score | PR-AUC |
|:---|---:|---:|
| Initial Model | **0.8093** | **0.9121** |
| Drift Scenario | **0.5366** | **0.4692** |
| Retrained Model | **0.9965** | **1.0000** |

> **Experiment context:** The retrained result comes from a controlled simulated drift environment. The dataset and drift scenarios are synthetic, so the result represents recovery inside this experiment rather than expected performance on real-world financial transactions.

### What I explored

`Fraud Detection` · `Feature Engineering` · `Random Forest` · `PR-AUC`

`Distribution Shift` · `Failure Analysis` · `Retraining` · `FastAPI`

### ML flow

```text
Transaction
     │
     ▼
Behavioral Features
     │
     ▼
Fraud Model
     │
     ▼
Fraud Probability
     │
     ├── LOW    → ALLOW
     │
     ├── MEDIUM → REVIEW
     │
     └── HIGH   → BLOCK
```

### Deployment

I separated static delivery from model computation rather than putting the whole application on one service.

```text
User
 │
 ▼
AWS S3
Static Frontend
 │
 ▼
FastAPI Backend
Render
 │
 ▼
ML Model
 │
 ▼
Fraud Probability
+
Risk Decision
```

The API also has automated tests covering prediction behavior, request validation, error handling, and model status.

Those tests run through GitHub Actions when changes are pushed to the repository.

[![FraudOPS Tests](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml/badge.svg)](https://github.com/Akshay576-crypto/upi-fraud-mlops/actions/workflows/tests.yml)

**[Source Code →](https://github.com/Akshay576-crypto/upi-fraud-mlops)** &nbsp;&nbsp;
**[Live Demo →](http://upi-fraud-mlops.s3-website.eu-north-1.amazonaws.com/)**

---

## DQM

### ML Pipeline Data Quality Monitoring

DQM started with a simple question:

> **What happens if poor-quality data reaches an ML pipeline before anyone notices it?**

The project adds a validation layer before downstream analytics or ML processing.

It profiles incoming datasets, looks for common data-quality problems, detects unusual observations, calculates a quality score, and keeps a history of pipeline runs.

### Pipeline

```text
CSV / Dataset
      │
      ▼
Data Profiling
      │
      ├── Missing Values
      │
      ├── Duplicates
      │
      └── Validation
      │
      ▼
Isolation Forest
      │
      ▼
Anomaly Detection
      │
      ▼
Data Quality Score
      │
      ├── MySQL History
      │
      ├── Dashboard
      │
      └── PDF Report
```

### What it includes

- Automatic dataset profiling
- Missing-value detection
- Duplicate detection
- Isolation Forest anomaly detection
- Data-quality scoring
- Pipeline-run history
- MySQL persistence
- FastAPI backend
- Dashboard trends
- PDF quality reports

**Built with**

`Python` · `Pandas` · `Scikit-learn` · `Isolation Forest` · `FastAPI` · `MySQL`

**[Explore DQM →](https://github.com/Akshay576-crypto/ML-Pipeline-DQM)**

---

## Cognexa

### RAG · Semantic Retrieval · Agentic AI · GenAI

Cognexa is where I explore another side of intelligent systems.

Instead of treating an LLM as the entire application, I wanted to understand how **retrieval, routing, tools, and generation** can work together around it.

The project experiments with semantic retrieval using Sentence Transformers and Qdrant, along with different paths for retrieval, research, and tool-based requests.

### System flow

```text
User Query
    │
    ▼
Routing / Agent Workflow
    │
    ├──────────────┬───────────────┐
    │              │               │
    ▼              ▼               ▼
Semantic        Research          Tool
Retrieval         Path          Execution
    │                              │
    ▼                              │
 Qdrant                            │
    │                              │
    └──────────────┬───────────────┘
                   │
                   ▼
           Context / Evidence
                   │
                   ▼
              LLM Response
```

### What I worked with

`RAG` · `Agentic AI` · `GenAI`

`Semantic Retrieval` · `Vector Search` · `Qdrant`

`Sentence Transformers` · `LangChain` · `LangGraph`

`FastAPI` · `LLM Integration` · `Tool Routing`

### Frontend showcase

I host the Cognexa frontend separately on **AWS S3** as a public walkthrough of the project.

The showcase is intended to make the product flow and interface easy to explore without keeping the complete backend, vector database, and LLM stack publicly running.

**[Source Code →](https://github.com/Akshay576-crypto/Cognexa)** &nbsp;&nbsp;
**[Live Project Showcase →](http://cognexa-static.s3-website.eu-north-1.amazonaws.com/)**

---

# 04 / Backend & Data Engineering

## Athere

A FastAPI-based chat application I built while spending more time on backend application structure.

The project helped me work with API routing, authentication, database-backed application logic, and separating backend responsibilities instead of keeping everything inside a single application file.

**Built with**

`Python` · `FastAPI` · `REST APIs` · `Authentication` · `MySQL`

**[Explore Athere →](https://github.com/Akshay576-crypto/chatting-app-FastAPI)**

<br>

## Self-Healing ETL Pipeline

An earlier data-engineering experiment around detecting and handling problems as data moves through a pipeline.

The project separates clean and problematic records and keeps pipeline-run history so failures can be inspected instead of silently passing downstream.

**Built with**

`Python` · `Pandas` · `SQLite` · `Streamlit` · `Pipeline Monitoring`

**[View Live Dashboard →](https://selfhealingpipelinedashboard-et3gyntpk5eyzm28x9rkgc.streamlit.app/)**

<br>

**[Explore All Repositories →](https://github.com/Akshay576-crypto?tab=repositories)**

---

# 05 / Technical Writing

I write about concepts I'm learning and problems that become clearer while building.

The goal is mostly to force myself to explain the idea simply enough that I know whether I actually understand it.

<br>

### 01 — Self-Learning ML Systems

**Data Quality · Drift · Monitoring · Retraining**

How data quality, changing distributions, model degradation, and retraining fit together across an ML lifecycle.

**[Read on Hashnode →](https://self-trainig-ml-model.hashnode.dev/self-learning-ml-model)**

<br>

### 02 — Understanding Confusion Matrix, MSE & RMSE

**Model Evaluation · Mathematics · Intuition**

Breaking down common evaluation concepts using intuition, formulas, and small numerical examples.

**[Read on Hashnode →](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-mse-rmse-explained-like-you-re-5)**

<br>

### 03 — Precision, Recall & F1

**Classification · Thresholds · Trade-offs**

Looking at how precision, recall, and F1 depend on each other and how changing a decision threshold changes model behavior.

**[Read on Hashnode →](https://self-trainig-ml-model.hashnode.dev/confusion-matrix-pt-2)**

<br>

**[Explore More Technical Writing →](https://hashnode.com/@akshay0884)**

---

# 06 / Currently Going Deeper Into

I'm currently strengthening my foundations in:

```text
Deep Learning
     │
     ├── Neural Network Fundamentals
     ├── ANN
     └── RNN

TensorFlow
     │
     └── Foundations

Statistics & Probability
     │
     └── Stronger ML intuition

ML System Design
     │
     └── Models beyond the notebook
```

I'm continuing to build with classical Machine Learning while going deeper into these areas rather than adding tools only to make the stack longer.

---

# 07 / Connect

If you'd like to talk about Machine Learning, Data Science, RAG, Agentic AI, or something I've built:

**[LinkedIn →](https://www.linkedin.com/in/akshay-sapariya-438747375/)**

**[Technical Writing →](https://hashnode.com/@akshay0884)**

**[GitHub →](https://github.com/Akshay576-crypto)**

**[Email →](mailto:ak.56sapariya@gmail.com)**

<br>

<div align="center">

**Akshay Sapariya**

Machine Learning · Data Science · Agentic AI · GenAI

</div>