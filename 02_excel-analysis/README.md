# Supplement Sales Exploratory Data Analysis (Excel & Power Query)

## Project Overview

This project focuses on **exploratory data analysis (EDA)** using a **synthetic supplement sales dataset**. The goal is to **demonstrate analytical reasoning, data understanding, and structured thinking** using Excel and Power Query. Assumed analysis is Market Level Analysis.

This project shows **how I think with data**: asking the right questions, validating assumptions, and avoiding misleading conclusions.

---

## Dataset Description

The dataset contains transactional sales records for supplement products sold across multiple platforms and locations.

### Core Columns

* Date
* Product Name
* Category
* Units Sold
* Units Returned
* Price
* Revenue
* Discount (percentage)
* Location (USA, UK, Canada)
* Platform (Amazon, Walmart, iHerb)

**Dataset Source:** (https://www.kaggle.com/datasets/zahidmughal2343/supplement-sales-data)

### Engineered Columns (Created in Power Query)

* **Net Units Sold** = Units Sold − Units Returned
* **Discounted Price** = Price × (1 − Discount)
* **Return Rate** = Units Returned ÷ Units Sold
* **Net Revenue** = Discounted Price × Net Units Sold
* **Year, Month, Day** (derived from Date)

These transformations were intentionally done in **Power Query** to maintain a clean, reproducible data pipeline.

---

## Important Data Context

* The dataset is **Balanced** and **synthetic** (AI-generated). Realized by exploring it.
* No unit-size or packaging information is available

Because of this:

* Absolute business conclusions are avoided
* Analysis focuses on **distribution, structure, and behavior** of the dataset rather than profitability, and actual market level insights.

---

## Key Analysis Questions & Reasoning

### 1. Overall Market Structure (Category Dominance)

**Question:** What does the overall supplement market look like by category?

**My Approach:**

* Pivot table with Category as rows
* Metrics:

  * Sum of Net Units Sold
  * Sum of Net Revenue
  * % of Total Net Revenue
 
<img width="700" height="212" alt="image" src="https://github.com/user-attachments/assets/d7a78dc9-af0f-430a-8c85-7d9e7191b502" />

**Insight:**

* Vitamins and Minerals dominate the market (37% combined)
* Performance and Protein (25%)
* Remaining categories are evenly distributed

---

### 2. Product-Level Distribution

**Question:** Are results driven by a few products or evenly spread?

**Approach:**

* Product Name vs Net Revenue
* % of Total Net Revenue per product
* Checked Count of Products by Category

**Insight:**

* Each product contributes roughly 6% of revenue
* (Confirmed) Earlier Category dominance was due to more Counts
* Data gave 'balanced' and 'synthetic.

---

### 3. Platform Behavior

**Question:** How do platforms contribute within each category?

**Approach:**

* Category → Platform hierarchy
* Metrics:

  * % of Net Units Sold
  * % of Net Revenue
  * Average Discount
  * Average Return Rate

**Insight:**

* Platforms contribute almost equally
* Discounts and return rates are consistent

This confirms there is **no platform dominance**, reinforcing the synthetic nature of the dataset.

---

### 4. Geographic Behavior

**Question:** How does category performance vary by location?

**Approach:**

* Category → Location breakdown
* Same metrics as platform analysis

<img width="708" height="618" alt="image" src="https://github.com/user-attachments/assets/9324ac4b-a2ae-4753-9dc4-180dcef9aa85" />


**Insight:**

* USA, UK, and Canada show near-equal contribution
* No region-specific anomalies detected

Again, the value here is **recognition of the balance of the dataset**.

---

### 5. Time-Based Behavior (Critical Validation Step)

**Question:** How does performance change over time?

**Approach:**

* Year → Location breakdown
* Checked row counts per year and month

**Insight::**

* Years 2020–2024 have full data coverage
* 2025 contains only **January–March**

I excluded 2025 from year-over-year trend comparisons
 Apparent decline is due to **partial-year data**, not performance


---

## Why Net Revenue Was Used

For market analysis, **Net Revenue** was preferred over raw Revenue because:

* Discounts materially affect realized value
* Returns reduce the actual sales impact

This aligns analysis with **economic reality**, even in a synthetic dataset.

---

## Tools Used

* Microsoft Excel
* Power Query
* Pivot Tables

No dashboards were built, reflecting a **question workflow**.

---

## What This Project Demonstrates

* Analytical reasoning.
* Data validation before insight generation
* Clear distinction between data limitations and insights

---

## Final Note

This project is intentionally exploratory.

It shows **how I think as a data analyst**, how I question data structure, and how I avoid misleading conclusions.

---

If you’re a fellow learner, and this helped you think differently about data.
I do a step by step kinda tutorial on how to turn numbers into insights, this same project.
Here are links to the project; 

Part 1 (https://open.substack.com/pub/datanavi/p/step-by-step-data-reasoning-part?r=2xtnpd&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true)

Part 2 ([https://open.substack.com/pub/datanavi/p/step-by-step-data-reasoning-part-320?r=2xtnpd&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true])

If you’re a senior analyst, I’d value mentorship.

If you’re hiring for junior roles, I’m confident I’d be one of the strongest candidates to train and grow.

