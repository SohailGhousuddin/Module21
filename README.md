### Project Title
Semicondutor process optimization 

**Author**
Sohail Mohammed
www.linkedin.com/in/sohailghousuddin

#### Executive summary
In the complex and highly monitored field of semi-conductor manufacturing, engineers are often overwhelmed by the vast amount of data collected from various sensors and process measurement points. This data, although rich with potentially valuable insights, often includes a significant amount of irrelevant information and noise, obscuring the critical signals necessary for process optimization.

This project aims to develop a predictive model that leverages advanced feature selection techniques to identify the most relevant signals. By concentrating on these key features, the model will facilitate a streamlined and cost-effective manufacturing process. The primary benefits of this approach include cost optimization and reduced time-to-market, empowering process engineers to complete experiments more quickly and efficiently.

#### Rationale
Why should anyone care about this question?
Following are the two major benifits 
1. Cost optimization
2. Time to market 

#### Research Question
What are you trying to answer?
Semi-conductor manufacturing involves continuous monitoring of numerous signals, which include useful information interspersed with noise and irrelevant data. Engineers currently face the challenge of discerning the critical signals from the non-essential ones, leading to inefficiencies in the process.

Feature Selection: Utilize advanced feature selection methods to identify the most relevant signals.

Cost Optimization: Reduce costs by focusing on the key features that drive the desired outcomes.

Time-to-Market: Accelerate the experimental process, enabling quicker decision-making and implementation.

Process Improvement: Enhance throughput and decrease learning time by isolating and utilizing the most impactful signals.


#### Data Sources
What data will you use to answer you question?
https://archive.ics.uci.edu/dataset/179/secom


#### Methodology
What methods are you using to answer the question?

Method:
1. Read the data 
2. use info/describe and data analysis methods to get feel of data
3. Check for null values in each column and drop columns which has 60% or more null values
4. Drop columns who has only one value and see if it gives always positive result, which means this attribute may be important
5. use impute methods to fill the missing data 
6. use correlation/collineraity and drop attributs which are related and has less feature importance 
7.  use the following feature selection techniques and modeling to predict the accuracy and important features required to model 

Feature Importance: Determine the relevance of each feature using tree-based models like Random Forests.

Recursive Feature Elimination (RFE): Iteratively select features by training the model and pruning least significant features.

Principal Component Analysis (PCA): Reduce dimensionality by transforming features into principal components.

L1 Regularization: Apply Lasso regression to select features by shrinking less important feature weights to zero.

Tree-based Methods: Deploy Decision Trees and ensemble methods like Random Forests and Gradient Boosting for feature importance evaluation.

#### Results
What did your research find?
1. Reduce the attributes from ~550 to ~ 240 post data exploration and exploitation 
2. Looks like we need 10 attributes to predict the results with 92.5 accuracy 

The implementation of this predictive model will not only optimize costs but also significantly enhance the efficiency and effectiveness of the semi-conductor manufacturing process. By employing advanced feature selection techniques, process engineers will be better equipped to identify critical signals, thereby improving overall process performance and accelerating innovation.


#### Next steps
What suggestions do you have for next steps?
1. We can combine the results of different models and see if we can improve the accuracy
2. The target value were not balanced, if we can get balanced target values the accuracy can be improved lot. 
3. In case we cannot get balanced dataset we can use some Feature engineering methods to normalize the data and perform the same excercise

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
sohail.ghousuddin@gmail.com