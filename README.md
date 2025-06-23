# 📈 Causal Impact Analysis of Online Advertising

As part of a Causal Analytics assignment at the Carlson School of Management, this project evaluates the causal impact of **sponsored search ads** using a **natural experiment** at Bazaar.com. The goal was to determine whether online advertising genuinely drives incremental web traffic and whether the investment is justified.

---

## 🎯 Objective

- Measure the **true causal impact** of sponsored Google ads on website traffic.
- Correct inflated ROI calculations by distinguishing **incremental** vs. **non-incremental** traffic.
- Inform ad spend decisions using evidence-based, statistical methods.

---

## 🧪 Methodology

This project applies **causal inference techniques** using observational data:

- ✅ **Pre-post regression** (First Difference)
- ✅ **Parallel trends verification**
- ✅ **Difference-in-Differences (DiD)** with **two-way fixed effects**

---

## 🛠️ Tools & Skills

- **Language**: R
- **Libraries**: `dplyr`, `ggplot2`, `plm`
- **Techniques**: A/B Testing, Panel Data Regression, Causal Inference, ROI Analysis

---

## 🧾 Data Context

- **Platform**: Bazaar.com (multi-channel video service provider)
- **Natural Experiment**: Google sponsored ads paused for 3 weeks due to a technical glitch, while other platforms (e.g., Bing) remained unaffected.
- **Unit of Analysis**: Weekly traffic from different search platforms (sponsored + organic).

---

## 📊 Key Findings

- A **simple pre-post comparison** on Google alone suggested negligible effect.
- However, **DiD regression with fixed effects** revealed a **statistically significant 67.3% drop** in traffic after ads were paused.
- This effect represents the **true incremental value** of the sponsored ads.

---

## 💰 ROI Recalculation

- Original ROI by management: **320%**, based on total revenue/cost.
- Updated ROI using DiD-estimated incremental clicks: **182.4%**
  - Calculation:
    - Revenue per click: $2.52  
    - Cost per click: $0.60  
    - Adjusted ROI = `(Revenue - Cost) / Cost`

---

## 🔍 Lessons Learned

- Simple attribution often **overstates impact**; causal methods are crucial.
- DiD with fixed effects helps isolate treatment effects in observational settings.
- Even profitable channels can be **optimized with better targeting** and **spend efficiency**.
