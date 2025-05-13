
# 🛒 Customer Segmentation 

## 📌 Business Context

Instacart, a U.S.-based online grocery delivery platform, processes millions of orders across thousands of retailers. A core business challenge is increasing user retention and order volume through personalized recommendations and targeted marketing. With more than 3 million anonymized grocery orders from 200,000+ users, this project explores how data science can drive these outcomes by understanding customer behavior and predicting future purchases.



## 🎯 Project Objectives

- 🔍 Understand purchase behavior through exploratory data analysis (EDA).
- 🧮 Segment customers for targeted marketing using clustering techniques.
- 🤖 Predict product reorders using supervised ML models on user and product-level features.
- 🧠 Interpret model decisions using explainability tools like SHAP.



## 🗂️ Project Structure


```  
├── Clustering/                                  
│ ├── Data Description and EDA.ipynb          # Exploratory Data Analysis (EDA)  
│ ├── Customer Segmentation.ipynb             # Customer segmentation based on product aisles  
├── Prediction/                           
│ ├── Data Preparation.ipynb                    # Dataset merging and transformation
│ ├── Feature Extraction.ipynb                  # Engineering 30+ features from user/product behavior
│ ├── ANN Model.ipynb                           # Neural network for reorder prediction
│ ├── XGBoost Model.ipynb                       # XGBoost with SHAP-based model interpretation
```

## 🧠 Methodology

### 1. Exploratory Data Analysis
- Combined 6 raw datasets (~3M orders) into a unified memory-efficient structure.
- Identified top aisles, reorder rates, cart sizes, and weekly order patterns.

**Key Insights:**
- 60%+ of products are reorders.
- Organic and fresh produce are top repeat buys.
- Most orders occur on weekends, especially Saturday afternoons.

### 2. Customer Segmentation
- Created a customer–aisle matrix and reduced dimensionality using PCA.
- Applied KMeans clustering to uncover 5 distinct customer personas.
- Enabled targeted campaigns for each segment.

### 3. Feature Engineering
Extracted 30+ features across:

- **Product-level**: reorder rates, popularity, organic flag  
- **User-level**: order frequency, diversity, reorder percentage  
- **User-product interaction**: historical behavior  
- **Aisle/department**: volume, recency, encoded categories  

### 4. Predictive Modeling
- Trained XGBoost and ANN models to predict product reorder likelihood.
- Applied class weighting to handle class imbalance.
- Evaluated models using ROC-AUC and SHAP for explainability.


## 📊 Results & Insights

| Model        | ROC-AUC | Key Insights |
|--------------|---------|--------------|
| XGBoost      | ~0.86   | Top features: User reorder ratio, product popularity |
| Neural Net   | ~0.85   | Comparable performance with nonlinear feature handling |

✅ SHAP values highlighted important behavioral signals and made predictions explainable.

## 🚀 Business Impact

- 📦 Improved reorder prediction enables smarter cart suggestions.
- 🛍️ Association rules support bundle recommendations and shelf optimization.
- 👥 Customer segmentation powers personalized outreach and lifecycle marketing.

## 📥 How to Use

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/instacart-order-prediction.git
cd instacart-order-prediction
```

2. **Download the dataset from Kaggle and place the CSV files in the data/ directory.**

```bash
  Run notebooks in order:

- Clustering/Data Description and EDA.ipynb

- Clustering/Customers Segmentation.ipynb

- Prediction/Data Preparation.ipynb

- Prediction/Feature Extraction.ipynb

- Prediction/XGBoost Model.ipynb or ANN Model.ipynb
```
