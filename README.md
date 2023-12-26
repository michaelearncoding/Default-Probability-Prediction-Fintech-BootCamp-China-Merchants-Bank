# Default Probability Prediction-Fintech-BootCamp-China-Merchants-Bank

Hi, this is a ongoing project for further research on competition that held in Fintech Boostcamp by China Merchants Bank.

The data will not provided but the related training model would be present in here.

# `Project Summary`

Determine the likelihood of loan default for each customer, based on customer profile, historical transactions over
140,000 records in the last 60 days and digital activities in last 30 days, conduct data cleaning (impute missing value)
feature engineering, train model, parameter tuning using Python

Leverage machine learning algorithms including Xgboost and Gradient Boosting, output probability score and rank the
models based on accuracy and robustness


# `Code description`


0_0preprocessing_tag.py: tag table preprocessing 

0_1preprocessing_trd.py: trd table 

preprocessing 1_0trd_id_feature.py: feature extraction from trd table (by id) 1_1trd_time_feature.py: feature extraction from trd table (by id and time period)

1_2trd_R_feature.py: R-type feature extraction from trd table 

2_0lgb.py: single model lightgbm, five-fold cross-validation training 

2_1xgb.py: single model xgboost, five-fold cross-validation training 

3_0model_stack.py: model fusion, get the final result 

parameter.py: path parameter file method.py: common function methods 

run.py: one-click execution of pipeline, preprocessing, feature extraction, model training and fusion, from raw data to final result. 

Environment and dependent libraries Python 3.5.4 Pandas 0.25.3 Numpy 1.17.0 Sklearn 0.21.3 Lightgbm 2.2.3 Xgboost 0.81

Path description 


├─Final_code: py code file

└─data

​ ├─RawData: original csv file (including training set and test set)

​ ├─TempData: preprocessing file

​ ├─EtlData: feature file

​ └─Result: generate the final result submission.csv




