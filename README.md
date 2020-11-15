# Credit Risk Analysis


## Overview
The purpose of this analysis is to create a model that will predict credit risk.  I will create and train six different models then generate performance measures to determine which, if any, are appropriate to use to determine credit card risk.

## Results
* [RandomOverSampler:](ros_report.PNG) 
    * Accuracy = .660
    * Precision =  (high risk:.01, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.74, low risk: .58, mean: .58) 

* [SMOTE:](SMOTE_report.PNG) 
    * Accuracy = .654
    * Precision =  (high risk:.01, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.62, low risk: .68, mean: .68)

* [ClusterCentroids:](cluster_report.PNG) 
    * Accuracy = .547
    * Precision =  (high risk:.01, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.68, low risk: .41, mean: .41)

* [SMOTEEN:](SMOTEEN_report.PNG) 
    * Accuracy = .645
    * Precision =  (high risk:.01, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.72, low risk: .57, mean: .57)   

* [Balanced Random Forest:](bf_report.PNG) 
    * Accuracy = .789
    * Precision =  (high risk:.03, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.70, low risk: .87, mean: .87)

* [Easy Ensemble:](ada_report.PNG) 
    * Accuracy = .932
    * Precision =  (high risk:.09, low risk: 1.0, mean: .99) 
    * Recall = (high risk:.92, low risk: .94, mean: .94)  


## Summary
The accuracy of the over and under sampling models are all about the same with the Cluster Centroid model being the least accurate overall.  The accuarcy of the ensemble classifiers are much higher than the other models.  Precision is similar across all models.  A good recall rate is important for determining credit risk.  This is because we want fewer False Negatives.  Higher recall means our model will identify the maximum number of clients who are actually at risk for default.  The Easy Ensemble model had a high recall rate for determining both high and low risk.  This is the model I would choose because it is the most likely to correctly identify both high and low risk customers.