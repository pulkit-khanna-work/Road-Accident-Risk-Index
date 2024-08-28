We know our data is heavily unbalanced, so we will be using sampling techniques first to balance out our classes.

Rather than using a single technique i.e. oversampling or undersampling, it is better to use a combination of oversampling and undersampling to achieve better results. We will demonstrate how to perform combination of oversampling and downsampling using 'imblearn' library to balance out our classes. We will use 'SMOTETomek' combination method which uses SMOTE for over-sampling and Tomek links for cleaning.

We can also use sklearn resample to balance out our classes, however we should note that SMOTE method creates synthetic(new) data points. Also, 'Random Undersampling', although simple and effective, has the drawback of removing data points without any concern for how useful or important they might be in determining the decision boundary between the classes. 'TomekLinks', 'Edited Nearest Neighbours' help in overcoming this drawback.

Next we will demonstrate now how to use LightGBM algorithm for building, training and evaluating our model. Building LGBM is faster than XGBoost model and thus preferred initially to get a baseline model for tree based algorithms and in some in cases in general. We can try differnt transformations, encodings, feature engineerig methods etc and then quickly build models using LGBM and evaluate them, thus saving us time.

We will show how to build a multi-class classification model using LGBM and thus will be building 2 models:

A Baseline LGBM

A lightly tuned version of 'Baseline LGBM' by optimizing its 2 hyperparamters ('number of estimartors/trees' and 'learning rate') using grid search. Other hyperparamters can be fine tuned in a similar way as we did with XGBoost for our 'Predicintg Seasons Model'.

Note 1: We can also use lightgbm regressor for training and evaluating our model, however since our output is discrete in nature with only 5 values, lightgbm classifier would be the preferred method. Also, with lightgbm regressor we would be more intereted in its distribution and might have use transformation, resampling techniques, tweedie regressor(weighted regression) to balanced out our data.

Note 2: Optuna is another library useful for the same and gives better results in more efficient way.

Note 3: We should first focus on feature engineering and trying other models first to check for improvement in score and then fine tune.
