# Credit-Card-Fraud-Prediction


# CONCLUSION


# Describe your fraud detection model in elaboration.
We want to make a classifier, where the target variable is whether a given
transaction is fraudulent or not.
The model will produce a probability score at the transaction level for that
particular transaction being fraudulent, and if it is above a certain
threshold then it will predict a 1 for fraud and 0 for non-fraud.
The label, fraud or not, can be identified from looking at which past
transactions were actually refunded or disputed.


# How did you select variables to be included in the model?
To build our model, we split the data into a training and testing set.
Regardless of the classifier chosen (SVM, Logistic Regression, etc.)
To evaluate our classifier, we can look at precision and recall:
Precision is defined as the number of true positives divided by the sum of true
positives and false positives.
A true positive, for this business context, is when the model predicts a
fraudulent transaction and the transaction was actually fraudulent.
15
A false positive is when the model predicts a fraudulent transaction but the
transaction was actually not fraudulent. There is a cost to a false positive:
 the business will lose out on the particular transaction. Therefore, it is
important to maximize precision, since the higher it is, the fewer false
positives there are.
Recall is defined as the number of true positives divided by the sum of true
positives and false negatives.
A false negative is when the model predicts that the transaction is not
fraudulent, but the transaction actually turned out to be fraudulent.
The cost of a false negative is the cost of the transaction itself. Therefore,
it is important to maximize recall, since the higher it is, the fewer false
negatives there are.


# Demonstrate the performance of the model by using best set of tools.
We have seen that Accuracy of both Random Forest and Decision Tree is equal,
although teh precision of Random Forest is more.
In a fraud detection model,
Precision is highly important because rather than predicting normal
transactions correctly we want Fraud transactions to be predicted correctly
and Legit to be left off.
If either of the 2 reasons are not fulfiiled we may catch the innocent and
leave the culprit.
This is also one of the reason why Random Forest and Decision Tree are used
unstead of other algorithms.
Also the reason I have chosen this model is because of highly unbalanced
dataset (Legit: Fraud :: 99.87:0.13). Random forest makes multiple decision
trees which makes it easier (although time taking) for model to understand
the data in a simpler way since Decision Tree makes decisions in a boolean
way.
Models like XGBoost, Bagging, ANN, and Logistic Regression may give good
accuracy but they won't give good precision and recall values.


# What are the key factors that predict fraudulent customer?
The source of request is secured or not ?
16
Is the name of organisation asking for money is legit or not ?
Transaction history of vendors.


# Do these factors make sense? If yes, How? If not, How not?
Yeah


# What kind of prevention should be adopted while company update its
infrastructure?
Use smart vertified apps only.
Browse through secured websites.
Use secured internet connections (USE VPN).
Keep your mobile and laptop security updated.
Don't respond to unsolicited calls/SMS(s/E-mails.
If you feel like you have been tricked or security compromised, contact your
bank immidiately.


# Assuming these actions have been implemented, how would you determine if they
work?
Bank sending E-statements.
Customers keeping a check of their account activity.
Always keep a log of your payments.
