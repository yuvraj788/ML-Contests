# DigiCow Farmer Training Adoption Challenge

### 🧠 Problem Statement

## 🚜 Can You Predict Which Farmers Will Turn Training Into Action?

Access to high-quality agricultural training is only the first step toward improving farm productivity. The real challenge lies in understanding which farmers actually adopt improved agricultural practices after receiving training — and why.

DigiCow Africa supports smallholder farmers through digital tools, extension services, and targeted training programs. However, like many real-world development interventions, adoption rates remain low and uneven across farmers.

Being able to **predict adoption early** would allow DigiCow and its partners to:

- Prioritize follow-up interventions
- Allocate extension resources more efficiently
- Provide personalized support to high-risk farmers
- Design stronger and more effective training strategies

---

## 🎯 Objective

The goal of this project is to build a machine learning model that predicts the **probability** that a farmer will adopt improved practices within:

- **7 days**
- **90 days**
- **120 days**

of their first training session.

⚠️ Important constraint:  
Predictions must be made **using only the information available at the time of training**.

---

## 📊 Problem Type

This is a:

**Multi-target Binary Classification Problem**

Input:
- Farmer demographic details
- Registration method
- Geographic information
- Training details
- Trainer information
- Topic-related features

Output:
- Probability of adoption within 7 days
- Probability of adoption within 90 days
- Probability of adoption within 120 days

---

## 📈 Evaluation Metrics

The competition evaluates models using:

- **AUC (Area Under ROC Curve)** – Measures ranking quality
- **LogLoss** – Measures probability accuracy

Due to extreme class imbalance (very low adoption rates), accuracy is not a reliable metric.

---

# 🌍 About Digital Africa

Launched in 2018, the **Digital Africa** initiative aims to strengthen the capacity of African digital entrepreneurs to design and deploy disruptive innovations at scale to serve the real economy.

The initiative brings together a diverse network of international partners committed to supporting African digital entrepreneurship, led by the French Development Agency (AFD).

---

# 🐄 About DigiCow Africa LTD

DigiCow Africa LTD is an award-winning Kenyan Agritech company established in 2018 (formerly FarmingTech Solutions).

The company develops mobile-based technologies that support the agricultural sector by:

- Enabling digital extension services  
- Supporting data-driven decision making  
- Strengthening the agricultural ecosystem  

In 2019, DigiCow was recognized as the most innovative Agritech in Kenya at a World Bank challenge and is part of the Disruptive Agricultural Technologies “1 Million Farmer Platform”.

Today, DigiCow works with over **200,000 farmers** across Kenya.

---

## 💡 Why This Problem Matters

Improving agricultural productivity is critical for:

- Food security  
- Economic stability  
- Smallholder farmer livelihoods  

By predicting which farmers are likely to adopt improved practices, we can:

- Improve intervention effectiveness  
- Increase adoption rates  
- Maximize impact of training programs  
- Drive data-driven agricultural transformation  
