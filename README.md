# Customer Segmentation & Risk Analysis

## 📌 Overview
This project focuses on **customer segmentation and credit risk analysis** using a financial dataset.  
The goal is to identify distinct customer groups based on financial behavior and provide **data-driven business recommendations** for lending, risk management, and customer engagement.

---

## 📂 Dataset
The dataset contains ~15,000 customer records with features such as:

- Demographics: Age, Gender, Marital Status, Education
- Financials: Income, Assets Value, Loan Amount
- Credit Metrics: Credit Score, Previous Defaults, Debt-to-Income Ratio
- Behavioral Data: Payment History, Employment Status
- Target: Risk Rating

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Removed missing values and inconsistencies
- Converted data types for modeling
- Handled skewness and distributions
- Feature engineering (rounding, type conversion)

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis (Income, Loan Amount, Assets)
- Segment-based analysis using custom logic (RFS framework)
- Visualizations:
  - Customer distribution across segments
  - Income contribution by segment
  - Loan distribution by segment
  - Default patterns

---

## 🧠 Segmentation Logic (RFS Framework)

Customers are segmented based on:

- **R (Risk):** Credit score, defaults, risk rating  
- **F (Financial Strength):** Income, assets, loan size  
- **S (Stability):** Job tenure, payment history  

### Segments Identified:
- High Net-Worth Prime
- Premium Watchlist
- Volatile Affluent
- Asset-Heavy Prospect
- Growth Stable
- Emerging Profile
- Consistent Moderate
- Low Engagement

---

## 📊 Clustering (K-Means)

- Features scaled using **StandardScaler**
- Optimal clusters determined using:
  - Elbow Method (Inertia)
  - Silhouette Score
- Final model: **K = 5 clusters**

### Cluster Insights:
| Cluster | Description |
|--------|------------|
| Prime | High income, low risk |
| Watchlist | Stable but requires monitoring |
| Asset Builder | Growth potential |
| Volatile Affluent | High value but unstable |
| Low Engagement | Low value, high risk |

---

## 🤖 Machine Learning

### Models Used:
- Random Forest Classifier
- Logistic Regression

### Model Selection:
- GridSearchCV for hyperparameter tuning
- Best Model: **Random Forest (~60% accuracy)**

---

## 📈 Key Insights

- **Low Engagement segment dominates but has highest defaults**
- **High Net-Worth & Growth Stable are most profitable and safest**
- **Mid-tier segments show strong growth potential**
- **Volatile segments require monitoring despite high value**

---

## 💡 Business Recommendations

- Reduce exposure to high-risk (Low Engagement) customers  
- Focus on premium services for high-value clients  
- Nurture mid-tier customers into high-value segments  
- Implement monitoring systems for volatile customers  
- Use segmentation + clustering for decision automation  

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/RookieCoder12/DevArena-Week-11.git

# Navigate to project folder
cd DevArena-Week-11

### Installation
Install the required dependencies:
```zsh
pip install -r requirements.txt
```

### Running the Project

#### Running the Python Notebook
1. Run jupyter notebook:
```zsh
jupyter notebook
```
2. Open ```churn_prediction_pipeline.ipynb```.