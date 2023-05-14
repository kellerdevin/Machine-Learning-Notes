** 

1. AUC-ROC  

-   shows how well the model can distinguish between the positive and negative classes by plotting the true positive rate (TPR) against the false positive rate (FPR) at different classification thresholds. A higher AUC-ROC score indicates that the model is better at distinguishing between the two classes, while a lower score indicates that the model is less accurate.
    

2. R^2, Adjusted R^2, MSE, RMSE, MAE, MAPE  

-   R^2
    

-   R^2 tells us how well the independent variable(s) are able to predict the variation in the dependent variable. A higher R^2 value indicates a stronger relationship between the independent and dependent variables, and a better fit of the regression model to the data.
    
-   R^2 ranges from 0 to 1, with 1 indicating a perfect fit of the regression model to the data, and 0 indicating that the model is unable to explain any of the variance in the dependent variable. 
    

-   Adjusted R^2
    

-   Adjusted R-squared (Adjusted R^2) is a modification of the regular R-squared statistic that takes into account the number of independent variables in a regression model.
    
-   Adjusted R^2 addresses this issue by penalizing the R^2 value for each additional independent variable that is added to the model.
    

-   MSE 
    

-   MSE is used to measure the average squared difference between the predicted values and the actual values in a regression problem.
    
-   A lower MSE indicates that the model is better at predicting the actual values, while a higher MSE indicates that the model is less accurate.
    

-   RMSE 
    

-   Used to measure the average distance between the predicted values and the actual values in a regression problem.
    
-   The main advantage of RMSE over MSE is that it is in the same units as the dependent variable, making it more interpretable. 
    
-   RMSE is more sensitive to outliers than MSE, since the square root operation magnifies the effect of larger errors.
    

-   MAE
    

-   MAE tells us how well a regression model is able to predict the actual values by measuring the average absolute difference between the predicted and actual values.
    
-   Less sensitive to outliers and gives equal weights to all errors
    

-   MAPE
    

-   MAPE tells us how well a regression model is able to predict the actual values by measuring the average percentage difference between the predicted and actual values.
    

3. Accuracy, Precision, Recall, F1-Score 

-   Accuracy: 
    

-   Accuracy is the ratio of the number of correctly predicted samples to the total number of samples. It is a simple and intuitive metric, but it can be misleading in cases where the data is imbalanced or the cost of false positives and false negatives is not equal.
    
-   Great if data is evenly distributed
    

-   Precision measures how often the model correctly identifies positive samples. It is a useful metric when the cost of false positives is high, such as in medical diagnosis, where a false positive could lead to unnecessary treatment.
    

-   A high precision score means that the model is making few false positive predictions and is confident in its predictions.
    

-   Recall measures how often the model correctly identifies positive samples out of all positive samples. It is a useful metric when the cost of false negatives is high, such as in fraud detection, where a false negative could result in financial loss.
    

-   A high recall score means that the model is able to identify most of the positive samples and is not missing many positive cases.
    

-   F1-Score is a metric that combines both precision and recall into a single score, calculated as the harmonic mean of the two metrics. It is a useful metric when both precision and recall are important, and the data is imbalanced. The F1-Score is a balanced metric, providing a compromise between precision and recall.


**