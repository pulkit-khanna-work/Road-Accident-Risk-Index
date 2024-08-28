# Road Accident Risk Index

This is a regression problem. The problem stated is a realistic one where the aim is to predict the 'Accident Risk Index' against the postcode on the test data which is given by: Accident Risk Index (mean casualties at a postcode) = sum (Number of casualities)/count(Accident_ID))

The dataset was provided by Tredence. It has 484042 rows and 27 columns.

This can be useful for insurance firms as in order to pre-emptively plan for the losses, they can leverage accident data to understand the risk across the geographical units e.g. Postal code/district etc.

The chosen metric for assessing/evaluating performance of the model is mean squared error.

The analysis is divided into 2 sections: 

1) Wrangle: Here we will prepare the data starting with checkcing data integrity, treating missing values, exploratory data analysis, framing hypothesis and ANOVA testing, feature engineering, feature transformation, encoding etc.

2) Modelling: This section is further divided into 3 parts. Here we will demonstrate how to train and build a LGBM, Poisson GAM and also demonstrate usage of H2O library with Auto ML model building function.

Additional Info: We can try following methods which might further improve our scores:-

    Build model to handle missing values by predicting their values
    Feature Engineering (Create new features from given ones such as mean, deviations, interactions, etc)
    Try using other upsampling/downsampling techniques such as ADASYN, ENN etc to handle unbalanced classes    
    Use Optuna library to tune the hyperparameters efficiently
    
Note 1: The training dataset is too large in size to be loaded in github. Here I have shared my google drive link and will use gdown to directly download the file from there.

Note 2: The saved wrangled dataset loading from the '.ipnyb' follows the same directory structure as here on github. You can either create and save those files from 'Accident_Risk_Index_Wrangle.ipynb' file or download it using the link given in modelling folder 'readme.md' file
