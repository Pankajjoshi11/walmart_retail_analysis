
# 🛍️ Walmart Retail Sales Analysis Project

A complete data-driven project that analyzes Walmart-style retail transactions, extracts actionable insights, and predicts customer satisfaction levels using machine learning. The project includes exploratory data analysis, feature engineering, data cleaning, class imbalance handling, and model building with a robust ML pipeline.

---

## 📁 Project Structure
```
.
├── dataset/
│   ├── Walmart.csv               # Raw original dataset
│   └── walmart_updated.csv       # Cleaned and preprocessed dataset after feature engineering & outlier removal
├── main.ipynb                    # Full EDA, visualization, and initial data preparation notebook
├── ml_model_pipeline.ipynb       # Machine learning pipeline, model training, evaluation, and tuning
├── requirements.txt              # List of Python package dependencies
├── .gitignore                    # Files/directories to be ignored by Git (e.g., checkpoints, __pycache__)
└── README.md                     # Project overview and documentation (this file)
```
---

## 🔍 Objective

To derive insights from historical sales data and build a predictive model for classifying customer satisfaction ratings (`Low`, `Medium`, `High`) based on transactional features like product category, city, quantity, payment method, and total purchase value.

---

## 📊 Exploratory Data Analysis (EDA)

- Cleaned and processed 14 original features
- Created meaningful derived features:
  - `total = unit_price × quantity`
  - `profit = total × profit_margin`
- Binned numeric `rating` into `rating_level` with 3 categories
- Analyzed trends:
  - Sales by hour, day, and city
  - Category-wise profit margins
  - Distribution of ratings and purchase behavior
- Detected and removed outliers using the IQR method

---

## 🤖 Machine Learning Pipeline

- Built a reusable pipeline with:
  - `ColumnTransformer` for encoding and transformation
  - `SMOTE` to handle class imbalance
  - `RandomForestClassifier` for classification
- Implemented `GridSearchCV` for hyperparameter tuning
- Addressed overfitting and model leakage by properly splitting and preprocessing the data

---

## 🧪 Model Performance

| Model              | Accuracy | Macro F1 Score |
|-------------------|----------|----------------|
| Random Forest      | ~98–99%  | ~0.97          |


- High precision, recall, and F1-scores across all classes
- Class imbalance effectively handled
- Classification reports and confusion matrices provided for each model

---

## 📈 Visual Insights

- Class distribution before and after SMOTE
- Feature correlation heatmap
- Sales distribution by city and category
- Hourly sales trends
- Scatter plots for profit vs. total
- Feature importance visualizations
- Confusion matrix for model validation

---

## 💡 Business Insights

- Sales peak during late morning and early afternoon hours
- Cities like **San Antonio**, **Irving**, and **Harlingen** contribute significantly to revenue
- Product categories such as *Health and Beauty* and *Electronic Accessories* are high performers
- Strong correlation found between city, category, and customer satisfaction

---

## 🧰 Tech Stack

| Component       | Tools & Libraries                           |
|----------------|----------------------------------------------|
| Programming    | Python                                       |
| Data Handling  | Pandas, NumPy                                |
| Visualization  | Seaborn, Matplotlib                          |
| Modeling       | Scikit-learn, imbalanced-learn (SMOTE) |
| Evaluation     | Classification Report, Confusion Matrix     |
| Optimization   | GridSearchCV                                 |

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/walmart-sales-analysis.git
```

2. Navigate to the project directory and install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Launch the notebook:

   ```bash
   jupyter notebook notebooks/Walmart_Sales_Analysis.ipynb
   ```

---

## 📦 Deliverables

* End-to-end ML pipeline with preprocessing, sampling, and classification
* Visual EDA and insights
* Feature importance and model interpretability
* Exportable model for further deployment
* Clean, modular notebook ready for presentation or review

---

⭐ *If you found this project helpful, feel free to star the repository and share!*
