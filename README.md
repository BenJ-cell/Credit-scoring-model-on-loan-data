# Credit-scoring-model-on-loan-data

Develop a credit scoring model that can assess the creditworthiness of borrowers based on a range of factors.

Subjects tackled: Imbalanced Dataset, Data Visualization, Imputing missing nominal and numerical input variables, GridSearch for fine-tuning hyperparameters, Feature Transformation/Engineering, Feature selection - Pearson Correlation Factor Pearson, Chi Square Test, f_regression, f_classif. Then to focus more on recall or accuracy we can use the predicted probabilities of a loan being default instead of a binary variable and vary the threshold of decision to choose between the two classes. We have a trade-off between recall and accuracy performances. For example a good model in both metrics was CatBoost with no feature selection as CatBoost already implement it giving us 90% recall and 91% accuracy with a threshold of 0.1.

Features selection was interesting for logistic regression that does not do it itself.

To evaluate the various features selection strategies, we use four models: Logistic Regression, Decision Trees, LightGBM, CatBoost classifiers.

We can visualize the various results below:

Feature Selection Method, Model,  Accuracy Score, F1 Score, Precision Score,  Recall Score
------------------------------------------------------------------------------------------
None, CatBoost, 0.92, 0.86, 0.91, 0.83

None, Decision Tree,  0.83, 0.77, 0.75, 0.81

None, LightGBM, 0.92, 0.86, 0.90, 0.83

None, Logistic Regression,  0.68, 0.62, 0.62,  0.67

Pearson corr_fact,  CatBoost, 0.90, 0.84, 0.88, 0.81

Pearson corr_fact,  Decision Tree,  0.87, 0.81, 0.80, 0.82

Pearson corr_fact,  LightGBM, 0.89, 0.82,  0.86, 0.79

Pearson corr_fact,  Logistic Regression,  0.68, 0.62, 0.63, 0.68

chi2 test,  CatBoost, 0.91, 0.85, 0.89, 0.82

chi2 test,  Decision Tree,  0.86, 0.79, 0.78, 0.80

chi2 test,  LightGBM, 0.90, 0.83, 0.87, 0.81

chi2 test,  Logistic Regression,  0.68, 0.62, 0.62, 0.68

f_classif,  CatBoost, 0.91, 0.84, 0.89, 0.81

f_classif,  Decision Tree,  0.84, 0.78, 0.76, 0.82

f_classif,  LightGBM, 0.90, 0.83,  0.88, 0.80

f_classif,  Logistic Regression,  0.70, 0.63, 0.63, 0.69

f_regression, CatBoost, 0.91, 0.84, 0.89, 0.81

f_regression, Decision Tree,  0.85, 0.79, 0.78, 0.81

f_regression, LightGBM, 0.90, 0.83,  0.88, 0.80

f_regression, Logistic Regression,  0.71, 0.64, 0.64, 0.70

