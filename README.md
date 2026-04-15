# 🏥 Doctor Recommendation System

An intelligent healthcare platform leveraging machine learning to help patients find the right doctors based on location, specialization, fees, and services.

[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-5.0-green.svg)](https://www.djangoproject.com/)
[![CatBoost](https://img.shields.io/badge/CatBoost-ML-orange.svg)](https://catboost.ai/)

---

## Overview

A production-ready ML system that recommends doctors based on geographic location, medical specialization, consultation fees, and hospital services. Uses CatBoost model with **99.63% accuracy** on 500+ verified doctors dataset.

**Features:**
- AI-powered doctor recommendations (99.63% R² Score)
- Real-time search & filtering (500+ doctors)
- REST API + Web UI
- Network API for team sharing
- Production-ready with Django best practices  

---

## Model Performance

| Model | RMSE | R² Score | Accuracy |
|-------|------|----------|----------|
| **CatBoost** ✅ | **0.0126** | **0.9963** | **99.63%** |
| Gradient Boosting | 0.0227 | 0.9879 | 98.79% |
| XGBoost | 0.0235 | 0.9870 | 98.70% |
| AdaBoost | 0.0793 | 0.8520 | 85.20% |

**CatBoost selected** for native categorical handling and lowest RMSE.

---

## 📸 User Interface

### Input Page
![Input Interface](https://drive.google.com/uc?export=view&id=1OVoBvt2csRNjh2RqzHcuzMvtI9NjpcpE)

Fill in your requirements:
- Select District (Dhaka, Chittagong, etc.)
- Choose Thana/Area
- Select Medical Specialization
- Set Maximum Consultation Fee
- Optional: Filter by Online/Emergency services

### Output Page
![Output Results](https://drive.google.com/uc?export=view&id=1KD2jkHPG8esA16JSQ3nH67Cn0HHeXueZ)

Get recommendations ranked by AI quality score:
- Doctor name and specialization
- Rating and experience
- Consultation fees
- Hospital details
- AI quality prediction (Excellent/Good/Fair)

---

## Architecture

Django backend (port 7777) → CatBoost ML model → Pandas data processing → Excel database (500+ doctors)

Web UI for patient search | REST API for developers

---

## Project Structure

- `drseba_platform/` — Django project configuration
- `recommender/` — Main Django app (API & ML logic)
- `demo_ui/` — Frontend (HTML + CSS)
- `data/` — Dataset (500+ doctors)
- `models/` — Serialized ML models (CatBoost pickle)
- `manage.py` — Django entry point

---

## Quick Start

**1. Setup:**
```bash
git clone <repo-url>
cd model
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

**2. Run Server:**
```bash
python manage.py runnetwork
```
Access at: `http://192.168.10.23:7777`

**3. API:**
```bash
POST /api/recommendations
{
  "district": "Dhaka",
  "thana": "Dhanmondi",
  "specialization": "Cardiology",
  "max_fee": 2000,
  "top_n": 5
}
```

---

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Backend | Django 5.0 |
| ML Engine | CatBoost |
| Data Processing | Pandas + NumPy + Scikit-learn |
| Frontend | HTML + CSS |
| Database | Excel (.xlsx) |

---

## About

Developed under the mentorship of **Nusrat Jahan** during an internship program focusing on applied machine learning and data-driven healthcare solutions.

For detailed API documentation and setup troubleshooting, see `DEVELOPER_API_GUIDE.md` and `HOW_TO_RUN.md`.

---

**Made with ❤️ for Dr.Seba Platform**  
*April 2026*
