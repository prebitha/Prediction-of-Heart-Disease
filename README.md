# Prediction of Heart Disease
![heart](https://user-images.githubusercontent.com/81169091/119009637-9ec56600-b993-11eb-8d8e-791c8be74bb5.jpg)

Heart disease is one of the leading cause of death in the Unites States. The Dataset I have used is available in the UCI, Machine Learning Repository (This is also available in Kaggle). 

### ABOUT THE DATASET
First I did my Study on the Dataset using Tableau. Please go through this inorder to understand the dataset better [ tableau link here ](https://public.tableau.com/profile/prebitha.staphney.abraham#!/vizhome/HeartDiseaseDatasetStudy/cardiaccatheterization?publish=yes)

Here is the Summary of the Columns in the Dataset:


|   ABBREVIATION    |                                          DETAILS                                               |    
|-------------------|------------------------------------------------------------------------------------------------|
|  age              |       Age of the patient                                                                       |
|  sex              |       Sex of the patient                                                                       |
|  cp               |Chest pain type, 0 = Typical Angina, 1 = Atypical Angina, 2 = Non-anginal Pain, 3 = Asymptomatic|
|  trtbps           |  Resting blood pressure (in mm Hg)                                                             |   
|  chol             |     Cholestoral in mg/dl fetched via BMI sensor                                                |
|  fbs              |     ( fasting blood sugar > 120 mg/dl), 1 = True, 0 = False                                    |
|  restecg          | Resting electrocardiographic results*                                                          |
|  thalachh         | Maximum heart rate achieved                                                                    |
|  oldpeak          | Previous peak                                                                                  |
|  slp              | Slope                                                                                          |
|  caa              | Number of major vessels                                                                        |
|  thall            | Thalium Stress Test result ~ (0,3)                                                             |
|  exng             | Exercise induced angina ~ 1 = Yes, 0 = No                                                      |
|  output           | Target variable                                                                                |


### DATA CLEANING AND DATA WRANGLING 

I import the data into jupyter notebook and then work on the EDA and realised that the dataset was fairly clean with no null values or duplicates with standardised column headers and therfore i proceeded to check for outliers and then removed them using IQRS
![newplot](https://user-images.githubusercontent.com/81169091/119006536-c404a500-b990-11eb-8b51-1cdf3cb77144.png)

### MACHINE LEARNING 
Here begins the Machine learning: 

I define the categorical and numerical columns so that I can label encode and scale them respectively.
NOTE :  even though my categorical columns are numbers, I still use One Hot Encoder as my Randomn Forest Acuracy Drops without this. * but the other two models were unharmed.

I use 3 Machine Learning Models:
1. Logistic Regression.
2. Randomn Forest.
3. Support Vector Machine.

I carried out a few iterations on these 3 Models:
- 1. Iteration 1: the scaling used is normalizer.
- 2. Iteration 2: We did Feature Selection using Boratpy
- 3. Itertaion 3: For Scaling - RobustScaler
- 4. Itertaion 4: Feature Selction with RobustScaler

 Here is the comparision of the models with each iterations:
 
 ![newplot (2)](https://user-images.githubusercontent.com/81169091/119009105-1777f280-b993-11eb-9507-5b118493184f.png)
 
### VALIDATION :

To validate the Models I used :
 - 1. Acuracy
 - 2. Kappa Score
 - 3. ROC/AUC
 - 4. F1 score
 - 5. R2 score
 
I choose the best model on the F1 score and visulaised the confusion matrix along with the Area under the curve.

### CONCLUSION :

My ideal Model is the Logistic Regression using Robust Scaler. 

- [X] AREA UNDER THE CURVE

![AUC_LR_RS](https://user-images.githubusercontent.com/81169091/119008602-9caed780-b992-11eb-8e5b-b1e9a7ecc576.png)

- [X] CONFUSION MATRIX 

![confucion matrix - LR_RS](https://user-images.githubusercontent.com/81169091/119008606-9d476e00-b992-11eb-9e48-f31c790b8375.png)

As you can see this model has predicted all the Heart disease outcomes better.
