# Engineers Salary Prediction (ML Competition - Bitgrit)

## 1. Problem Statement

The goal of this project is to build a machine learning model that predicts the salary category of engineering jobs in the United States. The salary is classified into three categories:

- High
- Medium
- Low

The prediction is based on various job-related features such as job title, job description, required qualifications, industry, location, and experience level.

This project is part of the Bitgrit Machine Learning Competition, where participants aim to achieve the highest prediction accuracy on unseen data.

---

## 2. Dataset Description

The dataset used in this project was provided as part of the competition in the file:

**engineers_salary_prediction.zip**

It contains the following files:

- `train.csv` → Used for training the model  
- `test.csv` → Used for generating predictions  
- `solution_format.csv` → Submission format  

### Dataset Details

- Training data shape: **(1280, 317)**  
- Test data shape: **(854, 316)** :contentReference[oaicite:0]{index=0}  

### Features Description

- `obs`: Unique observation ID  
- `job_title`: Anonymized job titles  
- `job_posted_date`: Date of job posting  
- `salary_category`: Target variable (High, Medium, Low)  
- `job_state`: Location of the job  
- `feature_1` to `feature_12`: Structured job-related features  
- `job_desc_1` to `job_desc_300`: Vectorized job description features  

The dataset contains both categorical and numerical features along with high-dimensional text embeddings.

---

## 3. Data Preprocessing

The following preprocessing steps were applied:

- Handling missing values:
  - `feature_10` filled with median and scaled
  - `job_state` filled with mode
  - `job_posted_date` filled and converted to datetime

- Feature Engineering:
  - Extracted `job_posted_month` and `job_posted_year`
  - Grouped rare categories in `feature_1`

- Encoding:
  - Label Encoding applied to categorical variables
  - Combined train + test encoding to handle unseen categories :contentReference[oaicite:1]{index=1}  

- Feature Scaling:
  - StandardScaler used for Logistic Regression

- Train-Test Split:
  - 80% training, 20% validation

---

## 4. Evaluation Metrics

The model performance was evaluated using the following metrics:

### Accuracy
Measures overall correctness of the model predictions.

### Precision
Indicates how many predicted positive values are actually correct.

### Recall
Measures how many actual positives are correctly identified.

### F1-Score
Harmonic mean of Precision and Recall, useful for imbalanced datasets.

From the classification reports, models were evaluated on all these metrics for each class (High, Medium, Low). :contentReference[oaicite:2]{index=2}  

---

## 5. Models Used

### 1. Logistic Regression
A linear model used for classification. It works by estimating probabilities using a logistic function. It is simple, fast, and works well for linearly separable data.

### 2. Decision Tree
A tree-based model that splits the data based on feature conditions. It is easy to interpret but can overfit the data.

### 3. Random Forest
An ensemble of multiple decision trees. It reduces overfitting and improves generalization by averaging multiple trees.

### 4. XGBoost
A gradient boosting algorithm that builds trees sequentially to minimize errors. It is highly efficient and performs well on structured datasets.

### 5. CatBoost
A boosting algorithm designed to handle categorical features efficiently. It reduces the need for heavy preprocessing and provides strong performance.

### 6. LightGBM
A fast gradient boosting framework that uses histogram-based learning. It is optimized for speed and handles large datasets effectively.

---

## 6. Model Performance Comparison

| Model               | Accuracy |
|--------------------|----------|
| XGBoost            | 0.76     |
| LightGBM           | 0.75     |
| CatBoost           | 0.75     |
| Random Forest      | 0.66     |
| Decision Tree      | 0.66     |
| Logistic Regression| 0.63     |

The comparison clearly shows that boosting models outperform traditional models. :contentReference[oaicite:3]{index=3}  

---

## 7. Best Model

The best performing model based on validation accuracy:

**XGBoost → Accuracy: 0.76**

However, CatBoost was also used for final submission due to its stability and strong performance on categorical data.

---

## 8. Final Submission

- Predictions generated on `test.csv`
- Submission file created in required format:

