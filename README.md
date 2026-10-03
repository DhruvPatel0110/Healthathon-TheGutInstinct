<p align="center">
  <img src="https://img.shields.io/badge/Health--a--thon-2026-FF6B6B?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0id2hpdGUiPjxwYXRoIGQ9Ik0xMiAyMS4zNWwtMS40NS0xLjMyQzUuNCAxNS4zNiAyIDEyLjI4IDIgOC41IDIgNS40MiA0LjQyIDMgNy41IDNjMS43NCAwIDMuNDEuODEgNC41IDIuMDlDMTMuMDkgMy44MSAxNC43NiAzIDE2LjUgMyAxOS41OCAzIDIyIDUuNDIgMjIgOC41YzAgMy43OC0zLjQgNi44Ni04LjU1IDExLjU0TDEyIDIxLjM1eiIvPjwvc3ZnPg==&logoColor=white" alt="Health-a-thon 2026"/>
  <img src="https://img.shields.io/badge/Track-Cancer-9B59B6?style=for-the-badge&logo=target&logoColor=white" alt="Cancer Track"/>
  <img src="https://img.shields.io/badge/Team-The_Gut_Instinct-2ECC71?style=for-the-badge&logo=people&logoColor=white" alt="Team"/>
</p>

<h1 align="center">
  🔬 Gut Instinct
</h1>

<h3 align="center">
  <em>Multimodal AI-Based Physician Assist for Screening & Diagnosis of Colorectal Carcinoma</em>
</h3>

<p align="center">
  <strong>Transforming routinely available patient data into actionable CRC risk insights — so no high-risk patient falls through the cracks.</strong>
</p>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/BioBERT-NLP-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="BioBERT"/>
  <img src="https://img.shields.io/badge/XGBoost-ML-006600?style=flat-square&logo=xgboost&logoColor=white" alt="XGBoost"/>
  <img src="https://img.shields.io/badge/LSTM-Deep_Learning-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="LSTM"/>
  <img src="https://img.shields.io/badge/SHAP-Explainability-4B0082?style=flat-square" alt="SHAP"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License"/>
</p>

---

## 📋 Table of Contents

