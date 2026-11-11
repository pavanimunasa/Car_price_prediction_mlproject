
# 🚗 Car Price Prediction using Machine Learning

A Machine Learning project that predicts the selling price of used cars based on various vehicle attributes such as manufacturing year, present price, kilometers driven, fuel type, seller type, transmission type, and number of previous owners.

This project demonstrates the complete Machine Learning pipeline, including data preprocessing, exploratory data analysis, feature encoding, model training, evaluation, and prediction** using Python and Scikit-learn.


# 📌 Table of Contents

- Project Overview
- Dataset
- Machine Learning Workflow
- Technologies Used
- Project Structure
- Data Preprocessing
- Feature Engineering
- Model Training
- Model Evaluation
- Results
- Visualizations
- How to Run
- Future Improvements
- Author


# 📖 Project Overview

The objective of this project is to build a Machine Learning Regression model that accurately predicts the selling price of a used car.

Since the output is a continuous numerical value, this is a **Regression Problem**.

The project compares the performance of two popular regression algorithms:

- Linear Regression
- Lasso Regression


# 📊 Dataset

The dataset contains information about previously sold cars.

| Feature | Description |
|----------|-------------|
| Car Name | Manufacturer / Model of the car |
| Year | Manufacturing year |
| Selling Price | Selling price of the used car (Target Variable) |
| Present Price | Current showroom price of the same model |
| Kms Driven | Total kilometers driven |
| Fuel Type | Petrol / Diesel / CNG |
| Seller Type | Dealer / Individual |
| Transmission | Manual / Automatic |
| Owner | Number of previous owners |

### Dataset Size

- Rows: 301
- Columns: 9 Features + Target

---

# 🔄 Machine Learning Workflow


Dataset
     │
     ▼
Data Collection
     │
     ▼
Data Preprocessing
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Categorical Encoding
     │
     ▼
Feature Selection
     │
     ▼
Train-Test Split
     │
     ▼
Model Training
     │
     ▼
Prediction
     │
     ▼
Model Evaluation


# 🛠️ Technologies Used

### Programming Language

- Python

### Development Environment

- Google Colaboratory (Google Colab)

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn


# 📂 Project Structure

Car-Price-Prediction/
│
├── Car_Price_Prediction.ipynb
├── car data.csv
├── README.md
└── requirements.txt


---

# 🧹 Data Preprocessing

The following preprocessing steps were performed before training the model:

### ✔ Loading Dataset

python
pd.read_csv()


### ✔ Data Inspection

- Display first five rows
- Check dataset dimensions
- Verify data types
- Identify missing values

Methods used:

- head()
- shape
- info()
- isnull().sum()

Result:

- No missing values were found.

---

# 🔄 Categorical Feature Encoding

Machine Learning models require numerical input, so categorical values were converted into numerical values.

### Fuel Type

| Category | Encoded Value |
|-----------|---------------|
| Petrol | 0 |
| Diesel | 1 |
| CNG | 2 |

### Seller Type

| Category | Encoded Value |
|-----------|---------------|
| Dealer | 0 |
| Individual | 1 |

### Transmission

| Category | Encoded Value |
|-----------|---------------|
| Manual | 0 |
| Automatic | 1 |

Encoding was performed using the replace() function.

---

# 🎯 Feature Selection

### Input Features (X)

- Year
- Present Price
- Kms Driven
- Fuel Type
- Seller Type
- Transmission
- Owner

### Target Variable (Y)

Selling Price
The following columns were removed before training:

- Car Name
- Selling Price (Target)

---

# ✂ Train-Test Split

The dataset was divided into training and testing sets.

python
train_test_split()

Parameters:

- Training Data: 90%
- Testing Data: 10%
- random_state = 2

Using a fixed random state ensures reproducible results.

---

# 🤖 Models Used

## 1. Linear Regression

Linear Regression models the relationship between input features and the target variable using a straight-line equation.

Training:

python
LinearRegression()


Steps:

- Train model
- Predict on training data
- Predict on testing data
- Evaluate performance

---

## 2. Lasso Regression

Lasso Regression is a regularized version of Linear Regression that helps reduce overfitting by penalizing less important features.

Training:
Lasso()
Steps:
- Train model
- Predict values
- Evaluate using R² Score

# 📈 Model Evaluation

The performance of both models was evaluated using the **R² Score (Coefficient of Determination)**.

The R² score ranges from **0 to 1**, where values closer to **1** indicate better prediction accuracy.

## Linear Regression Performance

| Dataset | R² Score |
|----------|-----------|
| Training | 0.879 |
| Testing | 0.836 |


## Lasso Regression Performance

| Dataset | R² Score |
|----------|-----------|
| Training | **0.840** |
| Testing | Comparable performance with improved regularization |


# 📉 Visualization

The project visualizes the relationship between:

- Actual Selling Price
- Predicted Selling Price

using a scatter plot.

A good model produces points that lie close to the diagonal line, indicating that predicted values closely match the actual values.

# 🚀 How to Run the Project

### 1. Clone the Repository

bash:
git clone https://github.com/your-username/Car-Price-Prediction.git

### 2. Navigate to the Project Folder

bash:
cd Car-Price-Prediction

### 3. Install Dependencies

bash:
pip install -r requirements.txt

### 4. Run the Notebook

Open:

Car_Price_Prediction.ipynb

Run all cells sequentially.

---

# 📌 Future Improvements

- Hyperparameter tuning
- Feature scaling
- Cross-validation
- Random Forest Regressor
- XGBoost Regressor
- Gradient Boosting Regressor
- Model deployment using Flask/FastAPI
- Interactive web application using Streamlit

---

# 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- Data preprocessing
- Exploratory Data Analysis (EDA)
- Handling categorical variables
- Feature engineering
- Regression algorithms
- Model evaluation using R² Score
- Data visualization
- Building an end-to-end Machine Learning pipeline

---

# 👨‍💻 Author
MUNASA PAVANI SRI VAISHNAVI

- GitHub: https://github.com/pavanimunasa
- LinkedIn: https://www.linkedin.com/in/munasa-pavani-b81909241/
