# Decision Tree C4.5 Implementation

Subject info: 31005 Machine Learning (University of Technology Sydney) <br>
Developer: Hang Sheng<br>
Assignment mark: 50/50 <br>
Final mark for this subject: 100/100

## Description for "31005-MLAssignment2.ipynb"
To implement the decision tree C4.5 algorithm, I design three classes which are:

Myutils: This class includes some math operation functions as follows: <br>

|Function name | Usage |
|------ | ------- |
| get_split_pointSet() | Discretize continuous attributes through the dichotomy |
| get_discrete_variables() | Convert continuous variables through the split point into categorical variables |
| compute_entropy() | calculate the information entropy |
| compute_info_gain_ratio() | Calculate the information gain ratio of the specified attribute for a continuous variable |

<br>

TreeNode: used to generate the tree node and print the node's details recursively. <br>


|Function name | Usage |
|------ | ------- |
|make() | split the attribute according to the C4.5 algorithm and generate the child node by the value of split attribute. |
|print_node_details()| print the information details of each node, this function is used to help me understand the tree structure and draw the decision tree structure later. |

<br>

TreeC4_5: generates the root tree node, fit the decision tree model and make predictions. <br>

|Function name| Usage |
|------ | ------- |
|fit() | fit the model by recall the make() function in the root node |
|make_decision() | predict the decision for each sample in the fitted model |
|predict() | passed in the testing datasets and predict the sample one by one, then return the list of decisions for each sample |

## Description for dataset
The “iris” dataset is used to implement the algorithm, and another two datasets, “Blood transfusion service center” and “wine quality”, are used to evaluate the algorithm. The latter two datasets can be used to test the robustness of my algorithm. All attributes (except for the target attribute) in these datasets are numerical types

### “Iris” dataset
This dataset contains 150 samples with 4 attributes. Since this data set has no noise data, and the number of sample and features are relatively small, it is conducive to the realization of the algorithm. 

### “Blood Transfusion Service Center” dataset
This dataset has 748 samples (501 samples for training & 246 samples for testing) with 5 numerical attributes. This dataset is used to evaluate whether my algorithm can handle some noise samples in the dataset. Such as the duplicated samples with the same target value or different target value. I do not drop these duplicated samples because my algorithm is able to deal with these special samples.

### “Wine Quality” dataset
This dataset has 4898 samples with 12 numerical attributes.I use this dataset to evaluate whether my algorithm can work well with the dataset with multiple attributes. I randomly select 750 of the total samples and categorize the target value by whether the target value is higher or lower than 6.5 to the categorical value “good” or “not good”, and split these 750 samples to 502 samples for training and 248 for testing my model.

PS: Since I only study the impact of C4.5 algorithm on continuous data, this decision tree model can not handle the discrete data.
