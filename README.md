# Supervised_Machine_Learning

## Credit_Risk_Analysis

### Project Overview

We aimed to provide a faster, more reliable loan experience through the use of machine learning models. Using these models, I was able to accurately identify good candidates for loans that could help a financial institution minimize their loan risk. Several machine learning algorithms were developed and evaluated that could predict credit risk.

### Resources
* Dataset:

  **LoanStats_2019Q1.csv**

* Software used:

1. Python

2. Jupyter Notebook

Various libraries and algorithms were used to build and evaluate models using resampling including:

* imbalanced-learn
* scikit-learn
* RandomOverSampler
* SMOTE algorithms
* ClusterCentroids algorithm
* SMOTEENN algorithm
* BalancedRandomForestClassifier (bias reduction model)
* EasyEnsembleClassifier (bias reduction model)

### Results:
In this section we demonstrate the results of different resampling method:

**Oversampling: Naive Random Oversampling**
Random oversampling involves randomly selecting minority instances and putting them in the training set to achieve balance between majority and minority instances.

- Balanced Accurracy Score: 0.674
- High-Risk Precision: 0.01
- High-Risk Recall: 0.74

<img width="686" alt="Screen Shot 2022-10-27 at 9 54 10 PM" src="https://user-images.githubusercontent.com/108313440/198451469-90a14e3a-20e8-40eb-aa1e-dc2c4589a212.png">


**Oversampling: SMOTE**

An approach to handle unbalanced datasets is Synthetic Minority Oversampling Technique (SMOTE).

- Balanced Accurracy Score: 0.662
- High-Risk Precision: 0.01
- High-Risk Recall: 0.63

<img width="698" alt="Screen Shot 2022-10-27 at 9 57 49 PM" src="https://user-images.githubusercontent.com/108313440/198452579-55a83eda-a9dd-45b7-97fd-6018ff6c48ed.png">




**Undersampling: Random Undersampling**

In random undersampling, the majority class is randomly selected and removed until its size is reduced to that of the minority class

- Balanced Accurracy Score: 0.662
- High-Risk Precision: 0.01
- High-Risk Recall: 0.63

<img width="688" alt="Screen Shot 2022-10-27 at 10 02 15 PM" src="https://user-images.githubusercontent.com/108313440/198454814-3649587d-9ab6-494d-805d-15870c9ae362.png">



**Combination Sampling: SMOTEENN**

In SMOTEENN, we combine over- and under-sampling using SMOTE and Edited Nearest Neighbours.

- Balanced Accurracy Score: 0.644
- High-Risk Precision: 0.01
- High-Risk Recall: 0.72


<img width="669" alt="Screen Shot 2022-10-27 at 10 05 04 PM" src="https://user-images.githubusercontent.com/108313440/198456550-b0370d3d-c009-4b6a-9197-acc66b67859e.png">


**Balanced Random Forest Classifier**

A balanced random forest randomly under-samples each boostrap sample to balance. 

- Balanced Accurracy Score: 0.788
- High-Risk Precision: 0.03
- High-Risk Recall: 0.70


<img width="647" alt="Screen Shot 2022-10-27 at 10 15 17 PM" src="https://user-images.githubusercontent.com/108313440/198462408-c62c0263-02b4-4cc9-9597-847ea62121a0.png">





**Easy Ensemble AdaBoost Classifier**

Bag of balanced boosted learners also known as EasyEnsemble.This algorithm is known as EasyEnsemble. The classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.

- Balanced Accurracy Score: 0.931
- High-Risk Precision: 0.09
- High-Risk Recall: 0.92

<img width="672" alt="Screen Shot 2022-10-27 at 10 21 36 PM" src="https://user-images.githubusercontent.com/108313440/198465538-bd05b43d-090a-4c25-9c75-db06f81dce82.png">


### Summary

The financial industry values sensitivity over precision when determining the risk and default rate of loan candidates. Banks want all high-risk individuals to be marked as high-risk in order to prevent them from defaulting. My analysis showed that all six algorithms had a really low precision rate for high risk individuals. A maximum precision of ?? was achieved by the Easy Ensemble AdaBoost Classifier, which is still regarded as being quite low for identifying high-risk borrowers. In other words, out of all customers who were labeled as high-risk, ?? were really high-risk. In ontrast, all the algorythem work perfectly to define low-risk customers. 

In terms of sensitivity, The easy ensemble adaboost model was the most sensitive (91% for high-risk individuals and 94% for low-risk individuals). Therefore, 91% of the time, all high-risk individuals are classified as high-risk. Other two models that had high recall were the Random Forest Classifier (67%) and SMOTEENN Resample (70%).

Balanced Accurracy Score is another indication of model efficiency. A model's accuracy is measured by how many of its predictions match the classification, out of all the predictions. Clearly, the Easy Ensemble AdaBoost Classifier had the highest accuracy score by far. Therefore, We should choose this model due to its high accuracy, precision, and sensitivity, 







