# Week 3 Task: Statistical Analysis and Hypothesis Testing in Python

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Complete](https://img.shields.io/badge/Status-Complete-brightgreen.svg)]()

## 📌 Project Overview
This repository provides an end-to-end, production-grade statistical analysis and hypothesis testing framework built in Python. Designed for e-commerce business analytics, this project evaluates four key business initiatives using rigorous parametric and non-parametric statistical methods.

The pipeline automatically synthesizes data, executes hypothesis tests, verifies statistical assumptions (normality, homoscedasticity), computes effect sizes, exports publication-ready diagnostic visualizations, generates an interactive Jupyter notebook, and compiles a complete Word report (`.docx`).

---

## 🎯 Hypotheses & Statistical Methodology

| # | Business Case | Research Question | Primary Statistical Test | Secondary / Diagnostic Test | Effect Size Metric |
|---|---|---|---|---|---|
| **H1** | **A/B Checkout UI** | Does the new checkout UI increase Average Order Value (AOV) & conversion rate? | **Welch's Independent T-Test** | Two-Proportion Z-Test, Shapiro-Wilk Normality, Levene's Test | Cohen's *d* |
| **H2** | **Promotional Vouchers** | Do targeted discount vouchers increase customer monthly spend? | **Paired Samples T-Test** | Wilcoxon Signed-Rank Test | Cohen's *d* |
| **H3** | **Loyalty Program Tiers** | Does annual customer spend differ significantly across loyalty tiers? | **One-Way ANOVA** | Tukey HSD Post-Hoc Test, Levene's Variance Test | Eta-Squared ($\eta^2$) |
| **H4** | **Payment Methods** | Is payment method selection associated with order outcome (e.g., return rates)? | **Chi-Square Test of Independence** | Expected Frequencies Verification | Cramér's *V* |

---

## 📁 Repository Directory Structure

```text
d:/data-science/data-proof/
│
├── output/                                     # Generated analysis artifacts
│   ├── figures/                                # High-resolution visualization charts (300 DPI)
│   │   ├── fig1_ab_test_aov_distribution.png   # A/B Checkout UI AOV Distribution
│   │   ├── fig2_paired_spend_comparison.png    # Pre vs Post Promotional Spend Boxplot
│   │   ├── fig3_anova_loyalty_spend.png        # Loyalty Tier Annual Spend Comparison
│   │   ├── fig4_chi_square_heatmap.png         # Payment Method vs Outcome Contingency Heatmap
│   │   └── fig5_normality_qqplots.png          # Q-Q Diagnostic Plots & Normality Diagnostics
│   ├── Week3_StatisticalAnalysis_Report.docx  # Formatted Word Document summary report
│   └── statistical_results.json                # JSON dump of test statistics, p-values & effect sizes
│
├── .gitignore                                  # Git ignore rules for bytecode, venv, and cache
├── ecommerce_hypothesis_data.csv               # Synthetic e-commerce dataset (1,500 customer records)
├── main.py                                     # Master script executing the full analytical pipeline
├── README.md                                   # Comprehensive project documentation
├── requirements.txt                            # Python package dependencies
├── statistical_analysis_notebook.ipynb         # Interactive Jupyter Notebook
└── submission_description.txt                  # Report description text for portal submission (200+ words)
```

---

## ⚙️ Requirements & Installation

### Prerequisites
- **Python 3.8+**
- **pip** package manager

### Installation
Clone the repository and install required Python packages:

```bash
# Install dependencies
pip install -r requirements.txt
```

#### Key Dependencies
- `pandas` (>= 2.0.0) – Data manipulation and aggregation
- `numpy` (>= 1.24.0) – Numerical computations & data generation
- `scipy` (>= 1.10.0) – Hypothesis testing (T-tests, ANOVA, Chi-Square, Wilcoxon)
- `statsmodels` (>= 0.14.0) – Post-hoc analysis (Tukey HSD) & proportion tests
- `matplotlib` & `seaborn` – Statistical data visualization
- `python-docx` – Programmatic Word report generation

---

## 🚀 Execution Instructions

To execute the complete end-to-end analytical pipeline, run `main.py`:

```bash
python main.py
```

### What `main.py` performs automatically:
1. **Dataset Generation / Loading**: Creates or loads `ecommerce_hypothesis_data.csv` with 1,500 customer records.
2. **Statistical Testing**: Evaluates all 4 hypotheses, checking parametric assumptions and calculating effect sizes.
3. **Data Visualization**: Saves high-resolution figures to `output/figures/`.
4. **JSON Metrics Export**: Writes exact test outputs to `output/statistical_results.json`.
5. **Interactive Notebook Generation**: Builds `statistical_analysis_notebook.ipynb`.
6. **Executive Report Building**: Compiles `output/Week3_StatisticalAnalysis_Report.docx`.

---

## 📊 Statistical Summary of Results

| Hypothesis ID | Business Context | Test Applied | Key Test Statistics | Decision on $H_0$ | Business Finding |
|---|---|---|---|---|---|
| **H1: A/B Checkout UI** | Legacy vs New UI AOV | Welch's T-Test | $t = 6.656, p < 0.0001, d = 0.344$ | **Reject $H_0$** | New UI significantly increases AOV ($94.20 vs $85.50). |
| **H1: Conversion Rate** | Legacy vs New UI Conversion | Two-Proportion Z-Test | $z = 2.518, p = 0.0118$ | **Reject $H_0$** | New UI conversion rate is 19.0% vs 14.0% for Legacy. |
| **H2: Promo Voucher** | Pre vs Post Voucher Spend | Paired T-Test | $t = 48.790, p < 0.0001, d = 1.260$ | **Reject $H_0$** | Vouchers produce a large, statistically significant spend uplift. |
| **H3: Loyalty Tier Spend** | Spend across 4 Tiers | One-Way ANOVA | $F = 1148.92, p < 0.0001, \eta^2 = 0.697$ | **Reject $H_0$** | Strong tier differentiation; Tukey HSD confirms all pairs $p < 0.001$. |
| **H4: Payment Method** | Payment Choice vs Outcome | Chi-Square Test | $\chi^2 = 72.18, p < 0.0001, V = 0.155$ | **Reject $H_0$** | Significant dependence; Buy-Now-Pay-Later (BNPL) exhibits higher return rates. |

---

## 📤 Submission Checklist & Instructions

When submitting this project:
1. **Upload Report Document**: Attach `output/Week3_StatisticalAnalysis_Report.docx` to the portal's submission field.
2. **Submit Portal Description**: Copy the text from `submission_description.txt` and paste it into the project description field (meets the 200+ word requirement).
3. **Provide Repository URL**: Attach the link to your public GitHub repository containing this codebase.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
