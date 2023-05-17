# Length-of-stay-of-patients
In the past, our focus was on determining the likelihood of patients' mortality, but our current aim is to forecast the duration of their hospital stay.<br>

## Instructions:
In this project, I have to predict the length of stay (in days) of a patient that is entering an ICU (Intensive Care Unit) using decision tree and ensemble models.

The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.<br>

Each row of *mimic_train.csv* correponds to one ICU stay (*hadm_id*+*icustay_id*) of one patient (*subject_id*). Column *LOS* is the length of stay of this patient, equal to discharge time minus admit time.<br>
The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at *mimic_patient_metadata.csv*.<br>
Please don't use any feature that you infer you don't know the first day of a patient in an ICU.<br>

Note that the main cause/disease of patient contidition is embedded as a code at *ICD9_diagnosis* column. The meaning of this code can be found at *MIMIC_metadata_diagnose.csv*. **But** this is only the main one; a patient can have co-occurrent diseases (comorbidities). These secondary codes can be found at *extra_data/MIMIC_diagnoses.csv*.<br>

Don't use features that you don't know the first day a patient enters the ICU, such as *HOSPITAL_EXPIRE_FLAG*<br>

As performance metric, please use *RMSE* (root mean squared error).<br>

## Main tasks:
+ Using *mimic_train.csv* file build a predictive model for *LOS* .
+ For this analysis there is an extra test dataset, *mimic_test_los.csv*. Apply your final model to this extra dataset and generate predictions following the same format as *mimic_kaggle_los_sample_submission.csv*. Once ready, you can submit to our Kaggle competition and iterate to improve the accuracy.

As a *bonus*, try different decision trees algorithms, even combine with other prediction models.  Try to assess which features are more important, and if possible the confidence interval of predictions.

You can follow those **steps** in your first implementation:
1. *Explore* and understand the dataset. 
2. Manage missing data.
2. Manage categorical features. E.g. create *dummy variables* for relevant categorical features, or build an ad hoc distance function.
3. Build a prediction model
5. Assess expected accuracy  of previous models using *cross-validation*. 
6. Predict on the test file, following same preparation steps (missing data, dummies, etc). Remember that you should be able to yield a prediction for all the rows of the test dataset. Submit to Kaggle to check performance.

Data
+ Code runs        5% - That your code runs and you are using sklearn (and beyond) correctly
+ Data preparation        5% - That you know how to preprocess the data before applying the models

Decision trees
+ Decision trees method(s) have been used        10% - That you have fit at least one decision tree method and you understand which arguments you can consider for tuning
+ Hyperparameter optimization        10% - That you understand how to use a GridSearch to tune/regularise your Decision Tree parameters

Ensembles 
+ Ensemble method(s) have been used    10% - That you have fit at least one ensemble model and you understand which arguments you can consider tuning
+ Complexity of ensemble used   10% - How advanced was your ensemble? Did it include more than tree models? How did the ensemble learn to combine the models?

Neural Networks
+ Neural Networks method(s) have been used    10% - That you have fit at least one Neural Network model and you understand how to diagnose convergence of your model training
+ Complexity of Neural Network   10% - How advanced was your Neural Network? What types of regularisation did you consider?

Other
+ Length of stay is predicted for each test patient   5% - That you submitted out-of-sample predictions to kaggle and received a score

+ Accuracy of you best predictions   10% - The Kaggle score for your best model
+ Attempts made to interpret predictions   5% - That you attempted to interpret your ensemble or Neural Network predictions using LIME or SHAP
+ Neat and understandable code, with some titles and comments        5% - Comments showing good understanding of why you do what you do and how the output is interpreted
+ Improved methods from what we discussed in class (properly explained/justified)        5% - Methods used beyond those shown in class, this could involve further preprocessing steps than seen in class, and extensions to the models.
