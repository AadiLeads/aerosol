# Aerosol Classification
# 🌍 Global Aerosol-Type Classification using a Hybrid ML Algorithm

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository contains the code, methodology, and results for a machine learning project focused on classifying global aerosol types using a novel hybrid approach that combines **Gaussian Kernel Density Clustering** with a **Random Forest Classifier**. The project leverages data from **AERONET** and simulations from the **Mie Scattering Model** to develop a robust aerosol classification framework with high accuracy and scalability.

---

## 📌 Project Overview

### 🔬 Objective
To develop a **scalable**, **accurate**, and **hybrid machine learning model** for identifying global aerosol types using optical features derived from AERONET and synthetic datasets.

### 💡 Motivation
Aerosols significantly impact climate, air quality, and human health. Traditional classification methods lack scalability and precision due to the complexity and variability of aerosol properties. Our hybrid approach enhances classification accuracy and efficiency for global-scale applications in:

- Climate research 🌦️  
- Pollution monitoring 🏭  
- Atmospheric modeling ☁️  

---

## 📚 Methodology

### 1. Dataset Construction
- 47 globally distributed **AERONET** sites.
- Simulated data using **Mie Scattering** model.
- Target aerosol types:
  - Dust
  - Biomass Burning
  - Urban/Industrial
  - Mixed-Coarse
  - Mixed-Fine

### 2. Feature Extraction
- Single-Scattering Albedo (SSA)
- Asymmetry Parameter (g)
- Normalized AOD at various wavelengths
- Extinction Ångström Exponent (EAE)

### 3. Hybrid Model
- **Unsupervised:** Gaussian Kernel Density Clustering (to initialize class boundaries).
- **Supervised:** Random Forest Classifier (to refine and improve classification).

### 4. Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- Feature Importance Analysis

---

## 📊 Results

| Metric              | Baseline (Clustering Only) | Hybrid Model |
|---------------------|----------------------------|--------------|
| Micro-Precision     | 0.84                       | **0.95**     |
| Micro-Recall        | 0.80                       | **0.89**     |
| Micro-F1 Score      | 0.81                       | **0.91**     |
| Overall Accuracy    | 0.80                       | **0.89**     |

✅ High classification accuracy for **Dust** and **Urban/Industrial** types.  
⚠️ Misclassifications between **Mixed-Coarse** and **Mixed-Fine** due to overlapping features.

---

## 📈 Feature Importance

Top contributing features:
- SSA (440 nm)
- Extinction Ångström Exponent (440–870 nm)
- Asymmetry Parameter (870 nm)
- Normalized AOD (870 nm)

---

## 🧠 Key Insights

- The hybrid approach significantly outperforms traditional clustering methods.
- The framework is scalable and adaptable to diverse aerosol datasets.
- The model provides a global aerosol distribution map useful for various scientific domains.

---

## 🔗 References

1. Wei et al. (2024), *Atmospheric Chemistry and Physics*: [DOI](https://doi.org/10.5194/acp-24-5025-2024)  
2. L. Breiman (2001), *Random Forests*: [DOI](https://doi.org/10.1023/A:1010933404324)  
3. AERONET Dataset: [https://aeronet.gsfc.nasa.gov/](https://aeronet.gsfc.nasa.gov/)  
4. Mie Scattering Library: [http://scatterlib.wikidot.com/codes](http://scatterlib.wikidot.com/codes)

---

## 👨‍💻 Authors


- Namrata Mohane  
- Tanishq Nagdev  
- Aaditya Sawant  
- Harsh Zaveri  
**Department of CSE, Sardar Patel Institute of Technology, Mumbai**

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🚀 Future Work

- Integrate meteorological and satellite features
- Explore deep ensemble models
- Real-time aerosol classification dashboard

---



