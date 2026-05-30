# Shaha Finlease — NPL Recovery Analytics

**Case Study | Data Analyst Assessment**  
**Tools:** Python · Pandas · NumPy · Matplotlib · Seaborn

---

## Business Context

Shaha Finlease is an NBFC managing a portfolio of **9,000 Non-Performing Loan (NPL) accounts** with **₹143 Cr in outstanding debt**. Recovery operations relied on manual channel assignment with no data-driven prioritisation.

**Objective:** Analyse the portfolio to identify recovery drivers, segment borrowers into actionable groups, detect channel assignment inefficiencies, and recommend a data-backed recovery strategy including a 3-use-case AI roadmap.

---

## Key Findings

| Finding | Detail |
|---|---|
| Portfolio size | 9,000 accounts · ₹143 Cr outstanding |
| Current recovery rate | 17.73% — 68.1% of accounts at zero recovery |
| Strongest recovery driver | Payment history — **9x gap** between Good (40.1%) and Poor (4.6%) borrowers |
| Channel mismatch | **5,173 accounts (57%)** assigned to wrong channel — ₹83 Cr misaligned |
| Estimated uplift | **~₹82 Lakhs** additional recovery from channel reallocation alone |
| Target recovery rate | 21–23% after recommended channel fix |

---

## Analysis Structure

```
1. Setup & Data Loading
2. Exploratory Data Analysis (EDA)
3. Identifying Recovery Drivers (4 key signals)
4. Borrower Segmentation (5-tier model)
5. Channel Mismatch Detection — the ₹83 Cr problem
6. Rule-Based Scoring Model (0–100)
7. Impact Estimation
8. AI Roadmap (3 use cases)
```

---

## Segmentation Model

| Segment | Accounts | Outstanding | Recovery % | Priority | Channel |
|---|---|---|---|---|---|
| 🟢 Quick Win | 1,495 | ₹24.25 Cr | 41.37% | P1 — Immediate | Call |
| 🟡 High Potential | 608 | ₹9.56 Cr | 21.45% | P1 — Immediate | Field |
| 🟠 Mid Tier | 2,368 | ₹37.81 Cr | 14.68% | P2 — This Week | Call |
| 🔵 Watch List | 3,961 | ₹61.93 Cr | 12.14% | P3 — Monitor | Call |
| 🔴 High Risk | 568 | ₹9.46 Cr | 2.23% | P4 — Last Resort | Legal |

---

## Scoring Model Weights

| Driver | Weight | Rationale |
|---|---|---|
| Payment History | 40 pts | Strongest signal — 9x recovery gap |
| Last Outcome | 25 pts | Borrower attitude at last contact |
| Days Past Due | 20 pts | Urgency — earlier debt recovers better |
| Contact Attempts | 15 pts | Diminishing returns after 5 contacts |

Transparent rule-based scoring chosen over black-box ML for explainability — field agents and managers need to understand and trust the scores.

---

## AI Roadmap

| Use Case | Timeline | Expected Benefit |
|---|---|---|
| LLM-Powered Personalized Call Scripts | 6–8 weeks | Higher agent conversion, tailored per borrower profile |
| Propensity Scoring & Auto Channel Routing | 2–3 months | Eliminates manual mismatch, auto-assigns 9,000 accounts daily |
| Sentiment Analysis on Call Transcripts | 3–4 months | Recovers accounts that fall through cracks due to lost nuance |

---

## Repository Structure

```
shaha-finlease-npl-recovery/
├── shaha_finlease_npl_recovery.ipynb   # Main analysis notebook
├── shaha_finlease_recovery_dataset.csv # Dataset (9,000 accounts, 12 variables)
└── README.md                           # This file
```

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/saarimds/shaha-finlease-npl-recovery.git
cd shaha-finlease-npl-recovery

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch notebook
jupyter notebook shaha_finlease_npl_recovery.ipynb
```

---

**Author:** Mohammad Saarim Khan  
[GitHub](https://github.com/saarimds) · [LinkedIn](https://linkedin.com/in/m-saarim-khan)
