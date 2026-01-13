# PipePilot — MLOps Training + Deployment (Starter)

A minimal MLOps template that you can expand:
- MLflow experiment tracking
- Model registry basics (local)
- Dockerized inference service (optional)

## Run MLflow locally
```bash
pip install -r requirements.txt
mlflow ui
```

## Train + log a model
```bash
python train_and_log.py
```

## Next upgrades
- GitHub Actions CI
- Dockerfile + deploy
- Drift monitoring + retrain trigger
