# Diwali Sales Analysis using Python

## Project Overview
This project analyzes Diwali sales data to uncover customer purchasing behavior, sales trends, and business insights using Python.

![image](https://github.com/adarshvatspandey/Diwali_Sales_Analysis_Python/blob/dc5118102f1fed8a3feb287459b29ca9c7d28879/Diwali%20pic.png)

## Objectives
- Analyze customer demographics.
- Identify top-performing states.
- Understand purchasing behavior.
- Discover high-revenue product categories.
- Generate actionable business insights.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset Information
The dataset contains:
- User ID
- Customer Name
- Gender
- Age Group
- Marital Status
- State
- Occupation
- Product Category
- Orders
- Amount

## Data Cleaning
- Removed null values
- Dropped unnecessary columns
- Checked data types
- Handled missing records

## Exploratory Data Analysis

## 1. Which gender contributes the highest sales revenue?

```python
df.groupby('Gender')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Female customers contribute the highest sales revenue.

---

## 2. Which age group spends the most?

```python
df.groupby('Age Group')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Age Group 26–35 contributes the highest sales revenue.

---

## 3. Which state generates the highest sales revenue?

```python
df.groupby('State')['Amount'].sum().sort_values(ascending=False).head(10)
```

**Answer:** Uttar Pradesh generates the highest sales revenue.

---

## 4. Which zone contributes the highest revenue?

```python
df.groupby('Zone')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Central Zone contributes the highest revenue.

---

## 5. Which occupation generates the highest revenue?

```python
df.groupby('Occupation')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** IT Sector professionals generate the highest revenue.

---

## 6. Which product category generates the highest revenue?

```python
df.groupby('Product_Category')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Food category generates the highest revenue.

---

## 7. Which product category receives the highest number of orders?

```python
df.groupby('Product_Category')['Orders'].sum().sort_values(ascending=False)
```

**Answer:** Clothing & Apparel receives the highest number of orders.

---

## 8. What is the average spending by gender?

```python
df.groupby('Gender')['Amount'].mean().sort_values(ascending=False)
```

**Answer:** Female customers have a higher average spending amount.

---

## 9. Which marital status group spends more?

```python
df.groupby('Marital_Status')['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Married customers spend more than unmarried customers.

---

## 10. Which state has the highest number of orders?

```python
df.groupby('State')['Orders'].sum().sort_values(ascending=False)
```

**Answer:** Uttar Pradesh records the highest number of orders.

---

## 11. Which occupation places the most orders?

```python
df.groupby('Occupation')['Orders'].sum().sort_values(ascending=False)
```

**Answer:** IT professionals place the highest number of orders.

---

## 12. Which age group places the most orders?

```python
df.groupby('Age Group')['Orders'].sum().sort_values(ascending=False)
```

**Answer:** Age Group 26–35 places the highest number of orders.

---

## 13. Which state has the highest average order value?

```python
df.groupby('State')['Amount'].mean().sort_values(ascending=False)
```

**Answer:** Karnataka has the highest average order value.

---

## 14. Which gender places more orders?

```python
df.groupby('Gender')['Orders'].sum().sort_values(ascending=False)
```

**Answer:** Female customers place more orders.

---

## 15. Which occupation-product category combination generates the highest revenue?

```python
df.groupby(['Occupation','Product_Category'])['Amount'].sum().sort_values(ascending=False).head(10)
```

**Answer:** IT Professionals purchasing Food products generate the highest revenue.

---

## 16. Who are the top 10 customers by spending?

```python
df.groupby('Cust_name')['Amount'].sum().sort_values(ascending=False).head(10)
```

**Answer:** The listed customers are the top spenders in the dataset.

---

## 17. Which age group prefers each product category?

```python
pd.crosstab(df['Age Group'], df['Product_Category'])
```

**Answer:** Age Group 26–35 shows the highest purchasing activity across most categories.

---

## 18. What percentage of sales comes from the top 5 states?

```python
top5 = df.groupby('State')['Amount'].sum().sort_values(ascending=False).head(5)
(top5.sum()/df['Amount'].sum())*100
```

**Answer:** Top 5 states contribute the majority of total sales revenue.

---

## 19. Which zone has the highest average spending?

```python
df.groupby('Zone')['Amount'].mean().sort_values(ascending=False)
```

**Answer:** Central Zone has the highest average spending.

---

## 20. Which customer segment is most valuable (Gender + Marital Status)?

```python
df.groupby(['Gender','Marital_Status'])['Amount'].sum().sort_values(ascending=False)
```

**Answer:** Married Female customers generate the highest revenue.

---

# Key Business Insights

* Female customers are the primary contributors to revenue.
* Married women aged 26–35 are the most valuable customer segment.
* Uttar Pradesh, Maharashtra, and Karnataka are top-performing states.
* Food, Clothing, and Electronics categories drive the majority of sales.
* IT, Healthcare, and Aviation professionals have high purchasing power.
* The Central Zone contributes significantly to overall revenue.
* Customer spending is concentrated among a few high-performing states.
* Festive shopping behavior is strongest among young working professionals.

## Conclusion
The analysis reveals valuable customer segments and product categories that businesses can target to maximize sales during festive seasons.
