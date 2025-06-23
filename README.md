# 📝 End-to-End Text Summarization

This project demonstrates an end-to-end NLP pipeline that automatically generates concise summaries from conversational text using the PEGASUS transformer model. It covers the complete ML lifecycle: from data ingestion to deployment, including model training, evaluation, and web UI integration.

## 🚀 Project Features
🧠 Model Training with PEGASUS

📊 ROUGE-based Evaluation

⚙️ FastAPI-based Inference Server

🐳 Dockerized Deployment on AWS EC2 & ECR

🔁 CI/CD with GitHub Actions

## 📂 Project Structure

├── config/                # Configuration files (params.yaml, config.yaml)
├── src/                   # Source code for pipelines and utilities
├── app/                   # FastAPI web server
│   ├── app.py             # API routes: /train and /predict
├── Dockerfile             # Docker container definition
├── main.py                # Entrypoint for model training
├── requirements.txt       # Dependencies
├── .github/workflows/     # CI/CD pipeline using GitHub Actions

## 🧪 Model Pipeline (Part 1)
Data Ingestion – Downloads SAMSum dataset and organizes it.

Data Validation – Verifies presence and format of train/val/test splits.

Data Transformation – Uses PEGASUS tokenizer to prepare inputs.

Model Training – Configurable training via params.yaml.

Evaluation – Outputs ROUGE scores and saves them for analysis.

## 🌐 Prediction + UI (Part 2)
Uses FastAPI to serve trained model.

Routes:

/train – Triggers model training.

/predict – Accepts dialogue and returns summary.

## ☁️ Deployment
Dockerized Application

Hosted on AWS EC2

Container image pushed to AWS ECR

Automated CI/CD via GitHub Actions

## 📈 Evaluation Metric
ROUGE Score: Measures overlap between generated and human-written summaries.

ROUGE-L, ROUGE-1, ROUGE-2 metrics used.

## 💡 Tech Stack
Language: Python

Model: PEGASUS (HuggingFace Transformers)

Frameworks: FastAPI, PyTorch

Deployment: Docker, AWS EC2, AWS ECR

CI/CD: GitHub Actions


