# Decision Tree C4.5 Implementation

## Introduction
Decision tree is a supervised learning algorithm that uses observed data and labels to build a decision tree. Given the observable datasets with attributes: {X1 ,X2, ...., Xn} and labels: {C1, C2, .....,Cn}, the decision tree fT may have a mapping from the input datasets with n attribute values to make a prediction y, the mapping relation is: fT(X1, X2, ...., Xn) = y , y ∈ {C1, C2, .....,Cn}. The tree fT performs the mapping by viewing the condition of the split attribute node by node until reaching the leaf node and making the decision. 

## Datasets description
The “iris” dataset is used to implement the algorithm, and another two datasets, “Blood transfusion service center” and “wine quality”, are used to evaluate the algorithm. All attributes (except for the target attribute) in these datasets are numerical types
