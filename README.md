# SpaceX Falcon 9 First Stage Landing Prediction  

### Machine Learning Project  

## Overview  
SpaceX advertises Falcon 9 rocket launches for 62 million dollars, while competitors charge around 165 million dollars for similar missions. The main reason for this difference is reusability — SpaceX can recover and reuse the first stage of the rocket.  

This project builds a machine learning pipeline to predict whether the first stage of a Falcon 9 rocket will successfully land. The prediction helps estimate launch costs and understand SpaceX’s competitive advantage in the aerospace industry.  

---

## Methodology  

### 1. Business Understanding  
**Goal:** Predict whether the Falcon 9 first stage will successfully land.  
**Insight:** Successful recovery of the first stage directly lowers launch costs and increases operational efficiency.  

### 2. Data Collection and Preparation  
- Data was collected from the **SpaceX public API** using Python and Jupyter Notebook.  
- The dataset was cleaned and transformed using `pandas`, `numpy`, and `scikit-learn`.  
- Redundant columns were removed, missing values were handled, and categorical data was encoded into numerical form.  
- Continuous variables such as **Payload Mass** and **Flights** were **standardized** to ensure fair comparison between features and improve model accuracy.  

### 3. Modeling  
Several classification models were trained and compared:  
- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Support Vector Machine (SVM)  

Before training, the dataset was split into **training** and **test** sets.  
**GridSearchCV** was used to optimize hyperparameters and improve model performance.  

After evaluating all models using accuracy, precision, recall, and confusion matrices, the **Support Vector Machine (SVM)** achieved the **highest accuracy** on the test data.  

The final trained model was saved as `model.pkl` using the **pickle** library for future reproducibility.  

---

## Results and Insights  
- The **SVM model** produced the highest accuracy among all tested algorithms.  
- Standardizing the features significantly improved the reliability and performance of all models.  
- The most influential predictors of successful landing were **launch site**, **orbit type**, and **payload mass**.  
- These results confirm that operational and orbital conditions play a major role in determining SpaceX’s ability to reuse the rocket’s first stage.  
- The developed model provides a reproducible framework for predicting reusability and estimating cost savings in rocket launches.  

---

## Tools and Technologies  
Python, Jupyter Notebook, pandas, numpy, matplotlib, seaborn, scikit-learn, GridSearchCV, pickle, SpaceX API  

---

## How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/SpaceX-Falcon9-Landing-Prediction.git
   cd SpaceX-Falcon9-Landing-Prediction
