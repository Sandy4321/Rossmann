# Rossmann Store Sales Kaggle Competition
This is a brief summary of my approach to solving the Rossmann Store Sales Kaggle Competition. The competition details can be found [here] (https://www.kaggle.com/c/rossmann-store-sales). My final rank was 1331 of 3303.

The final submission was generated by taking the arithmetic average of 16 different extreme gradient boosting models with varying learning rates, number of trees, max depth, and subsample ratios. This was done in an effort to try to reduce the variance. I spent quite a bit of time trying to create a robust time series model, but in the end it could not beat the XGB decision tree model. I also tried creating a dead simple model weight average model (similar to what James King did for the [Walmart Store Sales Forecasting] (https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/forums/t/8023/thank-you-and-2-rank-model) competition), but, again, it faired much worse than the XGB model on the leaderboard. In terms of feature engineering, very little was done besides cleaning up the data, converting variable types and breaking up the date column.  If I could go back and change a couple things, I would have concentrated more effort on feature engineering as well as performed a variable importance analysis to remove unimportant and redundant features. I also should have removed the last 6 weeks of the *training set* as a holdout set with which I could perform cross validation to address my problem with overfitting.
