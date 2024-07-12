# Logistic Regression and Linear Discriminant Analysis for Predicting Holiday Package Opt-in

## Project Overview

You are hired by a tour and travel agency which deals in selling holiday packages. You are provided details of 872 employees of a company. Among these employees, some opted for the package and some didn't. You have to help the company in predicting whether an employee will opt for the package or not on the basis of the information given in the dataset. Additionally, you need to identify the important factors that influence the decision to opt for the package so that the company can focus on targeting those employees.

## Data Dictionary

| Variable Name         | Description                               |
|-----------------------|-------------------------------------------|
| Holiday_Package       | Opted for Holiday Package (yes/no)        |
| Salary                | Employee salary                           |
| Age                   | Age in years                              |
| Education             | Years of formal education                 |
| No_Young_Children     | The number of young children (<7 years)   |
| No_Older_Children     | Number of older children                  |
| Foreign               | Foreigner (Yes/No)                        |

## Project Steps

### 1. Data Ingestion
- Read the dataset.
- Perform descriptive statistics and check for null values.
- Write an inference on the dataset quality.

### 2. Exploratory Data Analysis (EDA)
- Perform univariate and bivariate analysis.
- Visualize the data using histograms, frequency polygons, violin plots, scatter plots, pair plots, and heatmaps.
- Identify and discuss any significant outliers.

### 3. Data Preprocessing
- Encode categorical variables.
- Split the data into training and testing sets (70:30).
- Apply Logistic Regression and Linear Discriminant Analysis (LDA) models.

### 4. Model Evaluation
- Evaluate model performance using accuracy, confusion matrix, ROC curve, and ROC AUC score for both models.
- Compare and determine the best model.

### 5. Inferences and Recommendations
- Provide business insights based on the model predictions.
- Suggest strategies for targeting employees likely to opt for the holiday package.

## Findings and Inferences

### Exploratory Data Analysis
- The dataset contains 872 rows and 8 columns.
- No null values are present.
- Data types include integers and objects.
- No duplicate rows were found.
- Significant outliers were observed in the Salary column but were retained as salary variations are natural. Boxplot of Salary indicating the variables is given below.

  ![image](https://github.com/user-attachments/assets/027c6ce2-fa8a-43fd-84d5-31d5a26342b8)

### Univariate Analysis
- Distribution of numerical variables was visualized using histograms, frequency polygons, and violin plots.
- The cumulative distribution function indicated the density of data points.

  ![image](https://github.com/user-attachments/assets/8d7e7db6-f7c7-4abc-9a85-267ee8487191)
  
  ![image](https://github.com/user-attachments/assets/d3ee8143-9d3b-416e-ae35-a1839b0b4082)

  ![image](https://github.com/user-attachments/assets/b4a2c197-f6f8-4ef6-bafb-b756e30108e3)

### Bivariate and Multivariate Analysis
- Pair plots and scatter plots showed relationships between variables.
- Heatmaps indicated correlations, highlighting some strong positive and negative relationships.

  ![image](https://github.com/user-attachments/assets/6b072790-63a9-4381-9cd6-fff5ad55304f)

  ![image](https://github.com/user-attachments/assets/cbf85e0a-f685-4187-a3bb-91e54533005e)

### Model Performance
#### Logistic Regression
- Classification Report:
  - Class 0 (did not opt): Precision = 0.55, Recall = 0.89, F1 = 0.68
  - Class 1 (opted): Precision = 0.38, Recall = 0.09, F1 = 0.14
- Accuracy: 0.53
- Confusion Matrix: 
  - True Positives: 129
  - False Positives: 16
  - True Negatives: 107
  - False Negatives: 10
- AUC-ROC Score: Train = 0.567, Test = 0.627

Train AUC-ROC Score:

![image](https://github.com/user-attachments/assets/61d9022d-a004-4ad9-a9de-f0e0bdbc6fdf)

Test AUC-ROC Score:

![image](https://github.com/user-attachments/assets/4346df4f-4a5c-400e-aa16-1fae3db1f8f6)

#### Linear Discriminant Analysis (LDA)
- Classification Report:
  - Class 0 (did not opt): Precision = 0.66, Recall = 0.76, F1 = 0.71
  - Class 1 (opted): Precision = 0.66, Recall = 0.54, F1 = 0.60
- Accuracy: 0.66
- Confusion Matrix: 
  - True Positives: 360
  - False Positives: 111
  - True Negatives: 183
  - False Negatives: 218
- AUC-ROC Score: Train = 0.740, Test = 0.709

Train AUC-ROC Score:

![image](https://github.com/user-attachments/assets/dbaa672e-e6e6-4aa7-a557-f8aaa3fc4867)

Test AUC-ROC Score:

![image](https://github.com/user-attachments/assets/a56a4a34-f979-4e02-bd92-6976ae365b33)

### Conclusion
- The LDA model outperformed Logistic Regression in terms of accuracy, precision, recall, and AUC-ROC scores.
- LDA is the best-suited model for predicting whether an employee will opt for the holiday package.

### Business Insights and Recommendations
1. **Target Demographics:**
   - Employees who are not foreigners are more likely to opt for the holiday package.
   - Employees without children are more inclined to purchase the travel package.
   - Younger employees (20-40 years old) show a higher propensity to opt for the package.
   - Employees earning between Rs. 30,000 to Rs. 50,000 are more likely to opt for the package.

2. **Marketing Strategies:**
   - Focus marketing efforts on non-foreign employees, those without children, and younger employees.
   - Customize packages and offers to appeal to the identified target groups.
   - Highlight travel packages that fit within the identified salary range to maximize engagement and conversions.

By leveraging these insights, the travel agency can optimize their marketing strategies to effectively sell holiday packages to the most responsive employee groups.
