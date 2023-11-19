# Multi-label classification
Multi-label classification refers to the classification tasks that have two or more class labels, where one or more class labels may be predicted for each example.

## Examples
Consider the example of photo classification, where a given photo may have multiple objects in the scene and a model may predict the presence of multiple known objects in the photo, such as “bicycle,” “apple,” “person,” etc.

This is unlike binary classification and multi-class classification, where a single class label is predicted for each example.

## Algorithms
It is common to model multi-label classification tasks with a model that predicts multiple outputs, with each output taking predicted as a Bernoulli probability distribution. This is essentially a model that makes multiple binary classification predictions for each example.

Classification algorithms used for binary or multi-class classification cannot be used directly for multi-label classification. Specialized versions of standard classification algorithms can be used, so-called multi-label versions of the algorithms, including:

- Multi-label Decision Trees.
- Multi-label Random Forests.
- Multi-label Gradient Boosting.

Another approach is to use a separate classification algorithm to predict the labels for each class.