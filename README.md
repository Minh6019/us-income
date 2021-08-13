#  Model evaluation challenge - US Income
![Dollar Bundles (Image)](assets/us-dollar-bundles.jpg)

## Mission
One evening, while you were minding your own business watching the latest show on Netflix, you get an e-mail from a stock broker à la *Wolf of Wall Street*... the type of guy that only cares about sex, drugs and money.

He asks a favor from you.

At first, you are put off and stop reading. However, you remember that that guy has lots of money and likes to throw it around, so you read further.

He asks a simple question: *Are you able to predict the income of every US citizen?*

**How hard could that be ? Not that hard, no ?** True.

However, one has to be careful about how the data is processed to not give false results. That is why you are tasked, as a group, to discuss and implement various ways to get a correct prediction from a machine learning model.

## Mission objectives

- Be able to analyze a machine learning problem
- Be able to reason about possible causes of overfitting
- Be able to remedy the causes of overfitting
- Be able to tune parameters of a machine learning model
- Be able to write clean and documented code.

### Must-have features

- Baseline accuracy
- Multiple evaluation metrics
- Hyper parameter tuning
- Some type of validation strategy

##### Datasets: 
   - data_train.csv. Contains train data.
   - data_test.csv. Contains test data.

### Author:
* Hoang Minh (Minh6019)

### Step 1: Data preprocessing

 - The data is clean to use for the model

#### RandomForestClassifier:
+ **n_estimators=100**


  
   <img src = "plots/a1y_medianVSa2y_median_elbow.png" width = "500" height = "400">

 + **GridSearchCV _ param_grid = {'n_estimators': [100, 200, 300],'max_features': ['auto', 'sqrt', 'log2'} **
      
 
    <img src = "plots/4features.png" width = "450" height = "600">

 +  **GridSearchCV _ param_grid = {'n_estimators': [100, 200, 300],'max_features': ['auto', 'sqrt', 'log2'} **
      
     <img src = "plots/4features.png" width = "450" height = "600">
  
  +  **GridSearchCV _ param_grid = {'n_estimators': [100, 200, 300],'max_features': ['auto', 'sqrt', 'log2'} **
      
     <img src = "plots/4features.png" width = "450" height = "600">
    
 #### Results of Kmeans corresponding with 2, 3, 4, 5 ,6 -features: 
    Best silhouette scores for n features (KMeans++) using all the dataset
| # features | Clusters | Score |  
| ---------- | -------- | ----- |
| 2          | 2        | 0.873 | 
| 3          | 2        | 0.808 |
| 4          | 2        | 0.793 |
| 5          | 2        | 0.737 |
| 6          | 2        | 0.791 |

### Conclusion 
  + The results show that the best scores of 2 features are with a cluster of size 2, and the silhouette score keeps decreasing as we increase the number of features used to cluster.
  + With the current dataset, the Kmeans method gives higher silhouette score than DBSCAN


# Timeline: 
13/08/2021 - 13/08/2021
