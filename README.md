# Data Proof: E-Commerce Statistical Analysis & Hypothesis Testing

A statistical analysis pipeline built in Python to evaluate key e-commerce operational strategies, promotional impacts, UI conversion rates, and customer segment metrics.

## Key Analyses

- **A/B Checkout UI Test**: Welch's t-test and Two-Proportion Z-test comparing Average Order Value (AOV) and conversion rate across checkout UI variants.
- **Promotional Voucher Impact**: Paired t-test and Wilcoxon signed-rank test measuring pre- vs. post-promotion customer spend.
- **Loyalty Tier Spend Analysis**: One-Way ANOVA and Tukey's HSD post-hoc test evaluating annual spend variance across loyalty tiers.
- **Payment Method Dependencies**: Chi-Square test of independence evaluating return and cancellation rates across payment methods.
- **Automated Deliverables**: Automated generation of data visualizations, structured JSON results, and a Word (`.docx`) summary report.

## Repository Structure

```text
.
├── main.py                             # Execution pipeline & analysis runner
├── ecommerce_hypothesis_data.csv       # E-commerce transaction dataset
├── statistical_analysis_notebook.ipynb # Analysis notebook
├── requirements.txt                    # Project dependencies
└── output/                             # Generated charts & summary report
```

## Setup & Execution

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the analysis pipeline:
   ```bash
   python main.py
   ```
