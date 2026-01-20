# Auto Price Prediction – Project Report

## 1. Project Title
**Automobile Price Prediction Using Supervised Machine Learning (Regression)**

---

## 2. Project Overview
This project aims to build a machine learning model that predicts the **price of automobiles** using technical specifications such as brand, horsepower, engine size, body style, dimensions, and more.

The project helps automobile companies understand:

- Factors influencing vehicle prices  
- Customer buying behavior  
- How to design and price future models strategically  

This is a **Supervised Machine Learning Regression Project**.

---

## 3. Problem Statement
Automobile manufacturers want to determine the factors that influence car prices.  
Objectives:

- Predict car price using machine learning  
- Identify which features have the highest impact  
- Provide insights for pricing and design optimization  

---

## 4. Dataset Description
The dataset contains around **201 rows and 26 columns**.

### **Categorical Features**
- make  
- fuel-type  
- aspiration  
- body-style  
- num-of-doors  
- drive-wheels  
- engine-type  
- engine-location  
- fuel-system  

### **Numerical Features**
- wheel-base  
- length  
- width  
- height  
- engine-size  
- horsepower  
- peak-rpm  
- compression-ratio  

### **Target Variable**
`price`

---

## 5. Data Preprocessing

### ✔ Handling Missing Values
- Numerical: Filled using **Mean**  
- Categorical: Filled using **Mode**  
- Duplicate rows removed  
- No row deletion for missing values

### ✔ Handling Outliers
- IQR method used  
- Capping extreme values in horsepower & price

### ✔ Encoding Categorical Data
- **One-Hot Encoding** with `drop_first=True`

### ✔ Feature Scaling
- Applied **StandardScaler**  
- Required for regression models & stability

---

## 6. Feature Engineering
- Created power-to-weight ratio  
- Cleaned skewness with log-transform  
- Converted categorical data to numerical dummy variables  

---

## 7. Feature Selection Analysis

### ✔ Correlation Heatmap
High correlation found with:  
- Engine-size  
- Horsepower  
- Curb-weight  
- Wheel-base  
- Width  

### ✔ Variance Inflation Factor (VIF)
Used to remove multicollinearity.

### ✔ SelectKBest (ANOVA F-test)
Top selected features:  
- Engine-size  
- Horsepower  
- Width  
- Curb-weight  
- Length  

### ✔ RFE (Recursive Feature Elimination)
Best subset of features selected for regression.

### **Final Selected Features**
- Engine-size  
- Horsepower  
- Width  
- Curb-weight  
- Wheel-base  
- Length  
- Fuel-type (encoded)  
- Drive-wheels (encoded)

---

## 8. Model Building

Models used:

- **Multiple Linear Regression**  
- **Decision Tree Regressor**  
- **Random Forest Regressor**  
- **Gradient Boosting Regressor**

---

## 9. Model Evaluation

Metrics used:

- **R² Score**  
- **Mean Absolute Error (MAE)**  
- **Root Mean Squared Error (RMSE)**  

### **Best Model: Random Forest / Gradient Boosting**
- R² Score ≈ **0.93**  
- Low MAE  
- Low RMSE  

---

## 10. Customer Buying Behavior Insights

### **Customers value the most:**
1. Horsepower  
2. Engine-size  
3. Brand  
4. Body-style  
5. Fuel type  
6. Car dimensions  
7. Drive-wheel type  

### **Customers pay higher price for:**
- More horsepower  
- Bigger engine  
- Luxury brand  
- SUV or sports body style  
- Better fuel efficiency systems  

---

## 11. Difficulties Faced

- Missing values in key columns  
- Many categorical variables  
- Outliers affecting model performance  
- Multicollinearity  
- Small dataset → Overfitting risk  
- Feature scaling requirement  

---

## 12. Future Work

- Deploy model using Flask/Django  
- Create an interactive dashboard  
- Use Deep Learning for better predictions  
- Add customer reviews (sentiment analysis)  
- Integrate mileage, service history  
- Build real-time price API  
- Use AutoML for hyperparameter optimization  
- Add QR-based price comparison  

---

## 13. Conclusion
The Automobile Price Prediction model accurately predicts car prices using regression techniques.  
The most influential features include horsepower, engine-size, curb-weight, width, and brand.

This project provides important insights for:

- Pricing strategy  
- Customer preference analysis  
- Designing better automobiles  

The complete machine learning pipeline (preprocessing → modeling → evaluation) was successfully implemented.

---

