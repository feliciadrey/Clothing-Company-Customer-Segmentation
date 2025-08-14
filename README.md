# Clothing Company Customer Segmentation
Machine learning clustering project to segment customers of a fashion retail company based on purchasing behavior and demographic attributes. This project focuses on a complete end-to-end pipeline from data preprocessing and exploratory data analysis to clustering model training, optimal cluster selection, and customer segment profiling to support targeted marketing strategies.

---

## Overview
This project was developed for the **Machine Learning** course (4th semester) as part of the individual final exam. The objective is to group customers into distinct segments using unsupervised learning, enabling the business to create personalized marketing campaigns and improve customer engagement.

The workflow includes:
- Exploratory Data Analysis (EDA) to identify patterns and relationships in purchasing behavior
- Data cleaning and preprocessing (handling missing values, fixing label inconsistencies, encoding categorical variables, scaling numerical features)
- Feature engineering to derive meaningful metrics such as estimated total spend
- Dimensionality reduction using PCA for visualization
- Clustering using K-Means with optimal cluster selection
- Profiling clusters to provide actionable business recommendations

**Deliverables include:**
- **Python notebook** – complete pipeline for preprocessing, clustering, and profiling
- **Visualizations** – EDA plots, PCA scatter plots, and silhouette analysis
---

## 📊 Data

The dataset contains anonymized fashion retail customer records, including demographics, purchasing behavior, and product preferences.

**Key Information**
- **Entries:** 3,900+ rows  
- **Features:** Mix of numerical and categorical attributes after preprocessing  
- **Target Variable:** *None* (unsupervised task)  

### Data Dictionary
| Variable | Description |
|----------|-------------|
| **Customer’s ID** | Unique identifier for each customer |
| **Birth Date** | Date of birth of the customer |
| **Gender** | Gender of the customer |
| **Item Purchased** | Type of item purchased |
| **Category** | Category of the purchased item |
| **Purchase Amount (USD)** | Amount spent in USD |
| **Location** | Customer's location |
| **Size** | Size of the purchased item |
| **Color** | Color of the purchased item |
| **Season** | Season when the purchase occurred |
| **Review Rating** | Customer’s rating for the purchase |
| **Subscription Status** | Whether the customer has an active subscription |
| **Payment Method** | Payment method used for the purchase |
| **Shipping Type** | Shipping method used |
| **Discount Applied** | Indicates if a discount was applied (Yes/No) |
| **Promo Code Used** | Indicates if a promo code was used (Yes/No) |
| **Previous Purchases** | Month of the last purchase |
| **Preferred Payment Method** | Customer's preferred payment method |
| **Frequency of Purchases** | Average purchase frequency in the last year |

---

## Workflow
- **Data Cleaning**
  - Standardization of categorical labels (e.g., fixing inconsistent gender and frequency values)
  - Removal of irrelevant identifier columns
- **Feature Engineering**
  - Age calculation from `Birth Date`
  - Estimation of annual total spending adjusted for purchase frequency
- **Encoding**
  - Label Encoding for binary/ordinal variables
  - One-Hot Encoding for nominal multi-category variables
  - Ordinal Encoding for ordered size attributes
- **Dimensionality Reduction**
  - PCA to project high-dimensional data into 2D for cluster visualization
- **Modeling**
  - K-Means clustering with optimal `k` chosen using:
    - Elbow Method
    - Silhouette Score
  - Silhouette plots to assess cluster cohesion and separation
- **Cluster Profiling**
  - Analysis of demographic and spending patterns per cluster
  - Recommendations for targeted marketing per customer segment

---

## 🛠️ Tools & Technologies
- **Python** – data preprocessing, clustering, and visualization
- **Pandas / NumPy** – data manipulation
- **Matplotlib / Seaborn** – data visualization
- **Scikit-learn** – preprocessing, PCA, K-Means, evaluation metrics

---
## 🔍 Key Insights
Based on cluster traits and visualization, distinct customer behaviors and preferences were identified:

1. **Cluster 1** (previously Cluster 0)  
   - Middle-aged (avg. 49 years), mostly male  
   - Highest spending (75.88 USD) and highest satisfaction (4.17 rating)  
   - Moderate subscription and discount usage  
   **Suggestion:** Introduce a premium loyalty program with benefits such as early access to exclusive products.

2. **Cluster 2**  
   - Youngest group (avg. 34 years), mostly male but least male-dominated among clusters  
   - Moderate spending (59.43 USD) and average satisfaction  
   - Lowest subscription and discount usage  
   **Suggestion:** Use social media-driven marketing campaigns with trendy product promotions to appeal to younger audiences.

3. **Cluster 3**  
   - Oldest group (avg. 53 years)  
   - Lowest spending (44.84 USD) and lowest satisfaction  
   - Highest subscription and discount usage  
   **Suggestion:** Offer bundle deals or senior citizen discounts to increase engagement and spending.
