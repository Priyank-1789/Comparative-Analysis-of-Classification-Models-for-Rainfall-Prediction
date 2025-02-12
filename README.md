# Comparative-Analysis-of-Classification-Models-for-Rainfall-Prediction
# **Comparative Analysis of Classification Models for Rainfall Prediction**

## **Table of Contents**
- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Installation & Setup](#installation--setup)
- [Model Evaluation Metrics](#model-evaluation-metrics)
- [Results & Insights](#results--insights)
- [Future Enhancements](#future-enhancements)

---

## **Overview**
This project focuses on predicting rainfall using **classification algorithms** applied to historical weather data (2008–2017). The goal is to train models and evaluate their accuracy in predicting whether it will rain tomorrow based on meteorological parameters.

The following **classification models** were implemented:
1. **K-Nearest Neighbors (KNN)**
2. **Decision Tree**
3. **Logistic Regression**
4. **Support Vector Machine (SVM)**
5. **Linear Regression (for baseline comparison)**

---

## **Dataset Description**
The dataset, **weatherAUS.csv**, contains weather observations, including:

| Feature         | Description                                   | Unit       | Type   |
|---------------|---------------------------------|------------|------|
| Date          | Observation date               | YYYY-MM-DD  | object |
| Location      | City where data was collected  | City Name   | object |
| MinTemp       | Minimum temperature of the day | Celsius     | float  |
| MaxTemp       | Maximum temperature of the day | Celsius     | float  |
| Rainfall      | Rainfall amount                | mm          | float  |
| WindGustDir   | Direction of strongest wind gust | Cardinal Direction | object |
| WindGustSpeed | Speed of strongest wind gust   | km/h        | float  |
| RainToday     | Whether it rained today (Yes/No) | Binary   | object |
| RainTomorrow  | **Target Variable**: Will it rain tomorrow? (Yes/No) | Binary | object |

---

## **Technologies Used**
- Python
- Pandas, NumPy (Data Processing)
- Matplotlib, Seaborn (Visualization)
- Scikit-Learn (Machine Learning Models)
- Jupyter Notebook

---

## **Project Workflow**
1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical variables (One-Hot Encoding)
   - Normalizing numerical features
   - Splitting data into train & test sets

2. **Model Training**
   - Training classifiers on the dataset
   - Tuning hyperparameters for better performance

3. **Model Evaluation**
   - Measuring accuracy, precision, recall, F1-score
   - Comparing model performance

---

## **Installation & Setup**
### **1. Clone the Repository**
```bash
 git clone https://github.com/your-username/Rainfall-Prediction.git
 cd Rainfall-Prediction
```

### **2. Install Dependencies**
Ensure you have Python 3 installed, then run:
```bash
pip install -r requirements.txt
```

### **3. Run the Jupyter Notebook**
```bash
jupyter notebook Rain Prediction.ipynb
```

---

## **Model Evaluation Metrics**
We used the following performance metrics:

- **Accuracy Score** – Measures overall correctness.
- **Jaccard Index** – Intersection over union of predicted vs actual classes.
- **F1-Score** – Harmonic mean of precision and recall.
- **LogLoss** – Measures uncertainty in probabilistic predictions.
- **Mean Absolute Error (MAE)** – Average absolute errors in prediction.
- **Mean Squared Error (MSE)** – Average squared errors.
- **R² Score** – Determines how well the model explains variance.

---

## **Results & Insights**

| Model                | Accuracy | Jaccard Score | F1-score | LogLoss |
|----------------------|----------|--------------|---------|---------|
| **KNN (K=4)**       | 81.83%   | 0.7901       | 0.8024  | N/A     |
| **Decision Tree**   | 79.85%   | 0.7639       | 0.5926  | N/A     |
| **Logistic Regression** | 83.82% | 0.8051 | 0.6768 | 0.3797 |
| **SVM**             | **84.58%** | **0.8133** | **0.6930** | N/A |

### **Key Findings:**
✅ **SVM performed the best with the highest accuracy (84.58%)** and F1-score.  
✅ **Logistic Regression is a strong alternative (83.82%)**.  
✅ **KNN performed well (81.83%)**, but parameter tuning could improve performance.  
❌ **Decision Tree underperformed (79.85%)**, and an ensemble approach (e.g., Random Forest) could help.  

#### **Regression Model Results (For Baseline Comparison):**
| Model                  | MAE    | MSE    | R² Score  |
|------------------------|--------|--------|----------|
| **Linear Regression**  | 0.2563 | 0.1157 | -0.3847  |
| **Decision Tree Regressor** | **0.1354** | **0.0489** | **0.4732** |

✅ **Decision Tree Regressor significantly outperformed Linear Regression**.  
❌ **Linear Regression had a negative R² score, meaning it was a poor fit.**  

---

## **Future Enhancements**
- Implement **Random Forest** and **Gradient Boosting** for better accuracy.
- Optimize hyperparameters using **GridSearchCV**.
- Perform **feature engineering** for improved insights.
- Deploy as a **web-based ML model** using Flask/Django.

---

If you find this project useful, feel free to ⭐ the repository! 🚀

