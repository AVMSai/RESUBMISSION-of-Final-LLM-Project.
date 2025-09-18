Employee Sentiment Analysis

  Project Overview
This project analyzes employee email communications to evaluate **sentiment and engagement**.  
It implements **six main tasks**:
1. **Sentiment Labeling** — Classify each message as Positive, Negative, or Neutral using VADER.
2. **Exploratory Data Analysis (EDA)** — Understand sentiment distribution, trends, and active employees.
3. **Monthly Sentiment Scoring** — Assign scores (+1 / –1 / 0) and compute monthly totals per employee.
4. **Employee Ranking** — Identify top employees by sentiment (Positive, Neutral, Negative).
5. **Flight Risk Detection** — Flag employees with ≥4 negative messages in any rolling 30-day period.
6. **Predictive Modeling** — Build a linear regression model to analyze sentiment score trends.

---

 Key Findings
- **Sentiment distribution:** Most emails are **neutral**, with fewer positive/negative ones.  
- **Top senders:** A small group of employees account for most messages.  
- **Monthly sentiment trends:** Fluctuations align with periods of high communication (e.g., deadlines).  
- **Flight risks:** No employees were flagged under the strict criteria (≥4 negative emails in 30 days).  
- **Predictive modeling:** Linear regression showed **low explanatory power (R² ≈ 0)** — sentiment is influenced by more complex factors than message length/frequency.

---

 Rankings (Latest Month: Example `2011-12`)
| Employee Email          | Monthly Score | Rank Type     |
|--------------------------|---------------|---------------|
| eric.bass@enron.com      | 5             | Top Positive  |
| lydia.delgado@enron.com  | 5             | Top Positive  |
| patti.thompson@enron.com | 5             | Top Positive  |
| john.arnold@enron.com    | 1             | Top Negative  |
| johnny.palmer@enron.com  | 1             | Top Negative  |
| kayne.coulter@enron.com  | 2             | Top Negative  |

 In some months, “Top Negative” may still include positive scores if no employees had negative sentiment.

---

light Risk Employees
- **Total flagged:** 0  
- **List:** *None*  
- Explanation: No employee sent ≥4 negative emails in any 30-day rolling window.

---
 Predictive Model Performance
- **Model:** Linear Regression  
- **Features:** message count per month, average message length  
- **Metrics:**
  - Mean Squared Error (MSE): ~1.2  
  - R² Score: ~0.05  
- **Conclusion:** Sentiment cannot be predicted well with these simple features. Advanced NLP features are needed.

---

