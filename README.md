# CrimeCast: Forecasting Crime Categories

This project aims to analyze crime incidents and build predictive models capable of forecasting the category of crime based on various attributes.

---

## Aim
To leverage machine learning techniques to predict the **crime category** for incidents based on comprehensive datasets. The project involves exploratory data analysis, feature engineering, model development, and evaluation.

---

## Dataset Overview

The dataset provides detailed information about crime incidents, including geographical, temporal, and victim-related attributes. Here's a breakdown of the files:

### Data Files:
- **`train.csv`**: The training set, including the target variable `crime_category` and relevant feature attributes.
- **`test.csv`**: The test set, containing similar features but excluding the target variable `crime_category`.
- **`sample.csv`**: A file illustrating the expected format of predictions.

### Columns Description:
- **Location**: Street address of the crime incident.
- **Cross_Street**: Cross street of the rounded address.
- **Latitude**: Latitude coordinates of the crime incident.
- **Longitude**: Longitude coordinates of the crime incident.
- **Date_Reported**: Date the incident was reported.
- **Date_Occurred**: Date the incident occurred.
- **Time_Occurred**: Time the incident occurred (24-hour format).
- **Area_ID**: LAPD's Geographic Area number.
- **Area_Name**: Name designation of the LAPD Geographic Area.
- **Reporting_District_no**: Reporting district number.
- **Part 1-2**: Crime classification.
- **Modus_Operandi**: Activities associated with the suspect.
- **Victim_Age**: Age of the victim.
- **Victim_Sex**: Gender of the victim.
- **Victim_Descent**: Descent code of the victim.
- **Premise_Code**: Code indicating the location of the crime.
- **Premise_Description**: Description of the premise code.
- **Weapon_Used_Code**: Weapon code indicating the type of weapon used.
- **Weapon_Description**: Description of the weapon code.
- **Status**: Status of the case.
- **Status_Description**: Description of the status code.
- **Crime_Category**: The target variable representing the category of crime.

---

## Methodology

1. **Data Preparation**:
   - Loaded and cleaned the dataset.
   - Handled missing values, outliers, and inconsistencies.

2. **Exploratory Data Analysis (EDA)**:
   - Investigated data distributions and relationships.
   - Visualized patterns across attributes like location, time, and victim demographics.

3. **Feature Engineering**:
   - Created new features from date and time information.
   - Encoded categorical variables using techniques like one-hot encoding or label encoding.
   - Normalized numerical features for better model performance.

4. **Model Development**:
   - Split the dataset into training and validation sets.
   - Trained various machine learning models, including:
     - Logistic Regression
     - Random Forest
     - Gradient Boosting (e.g., XGBoost, LightGBM)
     - Neural Networks
   - Used grid search and cross-validation to optimize hyperparameters.

5. **Evaluation**:
   - Assessed models using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.
   - Selected the best-performing model based on validation performance.

6. **Prediction and Submission**:
   - Predicted crime categories for the test set.
---

## Tech Stack
- **Programming Language**: Python
- **Libraries**:
  - Data Manipulation: Pandas, NumPy
  - Visualization: Matplotlib, Seaborn, Plotly
  - Machine Learning: scikit-learn, XGBoost, LightGBM
- **Tools**:
  - Jupyter Notebook
  - Git for version control

---

## Insights and Findings

1. **Crime Distribution by Time:**
   - Most "Fraud and White Collar Crimes" and "Crimes Against Persons" occur in the **first week of the month.**
   - "Property Crimes" and "Violent Crimes" are **evenly distributed throughout the month.**
   - "Other Crimes" peak during the **third week of the month.**
    
2. **Geographical Hotspots:**
   - The area with the highest crime rate is **77th Street.**

3. **Weapon Usage:**
   - The most commonly used weapon is **'STRONG-ARM (HANDS, FIST, FEET OR BODILY FORCE)'.**

4. **Temporal Patterns:**
   - Maximum crimes occur on the **first day of the month** and the **4th day of the week.**
   - Crimes are most frequent around **noon.**

5. **Victim Demographics:**
   - The most targeted victims are of **descent 'H'.**
   - In many cases, either the victim's age is unknown, or no victim was present.

6. **Seasonal Trends:**
   - Most crimes occur in **January.**

7. **Best Model:**
   - The **Gradient Boosting** model achieved the best performance with an accuracy of **86.98%.**
---

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this software for both personal and commercial purposes, provided the original source is credited.
