# DAC_AIRQ
code:
# importing Randomforest
From sklearn.ensemble import AdaBoostRegressor
From sklearn.ensemble import RandomForestRegressor
# creating modelM1 = RandomForestRegressor()
# separating class label and other attributes
Train1 = train.drop([‘air_quality_index’], axis=1)
Target = train[‘air_quality_index’]
# Fitting the model
M1.fit(train1, target)‘’’
RandomForestRegressor(bootstrap=True, ccp_alpha=0.0, criterion=’mse’,Max_depth=None, max_features=’auto’, max_leaf_nodes=None,Max_samples=None, min_impurity_decrease=0.0,Min_impurity_split=None, min_samples_leaf=1,Min_samples_split=2, min_weight_fraction_leaf=0.0, N_estimators=100, n_jobs=None, oob_score=False,
Random_state=None, verbose=0, warm_start=False)’’’
# calculating the score and the score is 97.96360799890066%M1.score(train1, target) * 100
# predicting the model with other values (testing the data)
# so AQI is 123.71M1.predict([[123, 45, 67, 34, 5, 0, 23]])
# Adaboost model# importing module# defining model
M2 = AdaBoostRegressor()
# Fitting the modelM2.fit(train1, target)‘’’
AdaBoostRegressor(base_estimator=None, learning_rate=1.0, loss=’linear’,
N_estimators=50, random_state=None)’’’
# calculating the score and the score is 96.15377360010211%
M2.score(train1, target)*100
# predicting the model with other values (testing the data)
# so AQI is 94.42105263
M2.predict([[123, 45, 67, 34, 5, 0, 23]])
