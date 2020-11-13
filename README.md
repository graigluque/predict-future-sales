# Predict future sales 

This is the final project for [Coursera online course: "How to Win a Data Science Competition: Learn from Top Kagglers"](https://www.coursera.org/learn/competitive-data-science/). It is also a public challenge on the [Kaggle](https://www.kaggle.com/c/competitive-data-science-predict-future-sales) platform.


If you run into any trouble with the setup/code or have any questions please contact me at [graig.luque@gmail.com](mailto:graig.luque@gmail.com).


### Goal

In this competition you will work with a challenging time-series dataset consisting of daily sales data, kindly provided by one of the largest Russian software firms - [1C Company](http://1c.ru/eng/title.htm). We are asking you to predict total sales for every product and store in the next month. By solving this competition you will be able to apply and enhance your data science skills.


### Feature Engineering

The feature engineering part is built on the notebook by [Denis Larionov: feature engineering, xgboost](https://www.kaggle.com/dlarionov/feature-engineering-xgboost), with optimization on the code of lag features and trend features.

This solution I liked because it keeps low RAM consume that with other solutions I had problem with memeory error rises. Fortheremore using xgboost is used because generate a better LB score compared with other solutions like ensampling and NN that I had tested with performance issues in my notebook.


### Score

The public and private LB scores are: 0.919899 and 0.923187.

The solution is good already, but can be improvement.


### Archive Content

kaggle_model.zip: contains original code, notebook file, input files, submission file, this readme file


### Hardward

This solution was run on a Kaggle Jupyter Notebook with 4 CPU cores, 16 GB RAM and 20 GB disk.


### Software

Python 3.7.6

Python packages:
numpy 1.18.5
pandas 1.1.3
seaborn 0.10.0
sklearn 0.23.2
xgboost 1.2.1


### Model Build

Very fast prediction without memory issues:

    1) runs in almost an hour with a commodity hardware.
    
    2) uses distributed gradient boosting for predictions.
    
    3) configure input files path before run notebook.
    
    4) run [predicting-future-sales-xgboost.ipynb] notebook.
    
    5) get submission file in [$output_dir/xgb-submission.csv].


### Next Steps

To improve the score result need to divide in steps, first run EDA and feature engineering and then run single model training for LGBMRegressor, XGBRegressor and multilayer neural network, and then use weighted average and linear regression for ensampling.
