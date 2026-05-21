# 🫁 Lung Cancer Prediction using Decision Tree

## 📊 Dataset
- **Source:** Survey Lung Cancer dataset  
- **Features:** AGE, GENDER, Smoking-related and health indicators  
- **Target Variable:** LUNG_CANCER (Yes/No)  

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Loaded dataset using **pandas**  
- Converted categorical variables into numerical format using **Label Encoding**  
- Handled missing values and unnecessary transformations  

### 2. Outlier Detection
- Applied **Interquartile Range (IQR)** method on `AGE` column  
- Calculated:  
  - Q1 (25th percentile)  
  - Q3 (75th percentile)  
  - IQR = Q3 - Q1  
- Defined bounds:  
  - Lower bound = Q1 - 1.5 × IQR  
  - Upper bound = Q3 + 1.5 × IQR  

### 3. Feature Transformation
- Applied **PowerTransformer (Yeo-Johnson)** to normalize `AGE` distribution  
- Reduced skewness and improved model performance  

### 4. Model Building
- Split dataset into **training (80%)** and **testing (20%)** sets  
- Used **Decision Tree Classifier** for prediction  
- Trained model on training data  

### 5. Model Evaluation
- Predicted results on test data  
- Measured performance using **accuracy score**  

---

## 🌳 Model Visualization
- Visualized trained **Decision Tree** using `plot_tree()`  
- Helps understand decision-making at each node  

---

## 📈 Results
- **Model Accuracy:** *accuracy: 0.967741935483871*  
- The model demonstrates how demographic and health factors influence lung cancer prediction  

---

## 🧰 Libraries Used
- numpy  
- pandas  
- matplotlib  
- seaborn  
- scikit-learn  

---

## 🚀 How to Run
1. Clone the repository  
2. Install required libraries:  
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
