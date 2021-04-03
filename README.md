# Handling Imbalanced Data

pip install imbalanced-learn 0.7.0


**Interview Question: how will you handle imbalanced Data set:
- I'll look into data, if data is small, i'll use under sampling. I'll also look into performance metrics like precission and Recall, F1 Score. Based on domain knowledge, i'll also look into reducing false positives or false negatives. Based on that i'll see ROC Score and do some SMOTE techniques.
- If nothing is working, i'll go to Ensemble techniques like Random Forest, XGBoost,etc 

Imbalanced Data Set:
 - majority class is about 9 times bigger than the minority class

Standard classifier algorithms like Decision Tree and Logistic Regression have a bias towards classes which have number of instances. They tend to only predict the majority class data. The features of the minority class are treated as noise and are often ignored. Thus, there is a high probability of misclassification of the minority class as compared to the majority class.
                   - Accuracy Paradox


********* Decission Tree Algorithms - RF, XGBoost, ADABoost works so much better for Imbalanced Data Sets. 

----------------------------
1. Try using class weights - like increase class wight of the lower value to 100 times or etc

2. Undersampling - By using this, reduce the points of the Maximum Label.   ---(from imblearn.undersampling import NearMiss) it takes majority class ratio to minority - 0:199017 and 1: 347, after taking NearMiss(0.8); we get 0: 433 and 1:347 -->(0.8 of 433 = 347)

3. Over Sampling - By using this, increase the poins of the Minimum Label.  ---(from imblearn.oversampling import RandomOverSampler) 

4. SMOTE - SMOTE (Synthetic Minority Oversampling Technique) works by randomly picking a point from the minority class and computing the k-nearest neighbors for this point. The synthetic points are added between the chosen point and its neighbors.  (Look nalytics Vidya Blog - very detailed info)
Simply, it creates new points. Based on nearest points, it wll create new points. In oversampling, it creates points on same point

5. Ensembel techniques - Easy ensemble classifier




https://www.analyticsvidhya.com/blog/2017/03/imbalanced-data-classification/
https://www.analyticsvidhya.com/blog/2020/10/overcoming-class-imbalance-using-smote-techniques/
https://www.analyticsvidhya.com/blog/2020/07/10-techniques-to-deal-with-class-imbalance-in-machine-learning/

