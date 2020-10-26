# Virality-Predictor

Built a model that can predict virality of a new article being posted on the platform so that the news feed product can use the model to showcase new articles.

•	The features considered for to develop the model include number of bookmarks, comments created, follow, likes and views for given posts. The correlation of different features with target were analyzed. Since the number of features are smaller in number, there wasn't a need to compress the features.

•	Different models including linear regression(without regularization), lasso regression, k-fold elastic regression were tested on a test dataset with 20% split of data. The linear regression gave a 100% of training and testing accuracy, 100% of r-squared and explained variance metric. The model was doubted to overfit the data and hence other regularization methods were used as lasso (99% of r-squared and explained variance), k-fold elastic CV (61% of r-squared and explained variance) with 3-fold cross validation. The lasso model is the most generalizable among all the tested models

•	The data was preprocessed using Pandas to get count of features as like, follow, etc. for the posts and generate labels using given function of 1 * VIEW + 4 * LIKE + 10 * COMMENT + 25 * FOLLOW + 100 * BOOKMARK. The data was split into 80-20 (train, test). Evaluation metrics used were testing accuracy, r-squared/explained variance.
