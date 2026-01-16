# Customer Satisfaction Analysis – Olist E-commerce Dataset

This project analyzes the Brazilian Olist e-commerce dataset with the goal of understanding which factors are associated with customer satisfaction. The focus is on delivery performance, order characteristics, payment methods, and customer reviews, using exploratory data analysis and data visualization.

---

## Objective

Identify the main factors associated with customer satisfaction in an e-commerce context, with particular attention to:
- delivery times and delays
- order complexity (number of items and sellers)
- payment methods
- customer reviews and sentiment

---

## Dataset

- **Source**: Brazilian E-Commerce Public Dataset by Olist (Kaggle)
- **Content**:
  - orders
  - customers
  - sellers
  - products
  - payments
  - reviews
  - delivery timestamps

The dataset represents real e-commerce transactions in Brazil and includes both operational and customer experience information.

---

## Methodology

1. **Exploratory Data Analysis (EDA)**  
   - Initial exploration of each table using Python
   - Analysis of distributions, missing values, and data quality

2. **Data Modeling**  
   - Creation of a relational model in Power BI
   - Handling many-to-many relationships through an order-level fact table
   - Feature engineering (delivery time, delays, order complexity, payment type)

3. **Analysis & Visualization**

The analysis focuses on understanding how operational processes and customer experience relate to customer satisfaction.

Key analyses include:

- **Delivery process analysis along the acquisition funnel**  
  The end-to-end order timeline was decomposed into its main steps (purchase, payment approval, shipping, delivery) to identify where delays most frequently occur.  
  This analysis revealed that the **largest source of delay is the time between order creation and payment approval**, rather than the shipping or delivery phase itself.

- **Delivery performance analysis**  
  Estimated and actual delivery times were compared to distinguish absolute delivery duration from relative delays.  
  Orders were segmented by complexity (number of sellers and items) to explore how logistical structure affects delivery performance.

- **Exploratory visualizations**  
  Python was used to create advanced visualizations (violin plots, boxplots, scatter plots) that are not natively supported in Power BI, enabling a more accurate exploration of distributions and outliers.


5. **Interpretation & Storytelling**  

- **Revisiting initial hypotheses**  
  While multi-seller orders were initially expected to generate more delivery delays, the analysis showed that they are associated with more conservative delivery estimates.  
  This explains why relative delays are not higher, highlighting the importance of distinguishing between estimated and actual delivery times.

- **Quantitative analysis of customer reviews**  
  Customer comments were analyzed using Python and the `spacytextblob` library to extract sentiment and create word clouds for positive and negative reviews.  
  This analysis confirmed the **central role of delivery time** in shaping customer satisfaction.

- **Product expectation alignment**  
  Beyond delivery performance, review analysis revealed another important factor: customer satisfaction is strongly influenced by how well the received product matches the **photos and descriptions published by the seller**.  
  This highlights the relevance of expectation management in addition to logistical efficiency.

Overall, the storytelling emphasizes how operational delays, delivery expectations, and perceived product quality jointly contribute to the customer experience.


---

## Key Insights

- **Delivery time is strongly associated with customer satisfaction**: longer delivery times and delays tend to correspond to lower review scores.
- **Multi-seller orders are not necessarily slower**, but they receive more conservative delivery estimates, which explains why they do not show higher relative delays.
- **Order complexity** (number of items and sellers) shows limited direct correlation with ratings, except for cases involving multiple sellers.
- **Extreme delivery delays (>30 days)** represent a small fraction of orders but are strongly associated with negative customer sentiment.
- Distinguishing between **estimated delivery time, actual delivery time, and relative delay** is essential to correctly interpret customer experience.

---

## Tools & Technologies

- **Python**
  - pandas
  - matplotlib
  - seaborn
- **Power BI**
  - Data modeling
  - DAX
  - Interactive dashboards
- **Techniques**
  - Exploratory Data Analysis (EDA)
  - Feature engineering
  - Data visualization
  - Analytical storytelling

---

## Limitations

- The analysis is conducted at **order level**, which limits seller-level attribution in multi-seller orders.
- Results identify **associations**, not causal relationships.
- Some categories (e.g. orders with many sellers) have limited sample sizes.

