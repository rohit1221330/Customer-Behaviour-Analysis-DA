# 🛒 Customer Lifetime Value & Shopping Behavior Analysis

## 📌 Executive Summary
This project analyzes the shopping behavior of 3,900 customers (generating ~$233,000 in total revenue) to uncover actionable business strategies. The primary objective is to optimize Customer Lifetime Value (CLV), identify inefficiencies in the current promotional strategy, and provide data-driven recommendations for inventory and marketing reallocation.

Instead of just reporting descriptive statistics, this analysis acts as a strategic consulting document, bridging the gap between raw database metrics and executive decision-making.

## 🛠️ Tech Stack & Architecture
* **Data Engineering & Cleaning:** Python (Pandas, SQLAlchemy)
* **Relational Database:** MySQL (CTEs, Window Functions, Aggregations)
* **Data Visualization & Reporting:** Power BI, Gamma AI
* **Pipeline:** Raw CSV ➡️ Pandas (ETL & Imputation) ➡️ MySQL (Querying) ➡️ Power BI (Dashboarding)

## 📊 Key Business Insights (The "So What?")
1. **The Demographic Skew:** The customer base is heavily dominated by men (68%), who generate **$157,890** compared to female customers ($75,191). The most profitable age bracket is the **Young Adult** segment ($62,143).
2. **The Subscription Bottleneck:** A massive **73% of the user base (2,847 users) is unsubscribed**, leaving significant recurring revenue on the table. Crucially, among repeat buyers (>5 past purchases), **2,518 users** are still not subscribed.
3. **Marketing Redundancy:** Discovered a **100% overlap** between users applying discounts and promo codes, indicating a major inefficiency in ad-tracking and promotional budget allocation.
4. **Logistics Impact:** Customers opting for 'Express' shipping have a higher Average Order Value ($60.48) compared to 'Standard' shipping ($58.46).

## 🚀 Strategic Recommendations
* **Consolidate Promotions:** Immediately merge promo code and discount campaigns to stop wasting marketing budget on duplicate metrics.
* **Launch Subscription Upsells:** Target the 2,518 frequent but unsubscribed buyers with a 30-day premium trial to lock in recurring CLV. 
* **Optimize Inventory:** Reallocate budget towards top-moving categories (Jewelry, Blouses, Jackets) and skew ad spend aggressively towards the Young Adult Male demographic.

## 📂 Repository Structure
* `Customer_Shopping_Behaviour_Analysis.ipynb`: Python notebook detailing the ETL process, missing value imputation (median-based), and feature engineering (`age_group`, `purchase_frequency_days`).
* `Customer_Behaviour_Sql_Queries.sql`: Advanced SQL queries executing business logic, segmentation, and revenue extraction.
* `Customer_Behaviour_Dashboard.pbix`: Power BI file containing the interactive business dashboard.
* `Customer_Shopping_Behavior_Analysis.pdf`: The final executive presentation summarizing strategic actions.

## ⚙️ How to Run
1. Clone the repository.
2. Run the Jupyter Notebook to clean the dataset and push it to your local MySQL instance using SQLAlchemy.
3. Execute the SQL scripts in your preferred RDBMS to extract business metrics.
4. Open the `.pbix` file to interact with the visualizations.