- [The Crisis](#-the-crisis)
- [Our Solution](#-our-solution)
- [Clinical Workflow](#-clinical-workflow)
- [Technical Architecture](#-technical-architecture)
- [Model Pipeline Deep Dive](#-model-pipeline-deep-dive)
- [Key Features](#-key-features)
- [Expected Outcomes](#-expected-outcomes)
- [Team](#-team)
- [Acknowledgements](#-acknowledgements)

---

## 🚨 The Crisis

<table>
<tr>
<td width="60%">

### Colorectal Cancer in India — A Silent Epidemic

Colorectal Carcinoma (CRC) is one of the most commonly occurring malignancies worldwide, and India faces a uniquely devastating challenge:

| Metric | Reality |
|--------|---------|
| **Late Diagnosis Rate** | **60%** of patients diagnosed at advanced stages |
| **Trend** | Disease burden **increasing** over the past decade |
| **Gold Standard** | Colonoscopy — invasive, uncomfortable & expensive |
| **The Gap** | **No reliable pre-screening** to prioritize high-risk patients |

> *Late diagnosis → Increased disease burden → Decreased quality of life → Increased mortality*

</td>
<td width="40%" align="center">

```
     ╔══════════════════════╗
     ║   THE SCREENING GAP  ║
     ╠══════════════════════╣
     ║                      ║
     ║  Patient with        ║
     ║  early symptoms      ║
     ║       │              ║
     ║       ▼              ║
     ║  ❌ No pre-screening ║
     ║       │              ║
     ║       ▼              ║
     ║  Late diagnosis      ║
     ║  (Stage III/IV)      ║
     ║       │              ║
     ║       ▼              ║
     ║  Poor outcomes       ║
     ║                      ║
     ╚══════════════════════╝
```

</td>
</tr>
</table>

The core problem is clear: **there is no intelligent pre-screening mechanism** to identify individuals at elevated CRC risk *before* they need an invasive colonoscopy. High-risk patients are being missed. Screening opportunities are being lost. Lives are at stake.

---

## 💡 Our Solution

### Gut Instinct: Pre-Colonoscopy AI-Powered Risk Stratification

**Gut Instinct** is a multimodal AI system that analyses routinely available patient information and clinical records to identify individuals who are at increased risk of colorectal cancer and may require screening or follow-up.

<table>
<tr>
<td>

#### 🎯 What It Does

- **Identifies** individuals at elevated CRC risk using readily available clinical data
- **Prioritizes** patients who require further evaluation
- **Reduces** the possibility of high-risk individuals being missed
- **Triggers** personalized reminders for patients due for reassessment
- **Explains** its reasoning through interpretable AI (SHAP/LIME)

</td>
<td>

#### 📊 What Goes Into the Assessment

- **Patient Profile** — Age, clinical history, symptoms, family history
- **Lifestyle Factors** — Diet, physical activity, substance use
- **Clinical Data** — Routine laboratory findings, low-cost measurements
- **Temporal Patterns** — Trends in lab results over time
- **Clinical Text** — Physician notes, symptom descriptions

</td>
</tr>
</table>

> **Clinical Endpoint:** Identification of patients who warrant consideration for definitive CRC evaluation by colonoscopy.

```
  Earlier Recognition  →  Smarter Use of Colonoscopy  →  Improved Outcomes
```

---

## 🏥 Clinical Workflow

Our solution seamlessly integrates into existing clinical workflows, acting as a **physician decision-support tool** — never replacing clinical judgement.

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                 │
│   ┌──────────────┐     ┌──────────────────┐     ┌──────────────┐     ┌────────┐│
│   │  SYMPTOMS +  │     │  COMPUTATIONAL   │     │  PHYSICIAN   │     │COLONOS-││
│   │ PATIENT DATA │────▶│   ASSESSMENT     │────▶│  EVALUATION  │────▶│ COPY   ││
│   │              │     │                  │     │              │     │        ││
│   │ • History    │     │ • Risk Score     │     │ • Clinical   │     │ Gold   ││
│   │ • Labs       │     │   (0-100)        │     │   Judgement  │     │Standard││
│   │ • Lifestyle  │     │ • Component      │     │ • Treatment  │     │        ││
│   │ • Symptoms   │     │   Breakdown      │     │   Decision   │     │        ││
│   │ • Family Hx  │     │ • SHAP/LIME      │     │              │     │        ││
│   │              │     │   Explanations   │     │              │     │        ││
│   └──────────────┘     └──────────────────┘     └──────────────┘     └────────┘│
│                                                                                 │
│   ⚠️  The computational assessment SUPPORTS clinical decision-making;           │
│       it does NOT generate medical judgement.                                    │
│                                                                                 │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## 🧠 Technical Architecture

### 4-Layer Multimodal Pipeline

Our architecture processes heterogeneous patient data through four specialized computational layers, each optimized for a different data modality, before fusing them into a unified risk assessment.

```
                            ┌─────────────────────┐
                            │    PATIENT DATA      │
                            │  (Multi-Source)       │
                            └──────────┬──────────┘
                                       │
                    ┌──────────────────┼──────────────────┐
                    │                  │                  │
                    ▼                  ▼                  ▼
          ┌─────────────────┐ ┌──────────────┐ ┌──────────────────┐
          │   LAYER 1: NLP  │ │ LAYER 2: ML  │ │  LAYER 3: DL    │
          │                 │ │              │ │                  │
          │  BioBERT        │ │  XGBoost     │ │  LSTM            │
          │  Embeddings     │ │  Random      │ │  (Temporal Lab   │
          │       +         │ │  Forest      │ │   Trend Analysis)│
          │  Symptom        │ │              │ │       +          │
          │  Scoring        │ │  Tabular:    │ │  Dense Neural    │
          │                 │ │  Labs, Demo- │ │  Network         │
          │  Input:         │ │  graphics,   │ │  (Multi-Modal    │
          │  Clinical Text  │ │  Lifestyle   │ │   Fusion)        │
          └────────┬────────┘ └──────┬───────┘ └────────┬─────────┘
                   │                 │                  │
                   └─────────────────┼──────────────────┘
                                     ▼
                        ┌────────────────────────┐
                        │    LAYER 4: ENSEMBLE   │
                        │                        │
                        │  Weighted Voting +     │
                        │  Probability           │
                        │  Calibration           │
                        │                        │
                        └────────────┬───────────┘
                                     │
                                     ▼
                        ┌────────────────────────┐
                        │      CRC RISK SCORE    │
                        │        (0 — 100)       │
                        │                        │
                        │  + Component Breakdown  │
                        │  + SHAP/LIME Explain.   │
                        │  + Colonoscopy Rec.     │
                        └────────────────────────┘
```

---

## 🔬 Model Pipeline Deep Dive

<details>
<summary><strong>Layer 1 — Natural Language Processing (NLP)</strong></summary>

<br/>

| Component | Details |
|-----------|---------|
| **Model** | BioBERT (Bidirectional Encoder Representations from Transformers for Biomedical Text Mining) |
| **Purpose** | Extract semantic meaning from unstructured clinical text |
| **Input** | Physician notes, symptom descriptions, clinical history narratives |
| **Process** | Contextual embeddings + domain-specific symptom scoring |
| **Output** | Dense vector representations of clinical text + symptom risk signals |

BioBERT is pre-trained on large-scale biomedical corpora (PubMed abstracts + PMC full-text articles), giving it a nuanced understanding of medical terminology, symptom descriptions, and clinical context that general-purpose language models lack.

</details>

<details>
<summary><strong>Layer 2 — Machine Learning (ML)</strong></summary>

<br/>

| Component | Details |
|-----------|---------|
| **Models** | XGBoost + Random Forest (Ensemble) |
| **Purpose** | Process structured tabular patient data |
| **Input** | Laboratory results, demographics, lifestyle factors |
| **Process** | Gradient boosting + bagging for robust tabular predictions |
| **Output** | Risk probability from structured data features |

The dual-model approach (XGBoost + Random Forest) provides complementary strengths: XGBoost captures complex non-linear feature interactions, while Random Forest provides robust, low-variance predictions. Together, they deliver reliable risk estimates from structured clinical data.

</details>

<details>
<summary><strong>Layer 3 — Deep Learning (DL)</strong></summary>

<br/>

| Component | Details |
|-----------|---------|
| **Models** | LSTM (Long Short-Term Memory) + Dense Neural Network |
| **Purpose** | Capture temporal patterns in lab trends + fuse all modalities |
| **Input** | Sequential lab results over time + NLP embeddings |
| **Process** | Temporal pattern recognition + multi-modal feature fusion |
| **Output** | Time-aware risk signals + unified feature representation |

The LSTM component is critical for detecting subtle *trends* in laboratory values over time — a gradually declining hemoglobin or slowly rising inflammatory markers may signal early CRC even when individual values remain within "normal" ranges. The Dense NN then fuses these temporal signals with the NLP embeddings for a holistic patient representation.

</details>

<details>
<summary><strong>Layer 4 — Ensemble & Calibration</strong></summary>

<br/>

| Component | Details |
|-----------|---------|
| **Method** | Weighted Voting + Probability Calibration |
| **Purpose** | Combine all model outputs into a final, calibrated risk score |
| **Input** | Predictions from NLP, ML, and DL layers |
| **Process** | Optimized weight assignment + isotonic/Platt calibration |
| **Output** | Calibrated CRC Risk Score (0–100) with component breakdowns |

Probability calibration ensures that when the model says "70% risk," there is genuinely a ~70% probability of CRC suspicion. This is critical for clinical trust and decision-making. Component breakdowns via SHAP/LIME allow physicians to understand *why* a patient was flagged.

</details>

---

## ✨ Key Features

<table>
<tr>
<td align="center" width="25%">

### 🎯
### Risk Stratification
Calibrated CRC Risk Score (0–100) from routinely available patient data

</td>
<td align="center" width="25%">

### 🧬
### Multimodal AI
4-layer pipeline processing text, tabular data, and temporal trends simultaneously

</td>
<td align="center" width="25%">

### 🔍
### Explainable AI
SHAP/LIME explanations showing *why* each patient was flagged — building physician trust

</td>
<td align="center" width="25%">

### ⏰
### Smart Follow-Up
Automated identification of patients due for reassessment + personalized outreach

</td>
</tr>
</table>

<table>
<tr>
<td align="center" width="33%">

### 🩺
### Physician-Centric
Designed as a decision-support tool — augmenting, never replacing, clinical judgement

</td>
<td align="center" width="33%">

### 📊
### Component Breakdown
Risk decomposed into symptom, lab, and lifestyle components for clinical clarity

</td>
<td align="center" width="33%">

### 🏥
### Workflow Integration
Seamlessly fits into existing clinical workflows as a pre-colonoscopy screening step

</td>
</tr>
</table>

---

## 📈 Expected Outcomes

### Model Output & Clinical Use

Gut Instinct generates a **comprehensive risk assessment** for each patient:

```
┌──────────────────────────────────────────────────────────────────┐
│                    SAMPLE OUTPUT REPORT                          │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Patient: ████████████          Date: 2026-10-03                │
│                                                                  │
│  ╔════════════════════════════════════════════╗                  │
│  ║     OVERALL CRC RISK SCORE:  73 / 100     ║                  │
│  ║     ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░░░░  HIGH RISK      ║                  │
│  ╚════════════════════════════════════════════╝                  │
│                                                                  │
│  Component Breakdown:                                            │
│  ┌──────────────────────────────────────────┐                   │
│  │ Symptom Profile:     ████████░░  78%     │                   │
│  │ Lab/Clinical:        ██████░░░░  62%     │                   │
│  │ Lifestyle/Behav.:    ███████░░░  71%     │                   │
│  │ Temporal Trends:     █████████░  85%     │                   │
│  └──────────────────────────────────────────┘                   │
│                                                                  │
│  ⚡ Recommendation: Consider definitive CRC evaluation          │
│  📋 Key Contributing Factors (via SHAP):                        │
│     • Persistent change in bowel habits (12 weeks)              │
│     • Declining hemoglobin trend over 6 months                  │
│     • Family history of CRC (first-degree relative)             │
│     • Age > 50 with sedentary lifestyle                         │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### Clinical Impact Goals

| Goal | Description |
|------|-------------|
| **🔎 Earlier Detection** | Identify high-risk individuals *before* symptoms become advanced |
| **🏥 Smarter Resource Use** | Prioritize colonoscopy for patients who need it most |
| **📋 Better Follow-Up** | Ensure no high-risk patient is lost to follow-up |
| **🤝 Physician Empowerment** | Provide data-driven insights that complement clinical expertise |
| **📉 Reduce Late Diagnoses** | Shift the 60% late-diagnosis rate toward earlier detection |

---

## 👥 Team

<table>
<tr>
<td align="center" width="50%">

### Dr. S. Srikar Bharadwaj

*Co-Lead & Clinical Strategy*

</td>
<td align="center" width="50%">

### Dr. Jayalaxmi Srinivasan

*Co-Lead & Architect*

</td>
</tr>
</table>

---

## 🏆 Hackathon Context

<table>
<tr>
<td>

**Event:** Health-a-thon 2026 — India's Leading Health Ecosystem Comes Together

**Track:** 🎗️ Cancer

**Use Case:** Patient Registry & Population Health

**Primary User:** Doctor / Care Team

**Solution Type:** Building a new solution from scratch

</td>
<td>

**Organized By:**
- **Koita Foundation** — Driving Digital Health & AI adoption in India
- **IIT Bombay - KCDH** — India's first academic centre dedicated to Digital Health
- **Federation of Obstetric and Gynaecological Societies of India (FOGSI)**
- **National Cancer Grid** — 370+ member institutions serving nearly 60% of all cancer patients in India
- **Research Society for the Study of Diabetes in India**

</td>
</tr>
</table>

---

## 🙏 Acknowledgements

We would like to express our gratitude to:

- **Koita Foundation** and **IIT Bombay - KCDH** for organizing the Health-a-thon and fostering innovation in Digital Health and AI
- **National Cancer Grid** for their monumental work connecting 370+ cancer care institutions across India
- **FOGSI** and **Research Society for the Study of Diabetes in India** for their commitment to improving healthcare outcomes
- The broader **open-source biomedical AI community** — including the teams behind BioBERT, XGBoost, SHAP, and LIME — whose tools make this work possible

---

<p align="center">
  <strong>Gut Instinct</strong> — Because early detection shouldn't be left to chance.
</p>

<p align="center">
  <em>Built with ❤️ for the Health-a-thon 2026</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Made_for-Health--a--thon_2026-FF6B6B?style=for-the-badge" alt="Made for Health-a-thon 2026"/>
</p>
