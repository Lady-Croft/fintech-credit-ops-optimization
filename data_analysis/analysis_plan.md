# Data Analysis Checklist
- [X] Handle Nulls & Outliers: Identify missing Income or CreditScore values. Check for "impossible" data.<br>

_The dataset was audited across 100,000 records, confirming 100% completeness with zero missing values in critical fields such as Annual_Income and Credit_Score._
_A logical constraint check verified that there are no "impossible" entries, specifically recording zero negative loan amounts, zero interest rates exceeding 100%, and zero age outliers outside the 18–100 range._
_With a mean income of approximately $110,037 and a median credit score of 573, the data shows a symmetrical distribution and a robust middle-class borrower profile, making it a high-quality foundation for predictive modeling without the need for data imputation or row deletion._
- [ ] Feature Scaling: Determine if LoanAmount and AnnualIncome need normalisation for accurate comparison.<br>
- [ ] Target Distribution: Calculate the baseline Default Rate ($NPL\%$) across the entire 10k dataset.<br>
- [ ] Univariate Correlation: Which single factor has the highest correlation ($r$) with default? (Is it InterestRate? DTI Ratio? EmploymentLength?)<br>
- [ ] Debt-to-Income (DTI) Stress Test: Segment users by DTI brackets (e.g., 0-20%, 21-40%, etc.) to find the "Safety Threshold."<br>
- [ ] Interest Rate Sensitivity: Compare the InterestRate charged to defaulters vs. non-defaulters. Are we charging enough to cover the risk?<br>
- [ ] Demographic Cross-Tabulation: Do certain Gender or Employment status show significantly more resilience during repayment?<br>
- [ ] Segment Profitability (Unit Economics): Calculate the Net Contribution per segment <br>
- [ ] "Leak" Identification: Identify the specific "Net-Negative" segment (e.g., Low Income + High Interest + Short Term).<br>
- [ ] Strategy Validation: Simulate how a 10% reduction in lending to the highest-risk segment impacts the overall Portfolio ROI.<br>
