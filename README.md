# 🚀 AI Resume Intelligence Platform

### An end-to-end AI + ML powered resume analysis platform

[![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.35-red?style=for-the-badge&logo=streamlit)](https://streamlit.io)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.4-orange?style=for-the-badge&logo=scikit-learn)](https://scikit-learn.org)
[![Groq AI](https://img.shields.io/badge/Groq_AI-LLaMA_3.3_70B-purple?style=for-the-badge)](https://groq.com)
[![SQLite](https://img.shields.io/badge/SQLite-Database-green?style=for-the-badge&logo=sqlite)](https://sqlite.org)

---

## Screenshots

### Landing Page
![Landing Page](screenshots/landing.png)

### Login and Signup
![Login](screenshots/login.png)

### Analytics Dashboard
![Dashboard](screenshots/dashboard.png)

### ML Analysis
![ML Analysis](screenshots/ml_analysis.png)

### AI Features
![AI Features](screenshots/ai_features.png)

---

## Features

- ATS Scoring — Rule-based ATS score using required skill matching
- ML Job Match — TF-IDF + Cosine Similarity for real ML-based job matching
- Skill Gap Analysis — Detects skills missing from JD using NLP
- AI Summary — Groq LLaMA 3.3 70B generated professional resume summary
- AI Feedback — Detailed recruiter-style resume feedback
- Cover Letter — AI-generated tailored cover letter
- Interview Prep — Personalized interview questions by difficulty level
- Auth System — Secure login with PBKDF2-HMAC-SHA256 password hashing
- History — Per-user resume analysis history with all scores

---

## Tech Stack

- Frontend: Streamlit, Custom CSS, Glassmorphism UI
- AI: Groq API — LLaMA 3.3 70B
- ML: scikit-learn (TF-IDF Vectorization, Cosine Similarity)
- NLP: Custom skill detection, keyword density, section parsing
- Database: SQLite
- PDF Parsing: pdfplumber
- Charts: Plotly

---

## Run Locally

1. Clone the repo
   git clone https://github.com/M-jahnavi08/ai-resume-intelligence-platform.git

2. Install dependencies
   pip install -r requirements.txt

3. Add your Groq API key in .streamlit/secrets.toml
   GROQ_API_KEY = your_key_here
   Get free key at https://console.groq.com

4. Run
   python -m streamlit run app.py

---

## ML Architecture

Resume PDF
    |
    Text Extraction (pdfplumber)
    |
    TF-IDF Vectorizer -> Cosine Similarity -> Job Match Score (40%)
    |
    Keyword Density Scoring -> Skill Coverage (30%)
    |
    Section Detector (regex NLP) -> Structure Score (30%)
    |
    Weighted Combination -> Final ML Resume Score

---

## Security

- Passwords hashed using PBKDF2-HMAC-SHA256 with random salt
- 100,000 iterations — industry standard
- No plain-text passwords stored anywhere

---

## Developer

Mommineedi Jahnavi Satya

LinkedIn: https://linkedin.com/in/mommineedi-jahnavisatya-b8955a352
GitHub: https://github.com/M-jahnavi08
