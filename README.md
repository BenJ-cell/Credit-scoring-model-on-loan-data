# Credit-scoring-model-on-loan-data

Develop a credit scoring model that can assess the creditworthiness of borrowers based on a range of factors.

Subjects tackled: Imbalanced Dataset, Data Visualization, Imputing missing nominal and numerical input variables, GridSearch for fine-tuning hyperparameters, Feature Transformation/Engineering, Feature selection - Pearson Correlation Factor Pearson, Chi Square Test, f_regression, f_classif. Then to focus more on recall or accuracy we can use the predicted probabilities of a loan being default instead of a binary variable and vary the threshold of decision to choose between the two classes. We have a trade-off between recall and accuracy performances. For example a good model in both metrics was CatBoost with no feature selection as CatBoost already implement it giving us 90% recall and 91% accuracy with a threshold of 0.1.

Features selection was interesting for logistic regression that does not do it itself.

To evaluate the various features selection strategies, we use four models: Logistic Regression, Decision Trees, LightGBM, CatBoost classifiers.

We can visualize the various results below:

Feature Selection Method,Model,Accuracy Score,F1 Score,Precision Score,Recall Score
None,CatBoost,0.9176410777834265,0.8622977598008712,0.9058525128987636,0.832385296781462
None,Decision Tree,0.8251143873919674,0.7665816678533384,0.7456372563703171,0.8105381165919283
None,LightGBM,0.9161159125571937,0.8607949683657096,0.8997238656537325,0.8332468134926772
None,Logistic Regression,0.6822572445348246,0.6173734177116698,0.619531414254678,0.6722370717267887
Pearson corr_fact,CatBoost,0.9018810371123538,0.8350567109187799,0.8786027146989588,0.8060538116591929
Pearson corr_fact,Decision Tree,0.8703609557702084,0.8084943102095514,0.7994532920969529,0.818998652499503
Pearson corr_fact,LightGBM,0.8896797153024911,0.814947959952987,0.8548278111747984,0.7883430161920961
Pearson corr_fact,Logistic Regression,0.6842907981698018,0.6232039052077147,0.6262642983212159,0.6835417172899777
chi2 test,CatBoost,0.9089984748347738,0.8483372983515776,0.8884160214128669,0.8205615321743356
chi2 test,Decision Tree,0.8576512455516014,0.7884510790239466,0.7814247149132005,0.7964114515452075
chi2 test,LightGBM,0.8993390950686324,0.8324185470129601,0.8701624006926248,0.8062747133800172
chi2 test,Logistic Regression,0.6832740213523132,0.6201225400161505,0.6226468907328395,0.6774337847091829
f_classif,CatBoost,0.9054397559735639,0.8408659115820241,0.8857745629897529,0.8110296229207625
f_classif,Decision Tree,0.8408744280630401,0.7810795770728993,0.7611942348905305,0.8150003313525813
f_classif,LightGBM,0.9008642602948653,0.832983754489842,0.8775469958007928,0.8035907574720007
f_classif,Logistic Regression,0.6959837315709202,0.6318471584777443,0.6313454040837904,0.6881751308842696
f_regression,CatBoost,0.9054397559735639,0.8408659115820241,0.8857745629897529,0.8110296229207625
f_regression,Decision Tree,0.8530757498729029,0.7886513442240435,0.7747156765909411,0.8071969780644591
f_regression,LightGBM,0.9008642602948653,0.832983754489842,0.8775469958007928,0.8035907574720007
f_regression,Logistic Regression,0.7076766649720386,0.6436069831320488,0.6406747792518969,0.7000983012657669
