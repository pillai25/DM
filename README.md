**Practical No 2
**
Data Import and Dataset Understanding
Import datasets (CSV/ARFF) in WEKA, examine attributes, summary statistics, and visualize
data using preprocessing tools

Step 1
Open WEKA GUI Chooser.
Step 2
Click Explorer.
Step 3
Select the Preprocess tab.
Step 4
Click Open File.
Step 6
Dataset loads successfully.
Observe: ● Relation Name
● Number of Instances
● Number of Attributes
● Attribute Names
● Class Attribute

Part B: Import CSV Dataset

Part C: Examine Dataset Attributes
On the left side of the Preprocess window, click each attribute one by one.
Example
Attribute 1
SepalLength

Observe  ● Type
● Missing values
● Distinct values
● Minimum value
● Maximum value
● Mean
● Standard Deviation

Part D:
Select Class

Part E: Visualize Dataset
Step 1: Visualize All

Step 2
Scatter plots appear.
Each graph represents
Attribute vs Attribute

Part F: Examine Histograms
Click any attribute.
Histogram appears on the right side.
Observe
● Frequency Distribution
● Minimum
● Maximum
● Missing values

**Practical No. 3
**

Data Preprocessing Techniques
Perform preprocessing tasks such as handling missing values, normalization, discretization, and
filtering attributes using WEKA filters.

Step 1: Load Dataset
Dataset saved as studentperformance.arff
@relation student_performance
@attribute age numeric
@attribute gender {Male, Female}
@attribute study_time_weekly numeric
@attribute absences numeric
@attribute tutoring {Yes, No}
@attribute parental_support {Low, Medium, High}
@attribute grade_class {Pass, Fail}
@data
16, Female, 12.5, 3, Yes, High, Pass
17, Male, 5.0, 14, No, Low, Fail
15, Male, 8.5, 6, No, Medium, Pass
18, Female, 10.0, 9, Yes, Medium, Pass
16, Male, 3.0, 22, No, Low, Fail
17, Female, 15.0, 2, Yes, High, Pass

Open WEKA → Explorer.
Go to the Preprocess tab.
Click Open file → select your dataset

Choose a filter
● In the Preprocess tab, click Choose under Filter.
● ReplaceMissingValues → Handles missing values automatically. ○
unsupervised → attribute → ReplaceMissingValues

● Normalize → Scales numeric attributes to [0,1].
● Standardize → Converts numeric attributes to mean = 0, std. dev. = 1.
○ unsupervised → attribute → Standardize
Discretize:

**Practical 4
**
Data Cleaning and Transformation
Apply attribute selection, remove noisy data, transform datasets using filters such as
Remove, ReplaceMissingValues, and Normalize.
● You can include/exclude attributes:
○ Select an attribute → click Remove (e.g., remove ID or Name if they are not
useful).

Click Choose under Filter.
Click the filter name (Remove) to edit options.
Enter the attribute index.
Click Apply.

Remove Noisy Data
Noisy attributes can be removed manually.

The selected attribute is removed.

Attribute Selection
Attribute Selection helps choose the most relevant features.
Go to Choose. Select Attribute Selection from Supervised.

Click Apply.


Practical 5

Association Rule Mining using Apriori
Apply the Apriori algorithm to generate association rules. Analyze support, confidence, and lift
values. Perform a Market Basket Analysis case study.

Association Rule Mining is a data mining technique used to discover interesting relationships
between items in a dataset. It is commonly used in Market Basket Analysis, where retailers
identify products that are frequently purchased together.
The Apriori Algorithm generates frequent itemsets based on a minimum support threshold and
then creates association rules that satisfy a minimum confidence threshold.

1. Launch WEKA.
2. Click Explorer.
3. Open the Preprocess tab.

4.Click Open File.
5. Select the Market Basket dataset (marketbasket.arff or CSV).
6. Verify that all attributes are loaded correctly.

1. Click the Associate tab.
2. Click the Choose button.
Select:
Associations → Apriori

Click Start.

WEKA processes the dataset and displays the generated association rules.


**=Practical No. 6
**
To implement the Decision Tree (J48) classification algorithm in WEKA, train
and test the model using different datasets, and analyze the classification results.

Step 1: Open WEKA
1. Launch WEKA.
2. Click Explorer.

