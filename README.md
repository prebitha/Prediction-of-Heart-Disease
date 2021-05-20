# Prediction of Heart Disease

Heart disease is one of the leading cause of death in the Unites States. The Dataset I have used is available in the UCI, Machine Learning Repository (This is also available in Kaggle). 

First I did my Study on the Dataset using Tableau [ tableau link here ](https://public.tableau.com/profile/prebitha.staphney.abraham#!/vizhome/HeartDiseaseDatasetStudy/cardiaccatheterization?publish=yes)

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


### MACHINE LEARNING 

I import the data into jupyter notebook and then work on the EDA and realised that the dataset was fairly clean with no null values or duplicates with standardised column headers and therfore i proceeded to check for outliers and then removed them using IQRS
![newplot](https://user-images.githubusercontent.com/81169091/119006536-c404a500-b990-11eb-8b51-1cdf3cb77144.png)


