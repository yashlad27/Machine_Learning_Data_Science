# ZTM_Machine_Learning_Data_Science
Machine Learning And Data Science Repo

---
# Scikit-Learn:
### Feature Scaling:

->Once your data is all in numerical format, there's one more transformation you'll probably want to do to it.
It's called **Feature Scaling**.

-> In other words, making sure all of your numerical data is on the same scale.

-> Ex: say you were trying to predict the sale price of cars and the number of kilometres on their odometers varies from 6,000 to 345,000 but the median previous repair cost varies from 100 to 1,700. A machine learning algorithm may have trouble finding patterns in these wide-ranging variables.

-> Tp fix this: there are two main types of Feature Scaling:
1. Normalisation: [Min-max scaling]
    <br>
    This rescales all the numerical values to between 0 and 1, with the lowest value being close to 0 and the highest previous value being close to 1. Scikit-Learn provides functionality for this in the MinMaxScalar class.
    <br>
2. Standardization:
    <br>
    This subtracts the mean value from all of the features (so the resulting features have 0 mean). It then scales the features to unit variance (by dividing the feature by the standard deviation). Scikit-Learn provides functionality for this in the StandardScalar class.
    <br>

-> **Points to Remember:**
    <br>
* Feature scaling usually isn't required for your target variable.
    <br>
* Feature scaling is usually not required with tree-based models (e.g. Random Forest) since they can handle varying features.
 <br>
---
### ROC and AUC:
* Points to Remember:
    1. ROC curves and AUC metrics are evaluation metrics for binary classification models (a model which predicts one thing or another, such as heart disease or not).
    2. The ROC curve compares the true positive rate (tpr) versus the false positive rate (fpr) at different classification thresholds.
    3. The AUC metric tells you how well your model is at choosing between classes (for example, how well it is at deciding whether someone has heart disease or not). A perfect model will get an AUC score of 1.

---

Machine Learning Model Evaluation

Evaluating the results of a machine learning model is as important as building one.

But just like how different problems have different machine learning models, different machine learning models have different evaluation metrics.

Below are some of the most important evaluation metrics you'll want to look into for classification and regression models.

Classification Model Evaluation Metrics/Techniques

    Accuracy - The accuracy of the model in decimal form. Perfect accuracy is equal to 1.0.

    Precision - Indicates the proportion of positive identifications (model predicted class 1) which were actually correct. A model which produces no false positives has a precision of 1.0.

    Recall - Indicates the proportion of actual positives which were correctly classified. A model which produces no false negatives has a recall of 1.0.

    F1 score - A combination of precision and recall. A perfect model achieves an F1 score of 1.0.

    Confusion matrix - Compares the predicted values with the true values in a tabular way, if 100% correct, all values in the matrix will be top left to bottom right (diagonal line).

    Cross-validation - Splits your dataset into multiple parts and train and tests your model on each part then evaluates performance as an average.

    Classification report - Sklearn has a built-in function called classification_report() which returns some of the main classification metrics such as precision, recall and f1-score.

    ROC Curve - Also known as receiver operating characteristic is a plot of true positive rate versus false-positive rate.

    Area Under Curve (AUC) Score - The area underneath the ROC curve. A perfect model achieves an AUC score of 1.0.

Which classification metric should you use?

    Accuracy is a good measure to start with if all classes are balanced (e.g. same amount of samples which are labelled with 0 or 1).

    Precision and recall become more important when classes are imbalanced.

    If false-positive predictions are worse than false-negatives, aim for higher precision.

    If false-negative predictions are worse than false-positives, aim for higher recall.

    F1-score is a combination of precision and recall.

    A confusion matrix is always a good way to visualize how a classification model is going.

Regression Model Evaluation Metrics/Techniques

    R^2 (pronounced r-squared) or the coefficient of determination - Compares your model's predictions to the mean of the targets. Values can range from negative infinity (a very poor model) to 1. For example, if all your model does is predict the mean of the targets, its R^2 value would be 0. And if your model perfectly predicts a range of numbers it's R^2 value would be 1.

    Mean absolute error (MAE) - The average of the absolute differences between predictions and actual values. It gives you an idea of how wrong your predictions were.

    Mean squared error (MSE) - The average squared differences between predictions and actual values. Squaring the errors removes negative errors. It also amplifies outliers (samples which have larger errors).

Which regression metric should you use?

    R2 is similar to accuracy. It gives you a quick indication of how well your model might be doing. Generally, the closer your R2 value is to 1.0, the better the model. But it doesn't really tell exactly how wrong your model is in terms of how far off each prediction is.

    MAE gives a better indication of how far off each of your model's predictions are on average.

    As for MAE or MSE, because of the way MSE is calculated, squaring the differences between predicted values and actual values, it amplifies larger differences. Let's say we're predicting the value of houses (which we are).

        Pay more attention to MAE: When being $10,000 off is twice as bad as being $5,000 off.

        Pay more attention to MSE: When being $10,000 off is more than twice as bad as being $5,000 off.

For more resources on evaluating a machine learning model, be sure to check out the following resources:

    Scikit-Learn documentation for metrics and scoring (quantifying the quality of predictions)

    Beyond Accuracy: Precision and Recall by Will Koehrsen

    Stack Overflow answer describing MSE (mean squared error) and RSME (root mean squared error)