# Beer Popularity Score Analysis based on Sensory Features

# 1. Introduction

This R&D project is based on a dataset that contains product feature about 310 beer and sensory preference data from 10 customers. The complete dataset is from a food company in Canada, and it has been modified. 

# 2. Objectives

* Analyze key features influencing the rating score of 310 beer.
* Predict the liking score based on the features of the beer and panel's preference.
* Research the relationship between certain features.
* Conduct the clustering analysis to segment different beer.

# 3. Data Preparation

After data cleansing and merging, the original dataset of 10k records is converted to a final dataset of 878 rows and 53 columns.

![data_prep](https://user-images.githubusercontent.com/64850893/115800818-5cffca80-a3a9-11eb-8a45-77e521f6caa1.png)

# 4. Cluster Analysis

Segment the beer into 6 classes using Kmeans and silhouette score.

![cluster_pca](https://user-images.githubusercontent.com/64850893/115801124-00e97600-a3aa-11eb-82a7-1abcc262548c.png)

* The PC1 is impacted heavily by “Body", “Length of Aftertaste", “Intensity of Flavour" and “Bitterness", while the PC2 is mostly influenced by fruit related features and “Cereal”.

* There is a significant positive correlation between “Intensity of Flavour” and “Length of Aftertaste”, since the related axes are close.


# 5. Product Innovation Score

Calculate the cosine similarity between a product and its 10 nearest neighbors, and converted the probability to an Innovation score (from 0 to 100).

![product_location2](https://user-images.githubusercontent.com/64850893/115801461-d21fcf80-a3aa-11eb-94c6-5a0b654937e1.png)


* The beer 718 has a higher innovation score, which can also be shown in the plot, since the distance between it (in red) and its neighbors is longer than that of the beer 268 (in green).

* It is possible that the innovative features of the beer 718 is one of the reasons why it is more popular than the beer 268.

# 6. Data Modeling
Executed data modeling with various regression models.

* Lasso outperforms other models, in terms of the R square and RMSE.

# 7. Future work
In the future investigation, I will attempt to conduct feature engineering. Additionally, more machine learning models with different parameters would be implemented.

* Dig deeper regarding the relationship between various features.
* Experimented various feature engineering methods.
* Executed more ML models and hyperparameter tunining.
