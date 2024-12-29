# Movie Rentals Prediction: README

## Project Overview

A DVD rental company is seeking to enhance its inventory planning by predicting the number of days a customer will rent a DVD. Using this predictive model, the company aims to optimize its operations and improve efficiency. The objective of this project is to develop a regression model that accurately predicts rental duration, achieving a mean squared error (MSE) of 3 or less on a test set.

---

## Dataset Description

The dataset includes the following columns:

- **`rental_date`**: The date and time the customer rented the DVD.
- **`return_date`**: The date and time the customer returned the DVD.
- **`amount`**: The amount paid by the customer for renting the DVD.
- **`amount_2`**: The square of the `amount` column.
- **`rental_rate`**: The rate at which the DVD is rented.
- **`rental_rate_2`**: The square of the `rental_rate` column.
- **`release_year`**: The year the movie was released.
- **`length`**: The length of the movie in minutes.
- **`length_2`**: The square of the `length` column.
- **`replacement_cost`**: The cost to replace the DVD.
- **`special_features`**: Additional features of the DVD, such as trailers or deleted scenes.
- **`NC-17`**, **`PG`**, **`PG-13`**, **`R`**: Dummy variables representing the rating of the movie.

---

## Methodology

### **1. Data Loading and Inspection**
- The dataset was loaded and inspected to understand its structure, data types, and the relationship between features.

### **2. Data Preprocessing**
- Data cleaning was performed, including converting columns to their appropriate data types.
- New features were created based on existing ones to enhance the predictive power of the models.

### **3. Model Training**
- The dataset was split into training (80%) and testing (20%) sets.
- Multiple regression models were evaluated, including:
  - Random Forest Regressor
  - Gradient Boosting Regressor
  - AdaBoost Regressor
  - Decision Tree Regressor
  - XGBoost Regressor

- **Cross-validation and Hyperparameter Tuning**:
  - GridSearchCV was used to optimize model parameters for better performance.

### **4. Performance Metrics**
- Models were evaluated using:
  - Mean Squared Error (MSE)
  - R-squared (R²)

---

## Results

Among the models tested, the **Gradient Boosting Regressor** achieved the best results:

### **Best Model: Gradient Boosting Regressor**
- **Hyperparameters**:
  - `learning_rate=0.2`
  - `max_depth=5`
  - `n_estimators=200`
  - `random_state=9`
- **Performance**:
  - Test MSE: **1.935**
  - Test R²: **0.727**

The Gradient Boosting Regressor was selected as the final model due to its lowest MSE, meeting the project's objective of achieving an MSE of 3 or less.

---

## Conclusion

The predictive model provides accurate predictions of rental durations, helping the company improve inventory planning and efficiency. With the Gradient Boosting Regressor, the company can better forecast DVD rental behavior and make data-driven decisions for inventory management.
