# DigiCow Farmer Training Adoption Challenge

# 🧠 Problem Statement

Access to agricultural training alone does not guarantee improved farm productivity. The real challenge is identifying which farmers actually adopt improved practices after training.

DigiCow Africa provides digital tools and targeted training to smallholder farmers. However, adoption rates remain low and uneven. Predicting adoption early would allow DigiCow to prioritize follow-ups, allocate resources efficiently, and design more effective extension strategies.

## 🎯 Objective

Build a machine learning model to predict the probability that a farmer will adopt improved practices within:

- 7 days  
- 90 days  
- 120 days  

of their first training session.

Predictions must be made using only the information available at the time of training.

## 📊 Problem Type

This is a **multi-target binary classification problem**, evaluated using:

- AUC (ranking performance)
- LogLoss (probability accuracy)

Due to extreme class imbalance, accuracy is not a reliable metric.
