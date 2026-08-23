# 📊 Telco Customer Churn Analysis

An end-to-end Business Intelligence project built in Power BI that analyzes why customers leave, which segments are most at risk, how much revenue is lost, and what can be done about it.

**Developed by:** [Sameh Elaraby](https://github.com/samehmohamed2610)

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=flat)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-5C2D91?style=flat)

---

## 📌 Overview

Churn is one of the biggest threats to any subscription business: every lost customer removes recurring revenue and reduces long-term customer value.

This report studies customer demographics, tenure, contracts, charges, payment methods, subscribed services, and support interactions to expose churn patterns and turn them into retention opportunities.

The dashboard follows a storytelling flow — starting from the size of the churn problem, moving through customer, service, and payment behavior, and ending with concrete business recommendations.

---

## 📈 Headline Numbers

| Metric | Value |
| --- | --- |
| Total customers | 7,043 |
| Churned customers | 1,869 |
| Churn rate | 26.54% |
| Retention rate | 73.46% |
| Total monthly charges | $456.12K |
| Monthly revenue lost | $139.13K (30.50%) |
| Avg. tenure — retained | 37.57 months |
| Avg. tenure — churned | 17.98 months |

---

## 🎯 Business Objectives

1. **Measure churn** — quantify the overall churn rate and the monthly revenue leaking out of the business.
2. **Segment risk** — isolate high-risk cohorts based on tenure thresholds and demographic profiles.
3. **Explain the drivers** — link churn to contract commitment and payment friction.
4. **Assess services** — expose vulnerabilities in core and add-on services such as fiber optic, security, backup, and tech support.
5. **Act on insight** — convert the findings into precise, data-driven retention strategies.

---

## 📂 Dataset

Customer-level records covering:

- **Demographics** — gender, senior or young citizen, partner, dependents
- **Tenure** — months with the company
- **Contract type** — month-to-month, one year, two year
- **Services** — fiber optic, DSL, phone, multiple lines, online security, online backup, tech support
- **Billing and payment** — electronic check, mailed check, bank transfer, credit card, paperless billing
- **Charges** — monthly and total
- **Support** — technical and administrative tickets
- **Churn status**

---

## 🛠️ Tools and Technologies

| Tool | Purpose |
| --- | --- |
| Power Query | Data cleansing, shaping, and transformation |
| Power BI | Star-schema data modeling and report design |
| DAX | Measures, churn rates, and cohort calculations |
| Bookmarks & Drillthrough | Page navigation and detail-level exploration |
| KPI Dashboards | Executive-level summary of churn and revenue impact |

---

## 🖥️ Dashboard Walkthrough

### 🏠 Landing Page

Introduces the project and provides navigation into the analytical report.

![Landing Page](screenshots/0.png)

### 📊 Demographic Analysis

Profiles the customer base — gender, senior or young citizen status, partner status, and dependents — against churn behavior.

- Churn is almost identical across genders: **26.92%** for female and **26.16%** for male customers.
- Demographics alone do not explain churn, which shifts the investigation toward contracts, services, and payment behavior.

![Demographic Analysis](screenshots/1.png)

### 📅 Tenure and Contracts

Evaluates how long customers stay and how contract commitment affects retention.

| Contract type | Customers | Churn rate |
| --- | --- | --- |
| Month-to-month | 3,875 | **42.71%** |
| One year | — | 11.27% |
| Two year | — | 2.83% |

Retained customers average **37.57 months** of tenure, against **17.98 months** for churned customers.

![Tenure and Contracts](screenshots/2.png)

### 🎫 Tickets and Support Interactions

Analyzes administrative and technical ticket volume across segments.

- Senior citizens churn at **41.68%** with 586 admin tickets, against **23.61%** for young citizens with 3,046 admin tickets.
- Admin tickets split **2,747** for retained customers against **885** for churned ones, revealing distinct support-friction patterns per group.

![Tickets and Support](screenshots/3.png)

### 💰 Charge Analysis

Breaks down total and monthly charges across demographics and retention cohorts.

- **Total charges:** $13.19M from retained customers, against $2.86M from churned customers.
- **Monthly charges:** $364.96K from young citizens and $91.15K from senior citizens.
- Retained customers contribute **$316.99K** monthly, against **$139.13K** lost to churn.

![Charge Analysis](screenshots/4.png)

### 💳 Payment Analysis

Examines payment methods, paperless billing, and their correlation with dropout.

| Payment method | Churn rate |
| --- | --- |
| Electronic check | **45.29%** (2,365 customers) |
| Mailed check | 19.11% |
| Bank transfer | 16.71% |
| Credit card | 15.24% |

Automated payment methods correlate with markedly lower churn.

![Payment Analysis](screenshots/5.png)

### 🌐 Services Analysis

Evaluates core connectivity options alongside value-added services.

**Internet service**

| Service | Churn rate |
| --- | --- |
| Fiber optic | **41.89%** |
| DSL | 18.96% |
| No internet | 7.40% |

**Add-on services**

| Add-on | Without | With |
| --- | --- | --- |
| Online security | 41.77% | 14.61% |
| Online backup | 39.93% | 21.53% |
| Tech support | 41.64% | 15.17% |

Add-on services act as strong retention anchors — customers without them churn roughly three times more often.

![Services Analysis](screenshots/6.png)

---

## 💡 Strategic Recommendations

**01 · Contract strategy** — Move customers off month-to-month plans, which churn at 42.71%, using targeted upgrade incentives and loyalty discounts.

**02 · Early-tenure retention** — Churned customers last only 17.98 months on average, so strengthen onboarding and proactive engagement in the first year of the lifecycle.

**03 · Revenue protection** — Recover the $139.13K monthly loss, 30.50% of revenue, by prioritizing high-value cohorts for tailored retention offers.

**04 · Service experience** — Watch senior citizens and repeat ticket submitters, and resolve friction points before cancellation.

**05 · Payment experience** — Migrate customers away from electronic checks, which churn at 45.29%, toward automatic bank transfer or credit card.

---

## 🚀 Future Improvements

- **Predictive churn modeling** — score individual churn probability with classification models such as Random Forest or XGBoost via Python or R.
- **Customer Lifetime Value forecasting** — estimate long-term customer value with advanced DAX and regression to optimize acquisition cost.
- **Automated risk alerts** — trigger Power BI and Power Automate notifications when ticket volume or billing patterns spike.
- **What-if scenario simulator** — model revenue saved under different contract and discount strategies using parameters.
- **RFM and behavioral clustering** — group customers by recency, frequency, and monetary value to drive automated retention campaigns.

---

## 📁 Repository Structure

```
Customer-Churn-Analysis/
├── data/                        # Raw and cleaned dataset
├── screenshots/                 # Dashboard page exports
├── Customer_Churn_Analysis.pbix # Power BI report file
└── README.md
```

---

## ▶️ How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/samehmohamed2610/Customer-Churn-Analysis.git
   ```
2. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
3. Open `Customer_Churn_Analysis.pbix`.
4. If the data source path differs on your machine, update it under **Transform data → Data source settings**, then refresh.

---

## 👤 Author

**Sameh Elaraby**
GitHub: [@samehmohamed2610](https://github.com/samehmohamed2610)

If this project was useful to you, consider giving the repository a ⭐.
