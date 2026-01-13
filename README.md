# PipePilot — MLOps Training & Deployment

PipePilot is a lightweight MLOps framework that demonstrates how machine learning models move from
experimentation to reproducible, versioned, and deployable systems.

This project focuses on **how ML should be built in production**, not just how models are trained.

---

## Why this project exists

Many ML projects fail after training because:
- Experiments are not reproducible
- Models are not versioned
- There is no clear path to deployment or rollback

PipePilot addresses these gaps by modeling a **realistic ML lifecycle** used in industry.

---

## What this project does

- Trains a machine learning model on structured data
- Tracks experiments and metrics using **MLflow**
- Logs and versions trained models
- Prepares models for containerized deployment
- Demonstrates how teams can safely iterate on ML systems

---

## High-level architecture

1. **Data preparation**
   - Input dataset is cleaned and split into train/test sets

2. **Model training**
   - Model is trained using scikit-learn
   - Hyperparameters and metrics are logged

3. **Experiment tracking**
   - MLflow tracks:
     - parameters
     - metrics
     - artifacts
     - model versions

4. **Model versioning**
   - Each training run produces a versioned model
   - Enables comparison, rollback, and auditability

5. **Deployment-ready output**
   - Model artifacts are ready for Dockerized inference services

---

## Tech stack

- Python
- scikit-learn
- MLflow
- Pandas / NumPy
- Docker (deployment-ready design)

---

## Why this matters in production

This setup mirrors how real ML teams:
- Compare experiments objectively
- Avoid “works on my machine” problems
- Safely deploy and roll back models
- Collaborate across teams

It emphasizes **engineering discipline**, not just model accuracy.

---

## How to run locally

```bash
# Create virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start MLflow UI
mlflow ui

# Train and log a model
python train_and_log.py
