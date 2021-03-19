# Decision Tree C4.5 Implementation

Subject info: 31005 Machine Learning <br>
Developer: Hang Sheng <br>
Assignment mark: 50/50 <br>
Final mark for this subject: 100/100

## Dataset description
The “iris” dataset is used to implement the algorithm, and another two datasets, “Blood transfusion service center” and “wine quality”, are used to evaluate the algorithm. All attributes (except for the target attribute) in these datasets are numerical types

### “Blood Transfusion Service Center” dataset
This dataset has 748 samples (501 samples for training & 246 samples for testing) with 5 numerical attributes. This dataset is used to evaluate whether my algorithm can handle some noise samples in the dataset. Such as the duplicated samples with the same target value or different target value. I do not drop these duplicated samples because my algorithm is able to deal with these special samples.

### “Wine Quality” dataset
This dataset has 4898 samples with 12 numerical attributes.I use this dataset to evaluate whether my algorithm can work well with the dataset with multiple attributes. I randomly select 750 of the total samples and categorize the target value by whether the target value is higher or lower than 6.5 to the categorical value “good” or “not good”, and split these 750 samples to 502 samples for training and 248 for testing my model.

### 31005-MLAssignment2.ipynb
Three classes are defined to implement the decision tree C4.5 algorithm which are:

1. Myutils <br>
This class will be used in subsequent c4.5 decision tree construction, it includes some math operation functions as follows:

| get_split_pointSet() | Discretize continuous attributes through the dichotomy |
| get_discrete_variables() | Convert continuous variables through the split point into categorical variables |
| compute_entropy() | calculate the information entropy |
| compute_info_gain_ratio() | Calculate the information gain ratio of the specified attribute for a continuous variable |


Note: This decision tree model can only handle the numerical datasets.
