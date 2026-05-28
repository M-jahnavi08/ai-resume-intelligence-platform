# 🚀 AI Resume Intelligence Platform

An end-to-end AI + ML powered resume analysis platform built with Python, Streamlit, Google Gemini AI, and scikit-learn.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📊 ATS Scoring | Rule-based ATS score using required skill matching |
| 🧠 ML Job Match | TF-IDF + Cosine Similarity for real ML-based job matching |
| 🔍 Skill Gap Analysis | Detects skills missing from JD using NLP |
| 📋 Section Detector | Checks resume structure (Education, Projects, etc.) |
| 🤖 AI Summary | Gemini AI generated professional resume summary |
| 🔍 AI Feedback | Detailed recruiter-style resume feedback |
| ✉️ Cover Letter | AI-generated tailored cover letter |
| 🎯 Interview Prep | Personalized interview questions from Gemini |
| 🚀 Recommendations | Career path, project, and skill recommendations |
| 🔐 Auth System | Secure login with PBKDF2 password hashing |
| 📂 History | Per-user resume analysis history |

---

## 🛠 Tech Stack

- **Frontend:** Streamlit, Custom CSS, Glassmorphism UI
- **AI:** Google Gemini 2.0 Flash API
- **ML:** scikit-learn (TF-IDF, Cosine Similarity)
- **NLP:** Custom skill detection, keyword density, section parsing
- **Database:** SQLite (users + resume analytics)
- **PDF Parsing:** pdfplumber
- **Charts:** Plotly

---

## 🚀 Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/ai-resume-platform.git
cd ai-resume-platform

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your Gemini API key
# Edit .streamlit/secrets.toml:
# GEMINI_API_KEY = "your_key_here"
# Get free key at: https://aistudio.google.com

# 4. Run
streamlit run app.py
```

---

## 📁 Project Structure

```
resume-analyzer/
├── app.py                        # Main controller
├── components/
│   ├── dashboard.py              # ATS analytics dashboard
│   ├── ml_dashboard.py           # ML analysis dashboard
│   ├── ai_features.py            # Gemini AI tools
│   ├── recommendations.py        # Career recommendations
│   ├── landing_page.py           # Landing page UI
│   └── auth_ui.py                # Login / Signup UI
├── utils/
│   ├── parser.py                 # PDF text extraction
│   ├── skill_engine.py           # Rule-based scoring
│   └── ml_engine.py              # TF-IDF ML engine
├── database/
│   ├── db.py                     # Resume database
│   └── auth_db.py                # User auth database
├── assets/
│   └── styles.css                # Full UI styling
├── .streamlit/
│   └── secrets.toml              # API keys (not committed)
└── requirements.txt
```

---

## 🔒 Security

- Passwords hashed using **PBKDF2-HMAC-SHA256** with random salt
- 100,000 iterations — industry standard
- No plain-text passwords stored anywhere

---

## 🧠 ML Architecture

```
Resume PDF
    │
    ▼
Text Extraction (pdfplumber)
    │
    ├──► TF-IDF Vectorizer ──► Cosine Similarity ──► Job Match Score
    │
    ├──► Keyword Density Scoring ──► Skill Coverage %
    │
    ├──► Section Detector (regex NLP) ──► Structure Score
    │
    └──► Weighted Combination ──► Final ML Resume Score
```

---

## 📊 Scoring System

| Score | Weight | Method |
|---|---|---|
| TF-IDF Job Match | 40% | scikit-learn cosine similarity |
| Keyword Density | 30% | Custom NLP frequency analysis |
| Section Quality | 30% | Regex-based section detection |

---

## 🌐 Deploy on Streamlit Cloud

1. Push to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io)
3. Connect your repo
4. Add `GEMINI_API_KEY` in Secrets
5. Deploy — get a public URL instantly

---

## 👩‍💻 Developer

**Jahnavi** — Built as a full-stack AI + ML portfolio project.

