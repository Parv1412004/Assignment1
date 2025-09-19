# Assignment1  
# Forecasting Medical Insurance Costs using Linear Regression

This project demonstrates a **machine learning regression task** to predict medical insurance costs based on personal attributes. The primary algorithm used is **Linear Regression**, and the entire workflow is documented in a Jupyter/Kaggle notebook.

---

## 📌 Project Overview

The goal is to build a model that can accurately forecast insurance charges for an individual given a set of features.  
Key steps involved:

1. **Data Exploration** – Understanding the dataset and feature relationships.  
2. **Data Preprocessing** – Converting raw data into machine-learning-ready format.  
3. **Model Training** – Training a Linear Regression model on the dataset.  
4. **Model Evaluation** – Assessing model performance on unseen data.

---

## 📊 Dataset

The project uses the **"Medical Cost Personal Dataset"** from Kaggle.  

- File: `insurance.csv`  
- Records: **1,338 rows**  
- Columns: **7 features + 1 target (`charges`)**

| Feature     | Description |
|-------------|-------------|
| `age`       | Age of the primary beneficiary |
| `sex`       | Gender (male, female) |
| `bmi`       | Body Mass Index |
| `children`  | Number of dependents |
| `smoker`    | Smoking status (yes, no) |
| `region`    | Residential area in the US |
| `charges`   | Medical costs billed (**Target Variable**) |

---

## 🛠 Methodology

1. **Exploratory Data Analysis (EDA)**  
   - Histograms, scatter plots, and heatmaps were used.  
   - Insights:  
     - `charges` is right-skewed.  
     - Smoking status is the strongest predictor.  
     - `age` and `bmi` are positively correlated with `charges`.

2. **Data Preprocessing**  
   - Encoded categorical features (`sex`, `smoker`, `region`) using **One-Hot Encoding** (`pd.get_dummies`).  

3. **Model Training**  
   - Split dataset into training (80%) and testing (20%).  
   - Trained a **LinearRegression** model using `scikit-learn`.  

---

## ✅ Results

Performance on the test set:

- **Mean Absolute Error (MAE)**: `4181.19`  
- **Mean Squared Error (MSE)**: `33596915.85`  
- **R² Score**: `0.7836`  

📌 The model explains **~78.4% of the variance** in insurance charges, which is strong for a baseline Linear Regression.

---

## 🚀 How to Run

1. **Install dependencies**  
   Make sure you have Python and the required libraries installed:  

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn  
2. **Get the dataset**  
   Download insurance.csv from Kaggle and place it in the project directory.  

3. **Run the notebook**  
   Open the .ipynb notebook in Jupyter Notebook, JupyterLab, or VS Code, and execute the cells sequentially.  
