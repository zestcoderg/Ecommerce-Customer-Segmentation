# 🛒 E-Commerce Customer Segmentation & Revenue Strategy

### 📄 Executive Summary
This project focuses on **optimizing marketing ROI** by segmenting a customer base of 4,000+ users using **RFM Analysis** (Recency, Frequency, Monetary). 

Instead of a "one-size-fits-all" marketing approach, I developed a Python-based segmentation engine and a Power BI Strategy Dashboard to identify "Champions" (High Value) vs. "Hibernating" (At Risk) customers.

**Key Business Insight:**
The analysis revealed that **"Champions"** make up only **12%** of the customer base but contribute **45%** of Total Revenue. Conversely, the **"Hibernating"** segment represents huge potential revenue leakage, requiring an immediate re-engagement campaign.

---

### 📊 Dashboard Strategy

![Strategy Dashboard](Screenshots/dashboard_treemap.png)
*(Note: Rename your screenshot to match this)*

---

### ❓ Business Problem
The Marketing Director needed to move away from mass-email blasts to targeted campaigns. The goal was to answer:
1.  **Who are our most valuable customers?** (to reward them).
2.  **Who are we losing?** (to reactivate them).
3.  **What products drive loyalty?** (to recommend the right items).

### 🛠️ Tech Stack & Methodology
* **Python (Pandas):** * Performed ETL on 500,000+ transaction rows.
    * Calculated **RFM Metrics** relative to a dynamic snapshot date.
    * Implemented **Quintile Scoring (1-5)** using `pd.qcut` to mathematically rank customers.
    * Mapped scores to 10 distinct segments (e.g., "Loyalists", "Promising") using Regex.
* **Power BI:** * Built a **Star Schema** linking Customer Profiles (Dimensions) to Transactions (Facts).
    * Used **DAX** to generate Dynamic Smart Narratives (Automated text insights).
    * Implemented **Drill-Through** logic to link Segments to SKU-level product preferences.

---

### 📈 Visual Insights

**1. Revenue Distribution (Treemap):**
The visualization highlights that revenue is heavily skewed. The "Pareto Principle" is visible, where a small "Champion" block drives outsized value compared to the large "Hibernating" block.

**2. Dynamic Insight Generator:**
![Smart Narrative](Screenshots/smart_narrative.png)
*A custom DAX measure that automatically generates a strategic sentence based on the selected segment, calculating their exact Revenue Share vs. Population Share.*

**3. Product Affinity:**
By drilling into the "Champion" segment, we identified that **high-ticket decor items** (e.g., White Hanging Heart) are the primary drivers of loyalty, whereas "New Customers" tend to enter via low-cost consumables.

---

### 💡 Strategic Recommendations
1.  **For Champions:** Launch a "VIP Early Access" program for high-ticket decor items.
2.  **For At Risk:** Trigger automated discount emails for customers who haven't purchased in >90 days but have high historical spend.
3.  **For New Customers:** Focus on up-selling distinct "Gateway Products" identified in the matrix to migrate them to "Potential Loyalists."
