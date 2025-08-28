# amazon-sales-data-sql-analysis
SQL analysis of Amazon sales data to identify revenue trends, top categories, and branch-wise performance.

# Amazon Sales Data Analysis

## 🎯 Objective
The major aim of this project is to gain insight into the sales data of Amazon to understand the different factors that affect sales across different branches.

## 🛠 Tools & Technologies
- SQL (MySQL)
- Excel (for initial data handling)

## 📊 Key Analyses & Insights
### 1. Product Analysis
- **Food & Beverages** → highest revenue & average rating (7.1).  
- **Home & Lifestyle** → lowest rating (6.8).  
- **Electronics accessories** → top in sales volume.  

### 2. Sales Analysis
- **January** had the highest revenue (~116K).  
- Sales in the **first week of every month** were lower compared to later weeks.  
- **Naypyitaw branch** recorded the highest revenue.  
- **Cash** was the top payment method (34.7% of revenue).  

### 3. Customer Analysis
- Female customers generated **higher revenue** than males.  
- **Members** contributed the majority of revenue (~164K).  
- Predominant customer gender = **Female** (501 out of ~1,000).  

### 4. Advanced Insights (Feature Engineering)
- **Evening** was the peak time for transactions & ratings.  
- **Friday & Monday** had the highest customer ratings across branches.  
- Branch-level analysis showed:  
  - Branch A → best ratings in Afternoon.  
  - Branch B → best ratings in Morning.  
  - Branch C → best ratings in Evening.  

## 📜 Example Queries
```sql
-- Highest revenue by product line
SELECT Product_Line, SUM(Total) AS Revenue
FROM amazon
GROUP BY Product_Line
ORDER BY Revenue DESC
LIMIT 1;

