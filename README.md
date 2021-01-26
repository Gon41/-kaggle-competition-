## -Diamonts-Kaggle-Competition-

![](https://img.huffingtonpost.com/asset/5c8a48a1360000c81a6b466e.jpeg?ops=scalefit_630_noupscale)
______

# 1. **Objective**.

With Machine Learning techniques to obtain the prediction of the diamond price.

We have the train.csv that we must clean, investigate and from it train a predictive model trying to lower the score as low as possible. For this we use the second file (predict.csv).

----
# 2. **Methodology

## 2.1. Cleanup

There was not much to clean up in the dataset, since there was no null or duplicate data. Reviewing the columns there are three categorical columns that we will discuss later.

Studying the correlation and looking at the "price" column, the rows "carat", "x", "y" and "z" are highly correlated with "price".
From them we see that between "x", "y" and "z" there is too much correlation, which indicates that there is likely to be collinearity.
As "x" has a higher correlation with "price" I decide to leave it and eliminate "y" and "z".

I convert the categorical columns to numerical with the 'dummy' method.

## 2.2. Choice of model

I have tried the following models:

    - LinearRegression()
    - DecisionTreeRegressor()
    - RandomForestRegressorr()

Each of them gave me less distortion in the price and the difference is 600-700€.

------
