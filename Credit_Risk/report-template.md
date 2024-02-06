# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  - The purpose of this analysis is to create and evaluate the accuracy of a data model that predicts the worthiness of credit regarding to potential borrowers from peer-to-peer lending services
* Explain what financial information the data was on, and what you needed to predict.
  - This financial information is based on public historical lending activies from a peer-to-peer lending services and we are trying to predict the credit worthiness of borrowers
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  - Some variables used were, The Loan Size, The Interest Rate, Borrower Income, Debt-To-Income Ratio, The Number of Accounts, Derogatory Marks, Total Debt, and the Statues of the Loan
* Describe the stages of the machine learning process you went through as part of this analysis.
  - I Preprocessed the data by reading the CSV file and reviewed the columns to find the available features. I created features for X and Y variales that I could turn into structures training and testing data. With the data being split into training and testing with the train_test_split method. Afterwards a regression model was trained using the original data and then again with the resampled data. Finally, the model's performance was evaluated using metrics such as Accuracy, Precision, Recall, and Generation of a confusion matrix and a classification report.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  - Methods that I used in this code would be a Logistic Regression model to predict credit risk. A RandomOverSampler to address oversimplification from the minority class variable in the training data. Followed up by some Model Evaluation Metrics which balanced Accuracy Score, Confusion Matrix, and classification reports that were used to assess the model's performance in both scenarios.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    - Balanced Accuracy Score: 0.9697 which shows a high level of promise.
    - Precision Score: Healthy Loans (0) sit at 1.00 very comfortably which High-Risk Loans(1) sit at 0.85 which is still decent but far less desirable compared to the previous numbers.
    - Recall Score: Healthy Loans (0) are at a stable 0.99 similar to the precision and the High-Risk Loans(1) do a bit better here at 0.95.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    - Balanced Accuracy Score: 0.9936 which is higher than the first model and likewise shows good promise.
    - Precision Score: Healthy Loans (0) is 1.00 at the highest level while High-Risk Loans (1) are struggling at 0.84 which is less than I'd like to have.
    - Recall Score: Healthy Loans (0) here are 0.99 so still great but not as good as the Precision Score althought High-Risk Loans is at 0.99 giving it solid credibility compared to before.
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
- Overall Key Observations
  - Model 2 outperformed Model 1 in terms of balanced accuracy, achieving a higher score (0.9936 vs. 0.9697).
  - Both the models show high precision and recall for Healthy Loans (0), with somewhat near perfect accuracy and recall scores, showing their effectiveness in identifiying healthy loans.
  - Model 2 shows improvement in the recall for High-Risk Loans (1) compared to Model 1 which indicates that the oversampling process positively effected the model's ability to detect High-Risk Loans. 

- I would recommend Model 2 over Model 1 due to the higher balanced accuracy and improced recall for the High-Risk Loans. It shows that the oversampled data is better used for predicting credit risk.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  - I would say it is of critical importance that you make sure every possible High-Risk Loan is accounted for correctly as if you classify a High-Risk Loan as a Healthy one, there is a massive opportunity for loss to occur there. On the other hand, if you misclassify a Heathly Loan as a High-Risk Loan then there is an opportunity for a missed source of revenue or income but this is a far perferable outcome compared to going all in on a seemingly and reportidly safe call.

If you do not recommend any of the models, please justify your reasoning.
