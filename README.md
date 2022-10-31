# credit_risk_modeling - Purpose of the model is to calculate 'Expected Loss'

## Data source - https://www.kaggle.com/datasets/shawnysun/loan-data-for-credit-risk-modeling
1. Data to be used for training and validating the model - loan_data_2007_2014.csv
2. Data for monitoring the model - loan_data_2015.csv
3. Data Dictionary - LCDataDictionary.xlsx


PD model – Logistic Regression – determine the probability of borrower defaulting on the loan ('good_bad') <br>
LGD model – Logistic + Linear – Logistic to predict whether borrower will default or not ('recovery_rate_0_1') and linear to predict the percentage of money lost ('recovery_rate') <br>
EAD – Linear amount the is at risk once default has occurred ('CCF')

### (Expected Loss) EL = PD * LGD * EAD

### Example - 
1. Probability of default (%) – if 1 in 10 defaulted on the loan last year, then PD = 10%
2. Loss given default (%) – If borrower defaults, the loan remaining is 10K but the bank manages to sell the property for 8K. So, the remaining 2K divided by 10K is LGD i.e. 2/10 = 20%. (Percentage that cannot be recovered)
3. Exposure at default (Amount) – The 10K which the borrower was unable to pay, is EAD. EAD = 10K. (Debt left when the borrower defaulted)
4. Expected Loss = PD x LGD x EAD = 10% x 20% x 10K = 0.1*0.2*10000 = 200


### Order to run the .ipynb files
1. credit_risk_modelling_data_prep.ipynb
2. credit_risk_modelling_pd_model.ipynb
3. credit_risk_modelling_pd_monitoring.ipynb
4. credit_risk_modelling_lgd_ead_models.ipynb
5. credit_risk_modelling_expected_loss.ipynb
