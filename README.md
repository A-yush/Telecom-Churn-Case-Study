# Telecom Churn
> Building ML models to predict churn and uplaoding output to kaggle competition.

## Table of Contents
* [Problem Statement](#problem-statement)
* [Objectives](#objectives)
* [Data](#data)
* [Algorithms Used](#algorithms-used)
* [Conclusion](#conclusion)
* [Feature Importance](#feature-importance)
* [Recommendations](#recommendations)
* [Model Evaluation](#model-evaluation)
* [References](#references)
* [Technologies Used](#technologies-used)
* [Contact](#contact)

## Problem Statement
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business
goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyze customer-level data of a leading telecom firm, and build predictive models to identify customers at high risk of churn.

Goal is to build a machine learning model that is able to predict churning customers based on the features provided for their usage.

## Objectives
The main goal of the case study is to build ML models to predict churn. The predictive model that you’re going to build will the following purposes:

1. It will be used to predict whether a high-value customer will churn or not, in near future (i.e. churn phase). By knowing this, the company can take action steps such as providing special plans, discounts on recharge etc.

2. It will be used to identify important variables that are strong predictors of churn. These variables may also indicate why customers choose to switch to other networks.

3. Even though overall accuracy will be your primary evaluation metric, you should also mention other metrics like precision, recall, etc. for the different models that can be used for evaluation purposes based on different business objectives. For example, in this problem statement, one business goal can be to build an ML model that identifies customers who'll definitely churn with more accuracy as compared to the ones who'll not churn. Make sure you mention which metric can be used in such scenarios.

4. Recommend strategies to manage customer churn based on your observations.

## Data
The data consists of 4 files:
1. train.csv - the training set
2. test.csv - the test set
3. sample_submission.csv - a sample submission file in the correct format
4. metaData.csv - supplemental information about the data

Target column is "churn_probability" which denotes 1 for customer who churned and 0 for customer who didn't churn. See references section to get Data download link.

Distribution of customers who churned vs not churned:

![Data-Visualization](https://github.com/A-yush/Telecom-Churn-Case-Study/blob/master/images/churn-prob.png)

## Algorithms used
1. PCA for removing collinearity and reducing complexity of model.
2. Logistic Regression with PCA and regularization.
3. Decision tree with PCA.
4. Random Forest with PCA.
5. Gradient Boosting with PCA.
6. XG Boost with PCA.

### Conclusion
1. The most important features are as shown in above graph.
2. Top 5 important features are roam_ic_mou_8, roam_og_mou_8, amt_data_8, total_ic_mou_8,loc_ic_mou_8 so basically maximum columns are of August Month.
3. Only around 6.1% of high paying customers have a probability to churn and rest 93.9% will not churn. Hence, it's a highly imbalanced dataset.
4. Average revenue per user in month 6,7,8 is approximately same for non churn customers but varies significantly for customers with high churn probability. The average revenue decreases significantly by month. 
5. The average recharge decreases considerably on monthly basis when the customer is about to churn. Hence, if recharge value is decreasing then it suggests that the customer might churn.
6. Average total incoming call minutes decreases drastically when customer is about to churn. Hence, it's a good variable for model training.
7. Average local outgoing call minutes decreases drastically when customer is about to churn. This means that customer begins to limit usage of calling with current network.
8. Average roaming incoming and outgoing minutes are also high when customer is about to churn. This may be due to high roaming costs. Company should take the romaing pricing into consideration to prevent customer churn.

## Feature Importance

![Feature-importance](https://github.com/A-yush/Telecom-Churn-Case-Study/blob/master/images/Feature-Importance.png)


## Recommendations

Hence, in order to prevent churn, company can:

1. Reduce the pricing for customers using high volume of roaming.
2. Discounts on data and providing customized plans for same.
3. Check for customers whose revenues are decreasing drastically and provide them some good plans to avpid churn.

### Model Evaluation

Plotting of AUC-ROC curve for Random Forect Classifier:

![RandomForestClassifier](https://github.com/A-yush/Telecom-Churn-Case-Study/blob/master/images/RandomForestClassifier.png)

## References
- Kaggle Data: https://www.kaggle.com/competitions/telecom-churn-case-study-hackathon-c48/data
- Telecom churn case study hackathon : https://www.kaggle.com/competitions/telecom-churn-case-study-hackathon-c48/overview


## Technologies Used
- Tensorflow - 2.3.4
- Numpy - 1.19.5
- Pandas - 1.1.5
- Sklearn
- Imblearn

## Contact
Created by [@A-yush] - feel free to contact me!