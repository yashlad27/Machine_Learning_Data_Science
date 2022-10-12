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