Step 2: Load Dataset
1. Click Open File.
2. Navigate to:

data → weather.nominal.arff

3. Select weather.nominal.arff
4. Click Open.
The dataset summary will appear on the left side.

Step 3: Check Class Attribute
1. Ensure the Class attribute is selected.
2. For Iris dataset, the class attribute is:
class
3. It contains three classes:
1. Sunny
2. Overcast
3. Rainy

Step 4: Go to Classify Tab
Click
Classify

Step 5: Choose Classifier
Click
Choose
Navigate to
trees
↓
J48
Select J48.

Step 6: Set Testing Option
Choose one of the following:
Option 1 (Recommended)
10-Fold Cross Validation
Leave it as default.
OR
Option 2
Percentage Split

Step 7: Start Training
Click
Start
WEKA builds the Decision Tree.

Output
The Result List displays:


Practical N0. 7
To implement Naïve Bayes and IBk (k-Nearest Neighbors) classification algorithms in WEKA,
evaluate their performance using different datasets, and compare the results using evaluation
metrics.

A) Naive Bayes

Step 1: Open WEKA
1. Launch WEKA.
2. Click Explorer.

Step 2: Load Dataset
1. Click Open File.
2. Select iris.arff.
3. Click Open.
The dataset summary will appear.

Step 3: Verify Class Attribute
Ensure the class attribute is:
Class

Step 4: Open Classify Tab
Click the Classify tab.

Step 5: Select Naïve Bayes
1. Click Choose.
2. Navigate to:
bayes
↓
NaiveBayes
3. Select NaiveBayes.

Step 6: Select Test Option
Choose:
10-Fold Cross Validation
(Default option)
OR
Percentage Split (66%)

Step 7: Train the Model
Click
Start

Step 8: Observe Results
WEKA displays:
● Correctly Classified Instances
● Incorrectly Classified Instances
● Kappa Statistic
● Mean Absolute Error
● Root Mean Squared Error
● Precision
● Recall
● F-Measure
● ROC Area
● Confusion Matrix


B) k-NN Classification (IBk)
Step 1: Open the Same Dataset
Load iris.arff.

Step 2: Open Classify Tab
Click Classify.

Step 3: Select IBk
Click
Choose
Navigate to
lazy
↓
IBk

Select IBk.

Step 4: Set Value of K
Click on IBk.
Set
K = 3
(or leave the default value if preferred).
Click OK.

Step 5: Select Test Option
Choose
10-Fold Cross Validation

Step 6: Train Model
Click
Start

Step 7: Observe Output
WEKA displays:
● Accuracy
● Precision
● Recall
● F-Measure
● ROC Area
● Confusion Matrix

**Practical 8
**
Model Evaluation Techniques
Evaluate classification models using accuracy, precision, recall, F-measure, and confusion matrix
with cross-validation

Step 1: Open WEKA
1. Launch WEKA.
2. Click Explorer.

Step 2: Load Dataset
1. Click Open File.
2. Select a dataset (e.g., iris.arff).

3. The dataset summary appears.
4. Ensure the Class Attribute is correctly selected (usually the last attribute).

Step 3: Go to the Classify Tab
1. Click the Classify tab.
2. Click the Choose button.

Step 4: Select a Classification Algorithm
Choose any classifier such as:
● Trees → J48
● Bayes → NaiveBayes
● Lazy → IBk (k-NN)
Example:
Choose → Trees → J48

Step 5: Select Evaluation Method
Under Test Options, select:
Cross-validation
Set:
Number of folds = 10
This performs 10-Fold Cross Validation.

Step 6: Start Classification
Click Start.
WEKA trains and tests the model.

Step 7: Observe the Results
The output window displays:
● Correctly Classified Instances
● Incorrectly Classified Instances
● Kappa Statistic
● Mean Absolute Error
● Root Mean Squared Error
● Precision
● Recall
● F-Measure
● Confusion Matrix


**Practical 9
**
Clustering using K-Means
Perform clustering using the SimpleKMeans algorithm and analyze cluster formation with
visualization tools.

Step 1: Open WEKA
1. Launch WEKA.
2. Click Explorer.

Step 2: Load the Dataset
1. Click Open File.
2. Select the dataset (e.g., iris.arff).
3. The dataset summary will appear in the Preprocess tab.

