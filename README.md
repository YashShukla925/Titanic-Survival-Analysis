# Titanic Survival Analysis

## Overview
This project aims to analyze the Titanic dataset to determine the factors that influenced passenger survival rates. The analysis involves data preprocessing, exploratory data analysis (EDA), and building machine learning models to predict survival outcomes.

## Dataset
The dataset used is the Titanic dataset from Kaggle, which includes the following features:
- `PassengerId`: Unique ID for each passenger
- `Survived`: Survival status (0 = No, 1 = Yes)
- `Pclass`: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
- `Name`: Name of the passenger
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `SibSp`: Number of siblings/spouses aboard
- `Parch`: Number of parents/children aboard
- `Ticket`: Ticket number
- `Fare`: Passenger fare
- `Cabin`: Cabin number
- `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## Data Preprocessing
1. **Handling Missing Values**: 
   - Impute missing values for `Age` using the median age.
   - Fill missing values in `Embarked` with the mode.
   - Drop the `Cabin` feature due to a high number of missing values.

2. **Encoding Categorical Variables**:
   - Convert `Sex` to binary (0 for male, 1 for female).
   - Use one-hot encoding for `Embarked`.

3. **Feature Scaling**:
   - Standardize numerical features such as `Age` and `Fare`.

4. **Feature Engineering**:
   - Create new features such as `FamilySize` (SibSp + Parch + 1).
   - Create an `IsAlone` feature to indicate if the passenger was alone.

## Exploratory Data Analysis (EDA)
Key insights from EDA:
- Higher survival rate for females compared to males.
- Passengers in 1st class had a higher survival rate than those in 2nd and 3rd classes.
- Children (age < 16) had higher survival rates.
- Passengers who embarked from Cherbourg (C) had a higher survival rate compared to other ports.

## Model Building
We built and evaluated several machine learning models:
1. **Logistic Regression**
2. **Decision Tree**
3. **Random Forest**
4. **Support Vector Machine (SVM)**
5. **K-Nearest Neighbors (KNN)**

## Model Evaluation
Models were evaluated based on accuracy, precision, recall, and F1-score. The Random Forest model achieved the best performance with the highest accuracy and balanced precision-recall scores.

## Conclusion
The analysis revealed that gender, passenger class, and age were significant factors influencing survival rates on the Titanic. The Random Forest model was the most effective in predicting survival outcomes.

## How to Run
1. Clone the repository:
    ```bash
    git clone <repository_url>
    ```
2. Navigate to the project directory:
    ```bash
    cd titanic-survival-analysis
    ```
3. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter Notebook:
    ```bash
    jupyter notebook Titanic_Survival_Analysis.ipynb
    ```

## Files
- `Titanic_Survival_Analysis.ipynb`: Jupyter Notebook with the analysis and model building steps.
- `requirements.txt`: List of Python libraries required to run the project.
- `data/`: Directory containing the Titanic dataset.

## References
- [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)

## Author
[Your Name]
