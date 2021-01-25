# Capstone-Project
Analysis for Ransomware Detection on the Bitcoin Blockchain.

# Introduction about Bitcoin:
Bitcoin transactions can be created anonymously, and participation in the network does not require identity verification. A payment can be requested by delivering a public Bitcoin address to a sender by using anonymity networks.
This ease of usage and worldwide transaction availability of Bitcoin have been noticed by malicious actors.

# Purpose of the project:
Detection and classification.
Detection a new family of ransomware.

# Steps that will be follow for Detection and Prediction Ransomware.
1. Which features can we extract from the Bitcoin network to detect ransomware payments. 
2. Does a ransomware family.
3. Can we detect Bitcoin ransom payments that are not reported to law agencies or Blockchain Data Analytics companies?

# Feature Extraction:
-  Address: Ch, stores the bitcoin address.
- Year: Int, stores the day of the year of the transaction.
- Day: Int, stores the day of the year of the transaction, ex. 1 is the first day, 365 the last day.
- Length: Int, storing the number of maxing rounds on Bitcoin.
- Weight: Int, storing the merge behavior.
- Count: Int, quantifying the merging pattern.
- Neighbors: Int, storing number of transactions, that have address as one of its output addresses.
- Looped: Int, storing the number of starter transaction that connected with more than directed path. 
- Income: Int, storing the amount of Bitcoin.
 
Dependent/ Response Variable:
- Label: Ch, stores the name of ransomware family.

# Data Preprocess:
1. Check the number of columns and rows, in order to understand the size of data.
2. Check if there is missing values, in order to decided how to handle missing values when it apply machine learning.

# Machine learning model:
 1. DBScan Clustering:
Density-Based Clustering is an Unsupervised learning Non-linear algorithm. The data is partitioned into groups with similar characteristics or clusters. DBScan can mark outlier points that lie alone in low-density regions as noise. 

 2. Support Vector Machines (SVMs):
Is supervised learning models with associated learning algorithms that analyze data used for classification and regression analysis. This means that SVM trains on a set of labeled data. SVM studies the labeled training data and then classifies any new input data depending on what it learned in the training phase.

3. Naive Bayes
Naive Bayes is a Supervised Machine Learning algorithm based on the Bayes Theorem with an assumption of independence among predictors, that is used to solve classification problems  by following a probabilistic approach. idea that the predictor variables in a machine learning model are independent of each other. Meaning that the outcome of a model depends on a set of independent variables that have nothing to do with each other. 
 Bayes theorem provides a way of calculating posterior probability P(c|x) from P(c), P(x) and P(x|c). 
     P(c|x) is the posterior probability of class (c, target) given predictor (x, attributes).
     P(c) is the prior probability of class.
     P(x|c) is the likelihood which is the probability of predictor given class.
     P(x) is the prior probability of predictor.

# Conclusion:

In this project I have use SVM and Naive Bayes, to detect and predict ransomware payments on Bitcoin. That  seems to work well to classify and recognize the ransomware family. Therefore, we can detect a new ransomware family. 


# Challenge:
 - Error: vector memory exhausted (limit reached)!!
 By try to take a saple befor split the data into train and test data set.

 
# Future work:
- Based on the information about existing ransomware families at a time, we can detect the emergence of a new ransomware on the Bitcoin blockchain.
- Make my analysis as production.

