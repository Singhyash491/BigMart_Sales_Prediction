# Big Mart Sales Prediction

## 📖 Overvie
This project aims to predict the sales of products across various outlets in the Big Mart dataset. Using historical data, we employ machine learning techniques to build a regression model that predicts the target variable, `Item_Outlet_Sales`, based on features such as product type, visibility, outlet type, and more.

---

## 🛠️ Problem Statement
Big Mart, a retail chain, collects data on product sales across multiple outlets. The objective is to develop a predictive model that:
- Analyzes the relationship between various features and sales.
- Accurately forecasts sales for future scenarios.

---

## 📝 Dataset
The dataset contains the following key features:
- **Item_Identifier**: Unique identifier for each product.
- **Item_Weight**: Weight of the product.
- **Item_Fat_Content**: The fat content of the product (e.g., low fat, regular).
- **Item_Visibility**: Percentage visibility of the product in the store.
- **Outlet_Size**: Size of the store (e.g., Small, Medium, High).
- **Outlet_Location_Type**: Type of location for the store (e.g., Tier 1, Tier 2).
- **Item_Outlet_Sales**: Target variable; the sales amount for the product.

---

## 🔍 Steps Undertaken
1. **Exploratory Data Analysis (EDA)**:
   - Loaded the dataset and performed an initial inspection using `.info()` and `.describe()`.
   - Visualized relationships between features and the target variable using libraries like `seaborn` and `matplotlib`.

2. **Data Cleaning**:
   - Handled missing values:
     - Filled missing `Item_Weight` values with the mean.
     - Imputed missing `Outlet_Size` values with the mode, based on `Outlet_Type`.
   - Standardized inconsistent entries in categorical features like `Item_Fat_Content`.

3. **Feature Encoding**:
   - Encoded categorical variables (e.g., `Outlet_Type`, `Item_Fat_Content`) using `LabelEncoder`.

4. **Model Training**:
   - Split the data into training and test sets using `train_test_split`.
   - Trained two models:
     - **Linear Regression**: A basic regression model.
     - **XGBRegressor**: A gradient-boosting model for more robust predictions.
   - Used the trained model to predict `Item_Outlet_Sales` on the test data (`x_test`).

---

## 📊 Libraries and Tools Used
- **Data Manipulation**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
- **Machine Learning**: `sklearn`, `xgboost`

---

## ⚙️ Output
- The trained model (`XGBRegressor`) generated predictions for the test data (`y_pred`), which were stored as a NumPy array. These predictions correspond to the target variable (`Item_Outlet_Sales`) for each row in the test set.
