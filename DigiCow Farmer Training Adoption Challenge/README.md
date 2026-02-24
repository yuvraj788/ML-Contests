# DigiCow Farmer Training Adoption Challenge

### Problem Statement
The goal is to predict whether a farmer will adopt improved agricultural practices within 7, 90, or 120 days after their first training session.
This is a multi-target binary classification problem using only information available at training time.
Models are evaluated using AUC for ranking performance and LogLoss for probability accuracy.



### Dataset
The data is a tabular dataset of farmer information, with nearly 14,000 rows and 17 features (Train.csv), including farmer's age group, gender, geographic location and training information.


### Evaluation
This challenge uses multi-metric evaluation. There are two error metrics: Log Loss and ROC-AUC.



### ROC AUC and Log Loss
ROC AUC and Log Loss are two important metrics used to evaluate the performance of binary classification models. ROC AUC measures the area under the ROC curve, indicating the model's ability to discriminate between positive and negative classes across all possible thresholds. A higher AUC value suggests better model performance, while a value close to 0.5 indicates random guessing. Log Loss, on the other hand, measures the quality of predicted probabilities, with a value of 0 indicating perfect predictions. Log Loss is particularly useful for models that produce probabilities between 0 and 1, such as logistic regression and neural networks. Both metrics are essential for understanding model performance and making informed decisions about model selection and optimization.



### Implemented the following algorithms
**Random Forest** uses bagging (Bootstrap Aggregating), building multiple decision trees independently on random subsets of data and features, then aggregating results (majority vote or average). This reduces variance and improves generalization.

**XGBoost** uses gradient boosting, building trees sequentially, where each new tree corrects errors from the previous ones. It minimizes a loss function using gradient descent, making it more focused on reducing bias and variance simultaneously.

## Model Performance Results

###  adopted_within_07_days

XGBoost:
- AUC: 0.9198
- LogLoss: 0.0413

Random Forest:
- AUC: 0.9245
- LogLoss: 0.0424


###  adopted_within_90_days

XGBoost:
- AUC: 0.9425
- LogLoss: 0.0537

Random Forest:
- AUC: 0.9109
- LogLoss: 0.0578


###  adopted_within_120_days

XGBoost:
- AUC: 0.8921
- LogLoss: 0.0842

Random Forest:
- AUC: 0.8715
- LogLoss: 0.0796


## Final Model Selection

**XGBoost** was selected for final submission because it achieved:

- Higher AUC in 2 out of 3 targets
- Strong ranking performance
- More consistent overall results
