**A/B Testing E-Commerce Product Page**

**📌 Project Overview**

This project simulates an A/B test for an e-commerce platform to evaluate the impact of a redesigned product page on conversion rates. The business goal is to increase the average conversion rate from 13% to 15%.

To minimize risks of a full rollout, we design an experiment using a subset of users and validate results through statistical testing. We leverage a Kaggle dataset containing user sessions and conversions to simulate the experiment.

⸻

🎯 Business Problem
	•	Current conversion rate: 13%
	•	Target uplift: +2% (i.e., achieve ≥15%)
	•	Key Question: Does the new design significantly improve conversions compared to the old design?

⸻

🧪 Methodology

1. Experiment Design
	•	Control Group (A): Users exposed to old product page.
	•	Treatment Group (B): Users exposed to new product page.
	•	Independent Variable: Page design (old vs new).
	•	Dependent Variable: Conversion (0 = no purchase, 1 = purchase).

2. Hypothesis
	•	Null Hypothesis (H₀): p_{new} = p_{old}
	•	Alternative Hypothesis (H₁): p_{new} \neq p_{old}
	•	Significance Level (α): 0.05 (95% confidence).

3. Sample Size Estimation
	•	Effect size calculated from 13% → 15% expected uplift.
	•	Power = 0.8, Alpha = 0.05.
	•	Used power analysis with statsmodels to compute minimum sample size per group.

4. Data Preprocessing
	•	Removed duplicate users/sessions.
	•	Dropped bot traffic and incomplete records.
	•	Created binary conversion variable.

5. Statistical Testing
	•	Conducted a two-tailed z-test for proportions.
	•	Measured statistical significance (p-value).
	•	Compared uplift in conversion rates.

⸻

📊 Tools & Libraries
	•	Python
	•	Pandas, NumPy – Data processing
	•	Statsmodels, Scipy – Statistical analysis & power test
	•	Matplotlib, Seaborn – Data visualization

⸻

✅ Success Criteria
	•	Conversion rate in treatment group ≥ 15%.
	•	Difference in conversion rates statistically significant (p-value < 0.05)
