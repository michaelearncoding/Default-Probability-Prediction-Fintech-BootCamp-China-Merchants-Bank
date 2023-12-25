# Default Probability Prediction-Fintech-BootCamp-China-Merchants-Bank

Hi, this is a ongoing project for further research on competition that held in Fintech Boostcamp by China Merchants Bank.

The data will not provided but the related training model would be present in here.

# `Project Summary`

Determine the likelihood of loan default for each customer, based on customer profile, historical transactions over
140,000 records in the last 60 days and digital activities in last 30 days, conduct data cleaning (impute missing value)
feature engineering, train model, parameter tuning using Python

Leverage machine learning algorithms including Xgboost and Gradient Boosting, output probability score and rank the
models based on accuracy and robustness


1. Data Pre-processing

Data preprocessing
The preprocessing part mainly consists of two operations: filling in missing values and field variable conversion.

Missing value filling: Only the tag table has missing values, so fill in the tag

- Guessed that “\N” was a missing value, and filled it directly with “\N”. After analysis, I found that the number of “\N” in multiple fields was basically the same (those who have done it should know, those five hundred users). If all are filled with “\N”, the proportion distribution of field values will be changed, so the final filling rule is:

deg_cd: Fill with ~ 

edu_deg_cd: Fill with ~  

acdm_deg_cd: Fill with “\N” 

atdd_type: Fill with “\N” 

- Field variable conversion

For categorical fields, such as education, degree, gender, identification, etc., use labelencoder encoding method; For level codes and continuous fields, such as card holding days, books, risk tolerance level, etc., convert “\N” to 0 or -1 (the same idea as filling in missing values, ensuring that the proportion of those five hundred users remains unchanged after conversion), and convert the field type to integer. 

- Other

Unify 0 and 0.0 in atdd_type to 0, and 1 and 1.0 to 1. The time fields in the trd table and the beh table are sorted out, and the year, month, day, hour, week, and whether it is a weekend are extracted, which is convenient for extracting user features by time dimension later.




