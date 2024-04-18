# Penguin-Species-Clustering
Unsupervised machine learning clustering two species of penguins based on body measurements

# Data Analyzed
344 penguins measured
4 measurements and determination of biological sex 

# Project Goals 
Research Question
Given the unlabeled data, can we determine how many different species of penguins are in the group of data?

# Dataset Exploration and Preprocessing
What did we look at?
I started data exploration by looking at the general info for the data and noticed that there were some outliers in the ‘sex’ column that would need to be dropped later. 
Next I looked at boxplots for each of the measurements, and noticed that the flipper length measurements had one extremely high outlier and another value that was negative, that must be incorrect. I addressed this by identifying the two rows that had these values and dropped them from the dataset. 
Next I looked at correlation scatter plot for all of the features with data separated by sex, and I noticed that there were a couple of datapoints that were not classified into either sex. Checking the unique values for the ‘sex’ variable, there was a value for ‘ . ‘, which is likely supposed to be a null value. Ichanged any of the ‘ . ‘ values to nulls and then dropped all of the nulls, including the nulls I noticed initially. 
Lastly, I changed the ‘sex’ variable values from strings (‘MALE’ / ‘FEMALE’) to integers (1 for male, 0 for female)


# Dimensionality Reduction Process
Overview of methods used
PCA
t-SNE
UMAP 
Evaluation methods
Visual examination of labeled and unlabeled data to see if dimensionality reduction produced distinct separate clusters of data

# Modeling Process
Overview of models used 
K-means
Hierarchical clustering
Showed clear separation of groups, ward and cosine affinity worked best
DBSCAN
Performed well but not as well as the hierarchical clustering
Gaussian mixture models (GMM)
Performed well like k-means
Evaluation methods
ARI and silhouette score 


# Model Comparison
How did the models perform?
Looking at the ARI and silhouette scores for each method, the GMM clustering method, the k-means method, and two of the hierarchical methods tied, so any of those would be good for this dataset

# Conclusions
We saw four distinct clusters, indicating clear separation between the species as well as the sexes within each species. This indicates that it is possible to take measurements from each of these species and determine not only their species but sex from these measurements. 
