# Strategic Predictive Modeling for Bank Term Deposit Subscriptions

A financial analytics project that shifts a bank from **mass telemarketing** to **precision marketing** by predicting a customer’s **propensity to subscribe** to a term deposit using structured data + interpretable statistical diagnostics.

## 🎯 Business Problem
Term deposits are crucial for banking stability, but broad telemarketing creates:
- high operational sunk costs per call
- customer fatigue and brand damage

This project uses data-driven targeting to move from **“call everyone”** to **“call the right people.”**

## 🧰 Tools & Methods
- **JMP**: Fit Y by X, Odds Ratios (OR), Confidence Intervals (CI), ROC/AUC diagnostics  
- **Data sampling strategy**: stratified balanced sampling (50/50) to avoid the “accuracy paradox”
- **Feature engineering**: balance binning (Positive vs Negative) for financial solvency threshold

## 🧾 Dataset
- Observations: **N = 10,395**
- Target: **Subscription outcome (yes/no)**  
- Features include demographics, financial status, and behavioral/campaign history.

> Note: Dataset is used for academic analysis and modeling demonstration.

---

## 🔍 Key Insights (What Actually Moved the Needle)

### 1) Behavioral signal beats demographics
- Call **duration** showed excellent discrimination with **ROC AUC ≈ 0.808**
- Strong tradeoff balance: **~76.8% precision** and **~61.9% recall**

### 2) Campaign fatigue is real
- Each additional campaign contact reduces the odds of subscription (diminishing returns)
- Recommendation: cap attempts to avoid negative ROI

### 3) Biggest categorical lift: previous success + positive balance
- “Previous campaign success” created a major odds lift (very strong repeat-likelihood segment)
- Positive balance customers show substantially higher odds of subscribing (economic gatekeeper)

### 4) Strategic filter: significance ≠ impact
With a large dataset, many variables become statistically significant — so this project prioritizes **effect size (OR)** and real business impact over “p-values only.”

---

## ✅ Managerial Recommendations
- Lead scoring: prioritize customers with previous success massively higher than unknown leads
- Contact strategy: cap campaign contacts to prevent fatigue
- Execution: focus on agent training to improve call quality and engagement duration

---

## 📦 Deliverables
- Cleaned dataset (CSV)
- JMP analysis file (.jrp)
- Final report (PDF/DOCX)
- Dashboard/screenshots (ROC curve, Odds Ratio table, Fit Y by X outputs)

---

## 📁 Repository Structure
```text
.
├─ data/
│  ├─ raw/
│  └─ processed/
├─ analysis/
│  └─ jmp/
├─ reports/
├─ assets/
└─ README.md

