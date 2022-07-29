# Credit_Risk_Analysis
# Machine Learning
## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we need to employ different techniques to train and evaluate models with unbalanced classes.We used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.


## Results

### Deliverable 1: Use Resampling Models to Predict Credit Risk
We were given a Credit Risk resampling dataset which was cleaned up. Then we were asked to use 3 Machine Learning Models by using resampling to determine which is better at predicting credit risk. 
We have 2 types of loan_status es which are low_risk and high_risk. We are trying to see if the algorithms can predict the righ_risk s properly. 

#### Naive Random Oversampling

![image](https://user-images.githubusercontent.com/3753839/181682546-885b7f6b-f3a2-4d16-b2b1-f7853637ad66.png)

The above results don’t show a very good accuracy which is 0.63

![image](https://user-images.githubusercontent.com/3753839/181682584-6051dd6b-3d17-4b83-9f4d-0923560f9b2e.png)


The f1-score for the high risk shows 0.02 which is also very low.

#### SMOTE Oversampling

![image](https://user-images.githubusercontent.com/3753839/181682593-79c1d2aa-78b4-4094-9427-92ae30195769.png)


This model also doesn't provide a good result as we see above that the accuracy score is just 63%.

![image](https://user-images.githubusercontent.com/3753839/181682626-34cba86e-70bc-49da-8ba5-900c44a4a514.png)


The f1-score for the high risk also shows 0.02 which is very low, similar to the prior algorithm.

#### Undersampling

![image](https://user-images.githubusercontent.com/3753839/181682640-c114e4d9-9521-4433-836d-198996ca5487.png)


This model shows the worst prediction which just above 50%.

![image](https://user-images.githubusercontent.com/3753839/181682658-7954a709-b522-4f56-ac77-457bec10ec58.png)


The f1-score for high risk status reflects the same as well of a very low value 0.01 in this case.



### Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk

#### Combination (Over and Under) Sampling

![image](https://user-images.githubusercontent.com/3753839/181682689-7ea3546d-76eb-444e-aba9-8f07ddecfb77.png)


Though the score is similarly low, it is the highest relative to the above 3 shown here. 

![image](https://user-images.githubusercontent.com/3753839/181682720-09fdd86e-9354-4c08-abff-65d86d77105f.png)


The f1-score though says the same 0.02 for high risk status.


### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

#### Balanced Random Forest Classifier


![image](https://user-images.githubusercontent.com/3753839/181682738-93842221-9267-420b-9028-391788a7cedf.png)

The above algorithm shows us a significant improve in the prediction which is 78% which is not desired but definitely better than the prior ones seen above.

![image](https://user-images.githubusercontent.com/3753839/181682764-010ef365-013b-4eb4-b732-7d5d2e8ad17f.png)


The f1-score for high_risk score also shows improvement and the avg-total f1-score also reached 95% here which is pretty good. 

#### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/3753839/181682784-aba93440-b809-4705-849a-2c69a924c9f5.png)

Seeing the above result we can say this is the best prediction among all the others shown here.
It is 92% which means 92 out of 100 predictions can be done correctly which is much better. 


![image](https://user-images.githubusercontent.com/3753839/181682815-80f0a1f9-3f2a-4e45-a23c-746cf93650ca.png)

The f1-score for high_risk has also taken a leap to 0.14 which is the best among the results presented here.
Also the average f1-score shown 97% which is way better than the others here as well. 
This model is the best among all others shown here.

### Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)


## Summary
The dataset that was given to us had the following classification where the low risk status was way more than high risk.
This may cause the results to be skewed if the samples are not properly stratified.

![image](https://user-images.githubusercontent.com/3753839/181683111-8fee5d0a-ea1a-4b2b-a62a-b0cc044d573a.png)



Now if we see all the algorithms above, the Easy Ensemble AdaBoost Classifier model yielded the best results with an accuracy rate of 93% and a 7% precision when predicting "High Risk". The sensitivity/recall rate was also the highest at 91% compared to the other models. The model was also able to predict the highest results for "Low Risk" with sensitivity rate at 94% and an F1 score of 97%. 

Overall if we reconcile the details in order of highest performance for high_risk loan_status
* Easy Ensemble AdaBoost Classifier model : 93% accuracy, 7% precision, 91% recall, and 14% F1 Score
* Balanced Random Forest Classifier: 78.8% accuracy, 4% precision, 67% recall and 7% F1 Score
* Naive Random Oversampling: : 64.6% accuracy, 1% precision, 62% recall and 2% F1 Score
* Combination (Over and Under) Sampling: 64% accuracy, 1% precision, 70% recall and 2% F1 Score
* SMOTE Oversampling: 63% accuracy, 1% precision, 62% recall and 2% F1 Score
* Undersampling: 51% accuracy, 1% precision, 59% recall and 1% F1 Score

This is not a perfect model and would need more analysis. More work can be done with ordering the features by performance and then use those selected Features only to predict with this model and see if it improves the performance.





