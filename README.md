# READ ME 
## Data understanding
The dataset is a cleaned version of the original set which was collected during an anonymous survey conducted between January and June 2023. That dataset can be used for predictive modeling in mental health research, particularly in identifying key contributors to mental health challenges in a non-clinical setting.


The target dataset provides a more analysis-ready version for data scientists. It had gone through data cleaning (i.e. missing data, duplication) and has reduced number of features (columns), narrowing it down to the more important facets of depression in students. In particular, it contains 502 entres with 9 different features revolving around the target variable, Depression.

Unlike others, the target variable, Depression, is only a diagnosis given presumably by the original dataset's author, Dr. Samay Pathak, based the other variables collected from the survey. No additional information is found about how conclusions are made.

Link: https://www.kaggle.com/datasets/ikynahidwin/depression-student-dataset

Link (original dataset): https://www.kaggle.com/datasets/sumansharmadataworld/depression-surveydataset-for-analysis

## Motivation

The dataset is a perfect material for applying Machine Learning model to predict Depression diagnosis. It also provides a great opportunity to match professsional-level diagnosis in non-clinical setting as the data are from surveys that participants answered without requiring any professional mental health assessments or diagnostic test scores.

The analysis and data modelling of this dataset should provides significant insights onto how everyday factor affects the mental well-being of students and support early diagnosis and prevention against depression and its impacts on students.

It is worth noting that because the target variable was not collected like other variables and is only (presumably) diagnosis by a doctor based the other known factors, model accuracy should not be interpreted as how well it predicts depression in student but as how well it matches diagnoses of a professional.

## Result
After some additional cleaning and pre-processing, the datatset was used to train a logistic regression model with Depression as the target variables. Not all features of the set were used and selection was conducted based on correlation strength between each feature and Depression.

The Logistic Regression model utilized the sklearn library and used the default values for most hyperparameters. A seed number (2025) was set where appropriate to ensure reproducibility of the model and its results.

On the testset, the model scored an accuracy score of ~92% over 101 examples. Such performance is indicative a strong predictive power, showing how closely machine learning can match diagnosis of a professional using non-clinical data.

The model reinforced some common-sense connection while also brought about interesting insights onto diagnosing Depression and its relating factors in students:
- The most significant indicators of Depression in student include having suicidal thoughts, high academic pressure, and high financial stress, respectively.
- Students' study satisfaction, while having little to no effect in indicating Depression when low, reduces chance of having depression significantly when high.
- Age is not particularly indicative in determining Depression in students in comparison to other factors.
- Having a healthy diet is a significant sign of non-depression.

## Limitation
There are a few limitations on the model and how it was developed that could be corrected in future studies or attempts to improve its accuracy and practicality. These include:
1. The model was trained and tested on a relatively small dataset. This creates a risk where it performs much worse on other unseen data with unseen patterns.
2. For the same reason, the cases where the model made wrong prediction constitute a very small sample. It makes it hard to establish of a pattern in wrong predictions to enhance the model further.
3. The target variable's is loosely understood as there is not much documentation on it. If the presumptions on how it is made are not correct, it is vital to revise how the model and its results are interpreted.
4. The model development process is fairly simple and computationally-inexpensive. More intricate and complex methods and processes could be applied to further enhance its predictive power.
