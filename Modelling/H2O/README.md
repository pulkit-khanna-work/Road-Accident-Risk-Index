Here we will demonstrate how to use H2O library for training and building our models. Also, we will be building training and evaluation plots to better understand the data.

We will be building different regression model using H2O AutoML. The response variable needs to be of numeric type when using Auto ML for building regression models. They will build much faster and take lesser memory than multi-class classification models.

Through evalutaion plots (including SHAP plots) we will also determine our most important explanatory variables.

Note 1: H2O also provides us the ability to build GLM and GAM models. Here for our case, we can use a 'Multibinomial GLM' or a 'Poisson GAM' depending on the assumptions that need to be satisified for building such models.

Note 2: To use classification model we need to convert our response variable type to categorical/enum.

Note 3: For multi-class classification problems, H2O(ver 3.36) won't be building stacked enemble models.
