# Website Conversion A/B Test

End-to-end A/B testing project analyzing whether a redesigned website increases user conversion, using Python for statistical testing and Tableau for stakeholder-facing visualization.

**[📄 Read the full case study (PDF)](./AB_Test_Case_Study.pdf)** | **[📊 View the interactive Tableau dashboard](#)**

---

## Business Problem

A UX team redesigned a website's product page, believing it would improve conversion. Before rolling it out company-wide, the business needed a statistically sound answer to one question:

> **Does the new design actually convert better, or could the observed difference be random chance?**

Users were randomly split into a control group (current design) and a treatment group (new design), and their behavior was tracked across 5,000 sessions.

## Key Result

| Metric | Group A (Control) | Group B (Treatment) |
|---|---|---|
| Conversion Rate | 5.40% | **14.07%** |
| Sample Size | 2,519 | 2,481 |

- **Result:** Statistically significant lift of 7.04–10.30 percentage points (95% CI), p < 0.001
- **Consistency:** The lift held across every device type and every UK region tested — not driven by any single segment
- **Recommendation:** Ship the new design to all users

## Approach

1. **Business framing** — defined hypotheses and success metric before touching the data
2. **Data quality checks** — validated no missing values, no duplicate users, balanced group randomization
3. **Exploratory analysis** — checked Page Views, Time Spent, Device, and Location were balanced across groups (ruling out confounding variables)
4. **Power analysis** — confirmed the sample size (5,000) far exceeded the ~364 minimum required to detect this effect reliably
5. **Hypothesis testing** — two-proportion z-test on conversion; t-tests on Page Views and Time Spent; chi-square test on Device
6. **Segmentation analysis** — verified the lift held consistently across Device and Location subgroups
7. **Business translation** — converted statistical output into a plain-language recommendation and case study

## Tools & Skills

`Python` (pandas, scipy, matplotlib) · `SQL` · `Tableau` · Hypothesis Testing · Power Analysis · A/B Testing · Statistical Inference

## Repo Structure

```
├── ab_testing.csv                 # Raw dataset
├── ab_testing_analysis.ipynb      # Full analysis notebook (stats + code)
├── AB_Test_Case_Study.pdf         # Business-facing case study write-up
├── dashboard_screenshot.png       # Tableau dashboard preview
└── README.md
```

## Dataset

5,000 user sessions with columns: `User ID`, `Group` (A/B), `Page Views`, `Time Spent`, `Conversion` (Yes/No), `Device`, `Location`.

## Dashboard Preview

*(Add your dashboard screenshot here, e.g. `![Dashboard](./dashboard_screenshot.png)`)*

---

**Author:** [Your Name] · [LinkedIn](#) · [Portfolio](#)
