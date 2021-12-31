# Predict Future Sales
This repository contains my final project of an online course "How to Win a Data Science Competition: Learn from Top Kagglers" 
[(Coursera)](https://www.coursera.org/learn/language-processing)
organized by National Research University Higher School of Economics [(HSE)](https://www.hse.ru/). The project 
works with a challenging time-series dataset consisting of daily sales data, kindly provided by one of the largest Russian software firms - 
[1C Company](https://1c.ru/eng/title.htm) to predict total sales for every product and store in the next month. The competition is hosted
on [Kaggle platform](https://www.kaggle.com/c/competitive-data-science-predict-future-sales/).

## Overview
The task is to forecast the total amount of products sold in every shop for the test set. 

## Architecture
* STEP 1 : Perform target encoding and create some [lag-based](https://en.wikipedia.org/wiki/Lag_operator) features
* STEP 2 : Tune hyper parameters of gradient boosted trees [(LightGBM)](https://lightgbm.readthedocs.io/en/latest/)
* STEP 3 : Ensembling with simple averaging of linear model and gradient boosted trees and use stacking
* STEP 4 : Produce the final submit file

## Dataset
* sales_train.csv - the training set. Daily historical data from January 2013 to October 2015.
* test.csv - the test set. You need to forecast the sales for these shops and products for November 2015.
* sample_submission.csv - a sample submission file in the correct format.
* items.csv - supplemental information about the items/products.
* item_categories.csv  - supplemental information about the items categories.
* shops.csv- supplemental information about the shops.

## Results
The final solution is optimized for root-mean-square error (RMSE).
<table>
  <tr>
    <th>  </th>
    <th> Public Score </th>
  </tr>
  <tr>
    <td> My result </td>
    <td> 0.94099 </td>
  </tr> 
  <tr>
    <td> Top 1 Kaggle </td>
    <td> 0.75368 </td>
  </tr>
</table>

## Repository Files:
* EDA.ipynb : Exploratory data analysis on the data set
* DataProcess.ipynb : Feature engineering
* Model.ipynb : Stacking of linear model and gradient boosted trees

## References
* https://www.coursera.org/learn/competitive-data-science
* https://www.kaggle.com/c/competitive-data-science-predict-future-sales/
* https://lightgbm.readthedocs.io/en/latest/