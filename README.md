# Decision Tree C4.5 Implementation
Note: This decision tree model can only handle the numerical datasets.

## Introduction
Decision tree is a supervised learning algorithm that uses observed data and labels to build a decision tree. Given the observable datasets with attributes: {X1 ,X2, ...., Xn} and labels: {C1, C2, .....,Cn}, the decision tree fT may have a mapping from the input datasets with n attribute values to make a prediction y, the mapping relation is: fT(X1, X2, ...., Xn) = y , y ∈ {C1, C2, .....,Cn}. The tree fT performs the mapping by viewing the condition of the split attribute node by node until reaching the leaf node and making the decision. 

## Datasets description
The “iris” dataset is used to implement the algorithm, and another two datasets, “Blood transfusion service center” and “wine quality”, are used to evaluate the algorithm. All attributes (except for the target attribute) in these datasets are numerical types

### “Blood Transfusion Service Center” dataset
This dataset has 748 samples (501 samples for training & 246 samples for testing) with 5 numerical attributes. This dataset is used to evaluate whether my algorithm can handle some noise samples in the dataset. Such as the duplicated samples with the same target value or different target value. I do not drop these duplicated samples because my algorithm is able to deal with these special samples.

### “Wine Quality” dataset
This dataset has 4898 samples with 12 numerical attributes.I use this dataset to evaluate whether my algorithm can work well with the dataset with multiple attributes. I randomly select 750 of the total samples and categorize the target value by whether the target value is higher or lower than 6.5 to the categorical value “good” or “not good”, and split these 750 samples to 502 samples for training and 248 for testing my model.
