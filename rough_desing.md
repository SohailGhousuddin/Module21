Load the data 
Look for constant attributes and drop them 
Look for attributes which has 60% of null values, drop them
Use imputation method to fill the missing data for rest of the fields 
Now that all the attributes are non-null we can try to find the correlation 
Check for outliers and fix them
multi-collinearity , if there is a correlation of +/- 85 then lets drop one of the attribute 
check if we can use PCA (This will be imnplemented in next module)

Check if there are  same combinations of all attributes with different target (This will be imnplemented in next module)

Apart from sequential feature selection, there are several other methods you can use to select the minimum features for your predictive model:

(This will be imnplemented in next module, for now I have used only sequential feature selection)
Filter Methods: These involve statistical techniques to evaluate the relevance of each feature. Common techniques include:
Correlation Coefficient: Measures the linear relationship between features and the target variable.
Chi-Square Test: Evaluates the independence of categorical features from the target variable.
Mutual Information: Measures the dependency between features and the target variable.
Wrapper Methods: These use a predictive model to evaluate the combination of features and select the best subset. Examples include:
Recursive Feature Elimination (RFE): Iteratively removes the least important features based on model performance.
Genetic Algorithms: Uses evolutionary techniques to select the optimal subset of features.
Embedded Methods: These incorporate feature selection as part of the model training process. Examples include:
Lasso Regression: Adds a penalty for the absolute value of the coefficients, effectively shrinking some coefficients to zero.
Tree-based Methods: Decision trees and ensemble methods like Random Forests and Gradient Boosting naturally rank features by importance.
Dimensionality Reduction Techniques: These transform the feature space into a lower-dimensional space while retaining most of the information. Examples include:
Principal Component Analysis (PCA): Transforms features into a set of linearly uncorrelated components.
t-Distributed Stochastic Neighbor Embedding (t-SNE): Useful for visualizing high-dimensional data in a lower-dimensional space.

FS Method (Feature Selection Method):

Purpose: Feature selection methods are used to select a subset of relevant features (variables, predictors) for use in model construction.
Benefits: They help in reducing the dimensionality of the data, improving model performance, and reducing overfitting.
Example: The SelectKBest method in Python's sklearn library selects the top k features based on a scoring function like ANOVA F-value1.

Relief:

Purpose: Relief is a feature selection algorithm that evaluates the importance of features based on how well their values distinguish between instances that are near each other.
Benefits: It is particularly useful for handling noisy and multi-class data.
Example: ReliefF, an extension of the Relief algorithm, is commonly used in bioinformatics for selecting genetic markers2.

Pearson F-test:

Purpose: The Pearson F-test is used to compare variances between groups and is often used in the context of ANOVA (Analysis of Variance).
Benefits: It helps in determining if there are significant differences between group means in a dataset.
Example: In feature selection, it can be used to assess the significance of features by comparing the variance explained by the feature to the variance within the groups3.
Gram-Schmidt Process:

Purpose: The Gram-Schmidt process is a method for orthogonalizing a set of vectors in an inner product space, which is often used in linear algebra.
Benefits: It is used to create an orthonormal basis, which simplifies many mathematical operations and is useful in algorithms like QR decomposition.
Example: In AI, it can be used in dimensionality reduction techniques and to ensure numerical stability in computations


### Different ways to handle missing data in a dataset

- Remove Missing Data:
    - Drop Rows: Remove rows with missing values.
    - Drop Columns: Remove columns with a high percentage of missing values.
- Imputation:
    - Mean/Median/Mode Imputation: Replace missing values with the mean, median, or mode of the column.
    - Forward Fill: Use the previous value to fill the missing data.
    - Backward Fill: Use the next value to fill the missing data.
    - Interpolation: Use interpolation methods to estimate missing values.
- Predictive Modeling:
    - Regression: Use regression models to predict and fill missing values.
    - K-Nearest Neighbors (KNN): Use the KNN algorithm to impute missing values based on the nearest neighbors.
- Using Algorithms that Support Missing Values:
    - Some machine learning algorithms can handle missing values internally, such as decision trees and certain ensemble methods.
- Custom Imputation:
    - Domain-Specific Methods: Use domain knowledge to fill in missing values appropriately.
- Multiple Imputation:
    - Generate multiple imputations for the missing values and combine the results to account for the uncertainty of the missing data.