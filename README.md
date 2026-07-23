# 🏠 Lagos House Rent Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-blue?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)

<img width="1774" height="887" alt="image" src="https://github.com/user-attachments/assets/a8b00004-ad2b-4b53-addf-894b33da0c21" />


---

# 📌 Project Overview

Determining the appropriate rental price for residential properties in Lagos can be difficult due to variations in location, amenities, property type, and market demand.

This project develops a Machine Learning model capable of predicting rental prices of residential properties in Lagos, Nigeria by leveraging historical rental listings and engineered property features.

The project demonstrates the complete Data Science lifecycle—from data cleaning to model deployment preparation—and emphasizes building a reliable model while avoiding common pitfalls such as target leakage.

---

# 🎯 Project Objectives

The primary objective of this project is to build an intelligent machine learning model that can estimate the rental price of a property in Lagos using its characteristics.

Specifically, the project aims to:

- Predict residential rental prices accurately.
- Identify the major drivers of rental prices.
- Compare multiple Machine Learning algorithms.
- Improve model performance through Hyperparameter Tuning.
- Interpret model decisions using Feature Importance.
- Prepare the model for deployment.

---

# 📂 Dataset

The project uses rental property listings collected from Lagos real estate data.

Each property contains information such as:

- Property Title
- Property Type
- City
- Neighborhood
- Furnished Status
- Serviced Status
- Newly Built Status
- Boys' Quarter Availability
- Rental Frequency
- Rental Price

After extensive preprocessing, additional engineered features were introduced to improve prediction performance.

---

# 🛠️ Project Workflow

```
Data Collection
        │
        ▼
Data Cleaning
        │
        ▼
Exploratory Data Analysis (EDA)
        │
        ▼
Feature Engineering
        │
        ▼
Data Preprocessing
        │
        ▼
Machine Learning Models
        │
        ▼
Hyperparameter Tuning
        │
        ▼
Model Evaluation
        │
        ▼
Feature Importance
        │
        ▼
Cross Validation
        │
        ▼
Model Export
```

---

# 🧹 Data Cleaning

The original dataset contained numerous inconsistencies including:

- Mixed currencies
- Rental frequency inconsistencies
- Invalid price entries
- Missing values
- Duplicate records
- Irregular property descriptions
- Unstructured text

Cleaning involved:

✔ Converting prices into Nigerian Naira

✔ Standardizing rental frequency

✔ Removing unrealistic values

✔ Handling missing values

✔ Removing duplicates

✔ Cleaning property categories

✔ Formatting categorical variables

---

# 📊 Exploratory Data Analysis

Extensive Exploratory Data Analysis (EDA) was performed to understand the structure of the dataset.

### Univariate Analysis

- Rental Price Distribution
- Property Type Distribution
- Cities
- Neighborhoods
- Furnished Status
- Serviced Status
- Newly Built Status
- Rental Frequency
- Island vs Mainland
- Boys Quarter Distribution

### Bivariate Analysis

Relationships between:

- Property Type vs Rental Price
- City vs Rental Price
- Neighborhood vs Rental Price
- Furnished vs Price
- Serviced vs Price
- Island/Mainland vs Price

The EDA revealed that **location is the strongest determinant of rental prices in Lagos.**

---

# ⚙️ Feature Engineering

Several new predictive features were created including:

- Amenity Score
- Premium Neighborhood Indicator
- Neighborhood Frequency
- Property Type Frequency
- City Frequency
- Log Transformed Rental Price

During model development, engineered features were carefully reviewed to eliminate **target leakage**, ensuring realistic model performance.

---

# 🤖 Machine Learning Models

Four regression algorithms were trained and evaluated:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

Performance was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

# 🔍 Hyperparameter Tuning

RandomizedSearchCV was used to optimize the Random Forest Regressor.

Optimized Parameters included:

- Number of Trees
- Maximum Tree Depth
- Minimum Samples Split
- Minimum Samples Leaf
- Maximum Features
- Bootstrap Sampling

This improved the predictive performance of the model while reducing prediction error.

---

# 📈 Model Performance

| Model | R² Score |
|---------|---------:|
| Random Forest (Tuned) | **0.58** |
| Gradient Boosting | 0.57 |
| Linear Regression | 0.56 |
| Decision Tree | 0.55 |

The tuned Random Forest achieved the highest predictive accuracy and was selected as the final model.

---

# 📌 Model Evaluation

The project includes:

- Actual vs Predicted Plot
- Residual Analysis
- Feature Importance Analysis
- Cross Validation
- Error Metrics Comparison

These evaluations confirmed that the model generalizes reasonably well to unseen rental listings.

---

# ⭐ Feature Importance

The most influential features identified by the Random Forest model include:

- Premium Neighborhood
- Property Type
- Ikoyi Location
- Neighborhood
- Serviced Apartments
- Boys Quarter
- Island/Mainland Classification
- Amenity Score

The analysis confirms that **location remains the single most important factor influencing rental prices in Lagos.**

---

# 💡 Business Insights

This project provides valuable insights for multiple stakeholders.

### Property Owners

- Estimate competitive rental prices.
- Identify amenities that increase property value.

### Real Estate Agencies

- Automate rental valuation.
- Improve pricing consistency.

### Investors

- Identify high-value investment locations.
- Understand premium rental markets.

### Tenants

- Compare asking prices with predicted fair values.

---

# 🚀 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Joblib
- Jupyter Notebook

---

# 📁 Project Structure

```
Lagos-Rent-Prediction/
│
├── Data/
│      ├── Raw Dataset.csv
│      ├── Clean Dataset.csv
│
├── Notebook/
│      └── Lagos Rent Prediction.ipynb
│
├── Model/
│      └── lagos_rent_model.pkl 
│
├── Images/
│      ├── EDA
│      ├── Feature Importance
│      ├── Actual vs Predicted
│      └── Residual Plot
│
└── README.md
```

---

# 📌 Key Findings

- Premium neighborhoods command significantly higher rents.
- Property location is the strongest predictor of rental price.
- Serviced apartments attract higher rental values.
- Detached Duplexes and Mini Flats exhibit distinctive pricing patterns.
- Random Forest outperformed all other evaluated models.

---

# ⚠ Challenges Encountered

During development, several practical challenges were identified and addressed:

- Inconsistent rental price formats
- Missing values
- Duplicate records
- Mixed rental frequencies
- High-cardinality categorical variables
- Target leakage caused by engineered features

Resolving these challenges resulted in a more realistic and trustworthy model.

---

# 🔮 Future Improvements

Potential enhancements include:

- Incorporating number of bedrooms and bathrooms.
- Including floor area measurements.
- Adding property age.
- Integrating geospatial coordinates.
- Building a Streamlit web application.
- Deploying the model as a cloud-based API.

---

# 🎓 Conclusion

This project demonstrates the complete end-to-end Machine Learning workflow for predicting residential rental prices in Lagos.

Beyond building predictive models, emphasis was placed on data quality, feature engineering, model validation, interpretability, and business value.

The final tuned Random Forest model provides a reliable foundation for automated rental valuation systems and can serve as a valuable decision-support tool for landlords, tenants, investors, and real estate agencies.

---

# 👨‍💻 Author

**Onwuka Chukwuma**

Data Analyst | Machine Learning Enthusiast

If you found this project interesting, consider giving it a ⭐ on GitHub.
