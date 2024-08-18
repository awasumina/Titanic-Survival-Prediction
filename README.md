# Titanic Data Analysis

This project involves analyzing the Titanic dataset to predict survival outcomes using logistic regression. The dataset contains information about passengers on the Titanic, including attributes such as age, sex, fare, and more.

## Dataset

The dataset used in this analysis includes the following columns:
- `PassengerId`: Unique ID for each passenger
- `Survived`: Survival status (0 = No, 1 = Yes)
- `Pclass`: Passenger class (1, 2, 3)
- `Name`: Name of the passenger
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `SibSp`: Number of siblings or spouses aboard
- `Parch`: Number of parents or children aboard
- `Ticket`: Ticket number
- `Fare`: Fare paid for the ticket
- `Cabin`: Cabin number
- `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)


## Analysis and Data Wrangling

1. **Loading Data:**
   - The dataset is loaded into a Pandas DataFrame.

2. **Initial Exploration:**
   - Count plots are generated to analyze the distribution of survival based on various attributes.
   - Histograms are plotted for the `Age` and `Fare` columns.

3. **Data Cleaning:**
   - Missing values in `Age` and `Cabin` columns are identified.
   - The `Age` column is dropped due to its high proportion of missing values.
   - Rows with any missing values are removed.
   - Categorical variables (`Sex`, `Embarked`, `Pclass`) are converted into dummy variables.

4. **Feature Selection:**
   - Unnecessary columns are removed.
   - The dataset is prepared for model training by splitting it into feature variables (`X`) and target variable (`y`).

5. **Model Training:**
   - Logistic Regression is used to train the model.
   - The dataset is split into training and testing sets.

6. **Evaluation:**
   - Classification report, confusion matrix, and accuracy score are used to evaluate model performance.


## Results

The Logistic Regression model achieved an accuracy score of approximately 0.785. Detailed metrics including classification report and confusion matrix provide further insights into model performance.

          precision    recall  f1-score   support

       0       0.78      0.87      0.82        13
       1       0.79      0.67      0.73        12

accuracy                           0.78        25



### Confusion Matrix

[[11 2]
[ 4 8]]



## Conclusion

The logistic regression model achieved an accuracy of **78.5%** in predicting Titanic survival outcomes. This indicates the model effectively distinguishes between survivors and non-survivors based on key features such as `Sex`, `Fare`, and `Pclass`. With Key Features:
- Model Performance: The model shows good predictive power with balanced precision and recall.
- Feature Importance: Key features significantly impact accuracy, while handling missing data was crucial.
- Future Improvements: Further enhancements could include exploring more advanced models or additional feature engineering.