Step 3: Remove the Class Attribute (Optional)
Since K-Means is an unsupervised learning algorithm, it does not require a class label.

1. In the Preprocess tab, select the class attribute (e.g., class in Iris).
2. Click Remove if you want to perform pure clustering.
○ (Alternatively, you can leave the class attribute and ignore it during clustering.)


Step 4: Go to the Cluster Tab
1. Click the Cluster tab.
2. Click the Choose button.

Step 5: Select the SimpleKMeans Algorithm
Navigate to:
Choose → weka → clusterers → SimpleKMeans
Click SimpleKMeans.


Step 6: Configure the Algorithm
Click the algorithm name (SimpleKMeans) to modify its parameters.
Set the following:
Parameter                         Value
Number of Clusters (numClusters)    3
Distance Function                EuclideanDistance
Seed                               10
Preserve Order                   False

Click OK.

Step 7: Select Cluster Evaluation Mode
Under Cluster Mode, choose:
● Classes to Clusters Evaluation (if the dataset contains class labels), or
● Use Training Set (for unlabeled datasets).

Step 8: Run the Algorithm
Click Start.
WEKA performs clustering and displays the results.

Step 9: Observe the Output
The output window displays:
● Number of clusters
● Cluster centroids
● Number of instances in each cluster
● Within-cluster sum of squared errors
● Cluster assignments

Step 10: View Cluster Centroids
WEKA displays the centroid values for each cluster.

The centroid represents the average values of all instances in that cluster.
Step 11: Visualize the Clusters

1. After clustering, right-click the result in the Result List.
2. Select Visualize Cluster Assignments.
3. A scatter plot window opens.
4. Choose attributes for the X-axis and Y-axis (e.g., Petal Length and Petal Width).
5. Each cluster is displayed in a different color.
6. Observe how similar data points are grouped into clusters.

Step 12: Analyze the Results
Check the following:
● Number of clusters formed.
● Number of instances in each cluster.
● Cluster centroids.
● Distribution of data points.
● Separation between clusters.
● Whether similar instances are grouped


**Practical 10
**
Density-Based Clustering (DBSCAN) and Use Case
Implement density-based clustering in WEKA and analyze customer segmentation datasets.

Step 1: Open WEKA
1. Launch WEKA.
2. Click Explorer.

Step 2: Load the Dataset
1. Click Open File.
2. Select the customer dataset.
3. The dataset summary will appear in the Preprocess tab.

Step 3: Preprocess the Dataset (Optional)
1. Check for missing values.
2. Normalize the numeric attributes (recommended for DBSCAN).
3. Remove unnecessary attributes such as Customer ID if required.

Step 4: Open the Cluster Tab
1. Click the Cluster tab.
2. Click Choose.

Step 5: Select the DBSCAN Algorithm
Navigate to:
Choose → weka → clusterers → DBSCAN
Select DBSCAN.

Step 6: Configure DBSCAN Parameters
Click DBSCAN to edit the parameters.
Set the following values:
Parameter Example Value
Epsilon (epsilon) 0.9
Minimum Points (minPoints) 6
Database Type SequentialDatabase

Click OK.

Parameter Description

● Epsilon (ε): Maximum distance between neighboring points.
● MinPoints: Minimum number of neighboring points required to form a dense cluster.

Step 7: Select Cluster Mode
Choose one of the following:
● Use Training Set
● Classes to Clusters Evaluation (if the dataset contains class labels)

Step 8: Run DBSCAN
Click Start.
WEKA executes the DBSCAN algorithm.

Step 9: Observe the Output
The output window displays:
● Number of clusters formed
● Number of noise (outlier) instances
● Cluster assignments
● Cluster statistics


Step 10: Visualize Cluster Assignments
1. Right-click the result in the Result List.
2. Select Visualize Cluster Assignments.
3. A scatter plot opens.
4. Select suitable attributes for the X-axis and Y-axis.
5. Observe:
○ Different clusters shown in different colors.
○ Noise or outlier points displayed separately.

Step 11: Analyze the Results
Observe the following:
● Number of clusters created.
● Number of noise (outlier) points detected.
● Distribution of customers across clusters.
● Separation between dense regions.
● Whether customers with similar characteristics are grouped together.





