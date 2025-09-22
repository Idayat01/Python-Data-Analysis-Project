## Python Data Analysis Project  

This project demonstrates how Python can be used for **data cleaning, analysis, and visualization**.  
Using libraries like **Pandas, Matplotlib, and Seaborn**, I explored raw sales data to generate insights and build visualizations.  

---

##  Project Overview  
- Cleaned and prepared raw data using **Pandas**.  
- Analyzed **revenue trends, sales by product.  
    

---

## Tools & Libraries  
- Python   
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## Dashboard / Visualization Preview  
![Python Analysis](python pyt1.png) 
![Python Analysis](python pyt2.png)
![Python Analysis](python pyt3.png)
![Python Analysis](python pyt4.png)
![Python Analysis](python pyt5.png)
  

---

##  Sample Code  

### 1. Load and Explore Data  
```python
import pandas as pd

# Load dataset
df = pd.read_csv("sales.csv")

# Quick overview
print(df.head())
print(df.info())
print(df.describe())

### 2. Revenue Trend Over Time
import matplotlib.pyplot as plt

df['OrderDate'] = pd.to_datetime(df['OrderDate'])
monthly_sales = df.groupby(df['OrderDate'].dt.to_period('M'))['TotalSale'].sum()

monthly_sales.plot(kind='line', figsize=(10,5), marker='o')
plt.title("Monthly Revenue Trend")
plt.xlabel("Month")
plt.ylabel("Revenue")
plt.show()


## 3. Top 5 Products by Sales
top_products = df.groupby('Product')['TotalSale'].sum().sort_values(ascending=False).head(5)
print(top_products)


## 4. Revenue Distribution
import seaborn as sns

sns.histplot(df['TotalSale'], bins=30, kde=True)
plt.title("Revenue Distribution")
plt.show()



# Key Insights

 Revenue grew steadily across the year, with peak sales in Q4.

 Top 5 products generated 60%+ of total revenue.

 Customer purchasing patterns showed higher frequency but lower spend in Q1 compared to later months.

 Distribution shows most transactions fall under mid-range sales values, with a few high-value outliers.



## Files in This Repo

python_analysis.ipynb → Jupyter Notebook with all analysis

Python_Project_Report.pdf → Detailed report

python-dashboard.png → Screenshot of visualizations


#RECOMMENDATIONS
This project is basically to demonstrate my Python data analysis skills 
using the Pandas and Matplotlib libraries. I worked with raw 
sales data and my task is to clean it, explore it, and extract useful 
business 
insights which i did justice to that, my python analysis skill is now sharpened and recommended. 

















