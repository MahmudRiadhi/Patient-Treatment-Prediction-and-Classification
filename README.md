# Patient Treatment Prediction and Classification_Supervised Machine Learning

The dataset is contains the patients laboratory test results used to determine next patient treatment whether in care or out care patient.

In hospitals, medical treatments and surgeries can be categorized into inpatient and outpatient procedures.
For patients, it is important to understand the difference between these two types of care, because they impact the length of a patient’s stay in a medical facility and the cost of a procedure. The difference between an inpatient and outpatient care is how long a patient must remain in the facility where they have the procedure done.

Inpatient care requires overnight hospitalization. Patients must stay at the medical facility where their procedure was done (which is usually a hospital) for at least one night. During this time, they remain under the supervision of a nurse or doctor.

Patients receiving outpatient care do not need to spend a night in a hospital. They are free to leave the hospital once the procedure is over. In some exceptional cases, they need to wait while anesthesia wears off or to make sure there are not any complications. As long as there are not any serious complications, patients do not have to spend the night being supervised.
[source of information: pbmhealth]

# Problem Statement
In today’s world of automation, the skills and knowledge of a person could be utilized at the best places possible by automating tasks wherever possible. As a part of the hospital automation system, one can build a system that would predict and estimate whether the patient should be categorized as an incare patient or an outcare patient with the help of several data points about the patients, their conditions and lab tests.

# Objective Statement
Build a machine learning model to predict if the patient should be classified as in care or out care based on the patient's laboratory test result.

The process to do with this project are :
1. Import libraries and load the data
2. Data cleansing (missing value and duplicate rows handling), Exploratory data analysis (EDA) which consists of preliminary look at the data, and data deep-dive understanding (statistical summary, univariate analysis, multivariate analysis)
3. Machine Learning Solution (binary classification task, performance metrics by precision, recall and accuracy)
4. Expected Outcome (conclusions and recommendations)

# Data Understanding
- The dataset is Electronic Health Record Predicting collected from a private Hospital in Indonesia
- Source data : Sadikin, Mujiono (2020), “EHR Dataset for Patient Treatment Classification”, Mendeley Data, V1, doi: 10.17632/7kv3rctx7m.1 https://www.kaggle.com/datasets/saurabhshahane/patient-treatment-classification
- The dataset has 11 columns and 4412 rows
- Dataset Attribute information :
  - HAEMATOCRIT : Patient laboratory test result of haematocrit
  - HAEMOGLOBINS : Patient laboratory test result of haemoglobins
  - ERYTHROCYTE : Patient laboratory test result of erythrocyte
  - LEUCOCYTE : Patient laboratory test result of leucocyte
  - THROMBOCYTE : Patient laboratory test result of thrombocyte
  - MCH : Patient laboratory test result of MCH
  - MCHC : Patient laboratory test result of MCHC
  - MCV : Patient laboratory test result of MCV
  - AGE : Patient age
  - SEX : Patient gender
  - SOURCE : Target ( Binary : in / out )
- The dataset is made up of 3 data types; float, integer and object
- All dtypes are appropriate, given the appropriate column names

# Data Cleansing
- The data does not contain major issues. There are no NaN values and duplicated rows

# Exploratory data analysis (EDA)
- Statistical Summary :
  - The minimum and maximum values make sense for each column
  - All column, except column LUECOCYTE has a symmetrical distribution
  - The LEUCOCYTE columns show a skew distribution, because mean > median
- Univariate Analysis and Multivariate Analysis :
  - Outlier Handling 
  - See all column has a symmetrical distribution
  - Multicolinearity Handling

# Machine Learning Solution
- In EDA, we found out that many features are not very useful in predicting the target. Let's remove those features
- Modeling & Evaluating data : K-NN Classification
- Modeling & Evaluating data : Random Forest Classifier

# Recommendations
- The Best algorithm is random forest classifier
