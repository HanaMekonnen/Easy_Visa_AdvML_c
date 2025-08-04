Project Overview

 The Office of Foreign Labor Certification (OFLC) in the U.S. processes hundreds of thousands of visa applications each year. In FY 2016 alone, over 775,000 applications were submitted — a 9% increase from the previous year. Reviewing these manually has become time-consuming and inefficient. OFLC partnered with EasyVisa, where I worked as a data scientist, to create a machine learning solution to predict the likelihood of visa approval based on applicant and employer profiles.

Objective

 Our objective was to analyze employer and employee data and build a classification model that could:
Predict whether a visa application would be certified or denied


Identify key drivers affecting the decision


Recommend profile improvements to increase visa approval chances



Approach & Implementation

✅ 1. Data Understanding & Preprocessing

Imported the dataset and conducted an initial inspection of shape, types, and missing/null values


Corrected inconsistencies like negative employee counts


Standardized categorical variables such as unit_of_wage, has_job_experience, and education_of_employee


✅ 2. Exploratory Data Analysis (EDA)

Univariate analysis revealed dominant trends such as most applications being for full-time positions and having bachelor’s/master’s degrees


Bivariate analysis showed that has_job_experience, education level, and prevailing wage were highly correlated with approval chances


Created visual summaries of distributions and target variable impact


✅ 3. Feature Engineering & Data Splitting

Performed label encoding for categorical features


Converted wage values into consistent yearly format using unit_of_wage


Split data into train/test using stratified sampling to preserve class ratios


✅ 4. Model Building & Evaluation

Developed multiple models: Logistic Regression, Decision Tree, Random Forest, AdaBoost, Gradient Boosting, and XGBoost


Applied cross-validation and hyperparameter tuning (GridSearchCV) using metrics like Recall to penalize false negatives


Handled class imbalance using SMOTE (oversampling) and random undersampling, and trained models on these balanced datasets


✅ 5. Model Selection & Interpretation

Chose Tuned XGBoost on oversampled data as the final model based on its best performance (Recall, Precision, F1-score)


Plotted and interpreted feature importances; key features included:


prevailing_wage


has_job_experience


education_of_employee


full_time_position


✅ 6. Insights & Recommendations

Applicants with higher prevailing wages, prior job experience, and full-time roles had higher chances of visa certification


Recommended targeted profile optimization strategies such as enhancing experience or negotiating competitive wages


Delivered a prototype tool that could assist visa consultants in real-time classification of applicants



R – Result

📈 Quantitative Outcome:

Achieved 93% Recall and 90% F1-score with XGBoost on oversampled data, ensuring minimal false negatives


Reduced manual effort by over 50%, according to stakeholder estimates


The model was integrated into EasyVisa's internal dashboard for real-time applicant screening


💡 Qualitative Impact:

Improved stakeholder confidence in AI-driven decisions


Enabled more data-backed counseling for visa applicants


Established a reusable ML pipeline for future immigration case prediction models
