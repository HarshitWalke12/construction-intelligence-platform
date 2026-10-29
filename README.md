# 🏗️ Multimodal Construction Intelligence Platform

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://python.org)
[![Gemini](https://img.shields.io/badge/Powered%20by-Gemini%202.0%20Flash-orange?logo=google)](https://aistudio.google.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Skill Wallet — Capstone Project 1**
> An AI-powered Streamlit application combining Google Gemini multimodal AI with domain-specific construction engineering logic.

---

## ✨ Features

| Module | Description | Epic |
|--------|-------------|------|
| 🦺 **Site Safety & PPE Audit** | Upload site photos → AI detects PPE compliance, identifies hazards, generates OSHA/IS 456 report | Epic 2 |
| 🔍 **Crack Diagnostics** | Upload concrete/wall photos → classify defect type, estimate crack width, recommend repairs with costs | Epic 2 |
| 📊 **Planning & Valuation** | Interactive inputs → project budget, asset valuation (INR), material estimates, AI 3D rendering | Epic 3 |
| 💬 **Site Assistant** | Weather-aware safety alerts + multi-turn construction engineering chatbot powered by Gemini | Epic 5 |

---

## 🚀 Quick Start

### Local Development

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# 2. (Optional) Create a virtual environment
python -m venv .venv
.venv\Scripts\activate   # Windows
# source .venv/bin/activate  # macOS/Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
streamlit run app.py
```

The app opens at **http://localhost:8501**

### ☁️ Streamlit Community Cloud (1-Click Deploy)

1. Fork / push this repo to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in
3. Click **New app** → select your repo → set `app.py` as the main file
4. *(Optional)* Add `GEMINI_API_KEY` under **Settings → Secrets**
5. Click **Deploy** 🚀

---

## 🔑 API Key Setup

| Method | Instructions |
|--------|-------------|
| **Sidebar (local)** | Paste your key in the sidebar text box at runtime |
| **Streamlit Secrets (cloud)** | Add `GEMINI_API_KEY = "your-key"` in the Streamlit Cloud Secrets panel |
| **Demo Mode** | No key needed — app runs with simulated realistic results |

Get a free key at → [aistudio.google.com/apikey](https://aistudio.google.com/apikey)

---

## 🏗️ Architecture

```
┌─────────────────────────────────┐
│        Streamlit Frontend       │
│   Tabs · File Upload · Widgets  │
└──────────────┬──────────────────┘
               │  multimodal prompts (text + image)
               ▼
┌─────────────────────────────────┐
│     Google Gemini 2.0 Flash     │
│       Vision + Language Model   │
└──────────────┬──────────────────┘
               │  structured JSON responses
               ▼
┌─────────────────────────────────┐
│       Domain Logic Layer        │
│  PPE Audit · Crack Diagnostics  │
│  Cost Valuation · Weather Chat  │
└─────────────────────────────────┘
```

**Zero external database dependencies** — everything runs in-memory.

---

## 📦 Dependencies

```
streamlit>=1.36.0
google-generativeai>=0.7.0
Pillow>=10.0.0
```

---

## 📁 Project Structure

```
.
├── app.py                  # Main Streamlit application (all modules)
├── requirements.txt        # Python dependencies
├── README.md               # This file
├── LICENSE                 # MIT License
└── .streamlit/
    └── config.toml         # Dark theme configuration
```

---

## 🛡️ Standards Referenced

- **IS 456:2000** — Indian Standard for Plain and Reinforced Concrete
- **IS 1893** — Criteria for Earthquake Resistant Design
- **IS 875** — Code of Practice for Design Loads
- **IS 3696** — Safety Code for Scaffolding
- **OSHA 29 CFR 1926** — Construction Industry Safety Standards
- **ACI 318** — Building Code Requirements for Structural Concrete
- **ASTM C881** — Standard Specification for Epoxy-Resin-Base Bonding Systems

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">Built with ❤️ using Streamlit & Google Gemini · Zero DB Dependencies · 1-Click Deploy</p>
