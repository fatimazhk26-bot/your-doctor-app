# your-doctor-app

Business analysis & product design for an AI-powered medical assistant app

---

## 📋 Project Description

**Your Doctor (QuickDiag)** is an AI-powered mobile health triage application designed to help users evaluate their symptoms, understand possible causes, and know when to seek professional medical care — safely, quickly, and even offline.

The app is **not intended to replace a doctor**. Instead, it helps users to:
- Assess the urgency level of their symptoms (low / medium / high / emergency)
- Understand possible (non-diagnostic) causes behind their symptoms
- Know when to consult a medical professional
- Receive safe, general health guidance and over-the-counter medicine suggestions

This repository contains the **full Business Analyst deliverables** produced during the discovery and design phase of the project: market research, competitive analysis, requirements (MoSCoW), user stories, UML diagrams, business model design, pricing strategy, and interactive dashboards.

### Problem & Opportunity
Today, users often don't know how serious their symptoms are, emergency rooms are overloaded, access to a doctor is limited, and online searches ("Dr. Google") tend to generate anxiety and misinformation. The health-tech market shows strong growth in AI-based, privacy-first, and autonomous health solutions — an opportunity that **Your Doctor** aims to capture by positioning itself as a secure, explainable, and intelligent triage assistant.

### Key Product Principles
- **Safety-first**: a rule-based "Red Flag" safety layer always takes priority over the AI/LLM output.
- **Explainability**: every recommendation must state the symptoms considered, the simplified reasoning used, and a legal disclaimer.
- **Privacy-first**: ~97% of processing runs on-device / offline.
- **No self-improving AI in production**: model updates are manually validated, tested, and version-controlled — no autonomous learning in the field.

---

## 🛠️ Tech Stack

| Layer | Technology / Approach |
|---|---|
| **AI Engine** | On-device Large Language Model (e.g., Qwen2-7B quantized, or quantized Llama) for natural language understanding, symptom reformulation, follow-up question generation, and simplified medical explanations |
| **Safety Layer** | Rule-based medical logic (decision trees + "Red Flag" keyword/context detection) — has override priority over the LLM |
| **Confidence & Scoring Module** | Calculates a confidence score per recommendation to decide between general advice vs. referral to a professional |
| **Mobile App** | Android / iOS (native or cross-platform mobile application) |
| **Data & Privacy** | Local/on-device data storage, secure health history tracking, encrypted consultation data |
| **Business Analysis Tools** | Excel (competitor dataset of 40 health apps), Power BI (interactive dashboards) |
| **Modeling & Documentation** | UML diagrams — Activity, Class, and Sequence diagrams (draw.io / PlantUML style) |
| **Product Design Tools** | Business Model Canvas (BMC), Value Proposition Canvas (VPC), MoSCoW prioritization matrix, User Stories |
| **Distribution Channels** | Google Play Store, Apple App Store, digital marketing (Google/Meta Ads), university partnerships |

---

## 📂 Folder Structure Overview

```
your-doctor-app/
│
├── Diagrams/
│   ├── Diagramme d'activité.pdf        # Activity diagrams (Auth & Profile, Symptom Assessment,
│   │                                     Guidance, Consultation History, Plans & Payment, Gamification)
│   ├── Diagramme de Séquence.pdf       # Sequence diagrams for the same core flows
│   └── Diagramme de classe.pdf         # Class diagram — system entities, attributes, methods, relations
│
├── Docs/
│   ├── Business Analyst Study.pdf      # Full business analyst report / cahier des charges
│   └── MoSCoW-Method-YourDoctor.pdf    # Feature prioritization matrix (Must/Should/Could/Won't have)
│
├── business-model/
│   ├── business-model-canvas.png       # Business Model Canvas (BMC)
│   └── value-proposition-canvas.png    # Value Proposition Canvas (VPC)
│
├── dashboard/
│   └── medical-apps-market-analysis.pbix   # Power BI dashboard — competitor market analysis
│
├── market-analysis/
│   └── Competitive Pricing Analysis.pdf    # Pricing benchmark across 40 competing health apps
│
└── README.md
```

---

## 📊 Opening the Power BI Dashboard (`.pbix`)

The market analysis dashboard (`dashboard/medical-apps-market-analysis.pbix`) was built to visualize the competitive landscape of **40 medical/health applications** (downloads, ratings, reviews, business models, AI usage, pricing, etc.).

**Requirements:**
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only)

**Steps to open it:**
1. Download and install Power BI Desktop if you don't already have it.
2. Clone or download this repository.
3. Navigate to the `dashboard/` folder.
4. Double-click `medical-apps-market-analysis.pbix` — it will open automatically in Power BI Desktop.
5. Use the visuals to explore:
   - Total apps analyzed, average downloads, average ratings, total reviews, average app age
   - Apps by region, by consultation type
   - Prescription & pharmacy service availability
   - AI diagnostics usage (AI vs. non-AI apps)
   - Business model distribution (free, freemium, subscription, per-consult, B2B)
   - Top apps by downloads and ratings

> 💡 **Note:** If you don't have Power BI Desktop installed, you can still view a static export of the dashboard via the screenshots included in `Docs/Business Analyst Study.pdf` and the presentation deck.

---

## 📌 Summary of Business Analysis Deliverables

- **Market Analysis**: 40 competing health apps analyzed (avg. 15.63M downloads, 4.5★ average rating, ~5M reviews, ~10 years average app age)
- **Pricing Analysis**: Consultation pricing benchmark ($49–$99 average, ~$65 median) and recommended subscription tiers (Monthly $39–49, 3-Month $105–109, 6-Month $187–190, Annual $249–299, Lifetime $498–500)
- **MoSCoW Matrix**: Full functional requirement prioritization (Must/Should/Could/Won't Have)
- **User Stories**: Organized by Epic — Onboarding & Profile, Symptom Assessment (Core AI), Medical Guidance, Consultation History, Subscription & Plans, Gamification
- **UML Diagrams**: Activity, Class, and Sequence diagrams covering Authentication, Symptom Assessment, Guidance, Consultation History, Plans & Payment, and Gamification flows
- **Business Model Canvas & Value Proposition Canvas**: Full economic model and customer needs/pains/gains mapping
- **Naming Strategy**: Brand name selection process leading to the retained name **QuickDiag**

---

## ⚠️ Disclaimer

This project (and its underlying AI concept) is designed strictly as a **triage and guidance tool**. It does **not** provide official medical diagnoses, does **not** prescribe regulated medication, and does **not** replace a licensed physician.
