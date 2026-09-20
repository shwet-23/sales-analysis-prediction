# 📊 Sales Analytics & Profitability Prediction

An end-to-end data analytics and machine learning project using the Sample Superstore dataset.

The project analyzes sales, profitability, discounts, products, regions and customer segments, and builds machine learning models to predict whether a transaction is likely to generate a profit or loss.

---

## 🎯 Project Objective

The main objectives of this project are:

- Analyze overall business performance
- Identify profitable and loss-making categories
- Understand the relationship between discount and profit
- Analyze regional and customer-segment performance
- Identify important business patterns
- Build a machine learning classification model
- Predict potentially loss-making transactions

---

## 📂 Dataset

The project uses the Sample Superstore dataset.

Dataset size:

- 9,994 transaction records
- 21 original columns

Important columns include:

- Order Date
- Ship Date
- Ship Mode
- Customer Segment
- Category
- Sub-Category
- Region
- Sales
- Quantity
- Discount
- Profit

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Joblib

---

## 🔎 Exploratory Data Analysis

The analysis includes:

- Data cleaning
- Missing-value analysis
- Duplicate analysis
- Business KPI analysis
- Category analysis
- Sub-category analysis
- Discount analysis
- Time-series analysis
- Regional analysis
- State analysis
- City analysis
- Customer segment analysis

---

## 📈 Key Business Findings

### Overall Performance

- Total Sales: approximately $2.30M
- Total Profit: approximately $286.40K
- Overall Profit Margin: approximately 12.46%
- Total Quantity Sold: 37,873 units

### Category Performance

Technology generated approximately 17.40% profit margin.

Office Supplies generated approximately 17.04% profit margin.

Furniture generated approximately 2.49% profit margin despite generating substantial sales.

### Sub-Category

Tables generated significant sales but resulted in an overall loss.

### Discount

Discount showed a negative correlation with Profit of approximately -0.2195.

Higher discount levels were frequently associated with lower profitability in the dataset.

Correlation does not establish causation.

### Regional Performance

The West region generated the highest total sales and profit.

Central generated more sales than South but had a lower profit margin.

### Customer Segment

Consumer generated the highest sales and order volume.

Home Office generated the highest profit margin at approximately 14.03%.

---

# 🤖 Machine Learning

## Problem Definition

The machine learning task is binary classification.

The model predicts whether a transaction is likely to generate a loss.

Target:

- `0` → Profit
- `1` → Loss

### Class Distribution

- Profit: 81.28%
- Loss: 18.72%

Because the classes are imbalanced, precision, recall and F1-score are evaluated in addition to accuracy.

---

## 🔧 Machine Learning Workflow

The machine learning pipeline includes:

1. Feature selection
2. Train-test split
3. One-hot encoding of categorical features
4. Standardization of numerical features
5. Logistic Regression
6. Random Forest
7. Model evaluation
8. Feature importance analysis

---

## 📊 Model Performance

### Logistic Regression

- Accuracy: 94.25%
- Loss Precision: 87.98%
- Loss Recall: 80.21%
- Loss F1-Score: 83.92%

### Random Forest

- Accuracy: 94.25%
- Loss Precision: 91.37%
- Loss Recall: 76.47%
- Loss F1-Score: 83.26%

The two models show a precision-recall trade-off for the Loss class.

Random Forest achieved higher Loss precision, while Logistic Regression achieved higher Loss recall and slightly higher Loss F1-score.

---

## 🔍 Feature Importance

The Random Forest model identified Discount as the most important predictive feature.

Top feature:

- Discount: approximately 47.4% feature importance
- Sales: approximately 7.4%

Other influential features included product sub-category, order timing, quantity and region.

Feature importance represents predictive contribution within the model and should not be interpreted as causal evidence.

---

## 💡 Business Recommendations

Based on the analysis:

1. Review high-discount transactions.
2. Investigate loss-making product sub-categories.
3. Analyze Furniture profitability.
4. Investigate high-sales but low-profit regions and states.
5. Monitor profit margin alongside revenue.
6. Evaluate discount strategies using product-level profitability.
7. Use predictive models to identify potentially loss-making transactions.

---

## 📁 Project Structure

```text
sales-analysis-prediction/
│
├── Sales_Analytics_Profitability_Prediction.ipynb
├── Sample_Superstore.csv
├── preprocessor.pkl
├── random_forest_model.pkl
├── README.md
└── .gitignore