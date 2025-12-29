Data Science Certificate Program - Foundations Course - Assignment 4

In this assignment, you will practice using the kNN (k-Nearest Neighbors) algorithm to solve a classification problem. The kNN is a simple and robust classifier, which is used in different applications.

We will use the Iris dataset for this assignment. The dataset was first introduced by statistician R. Fisher and consists of 50 observations from each of three species Iris (Iris setosa, Iris virginica and Iris versicolor). For each sample, 4 features are given: the sepal length and width, and the petal length and width.

The goal is to train kNN algorithm to distinguish the species from one another.

The dataset can be downloaded from UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/machine-learning-databases/iris/.

Download iris.data file from the Data Folder. The Data Set description with the definitions of all the columns can be found on the dataset page - https://archive.ics.uci.edu/ml/datasets/Iris. Alternatively, you can import the data using sklearn.datasets. You will need to dowload both the sepal/petal data and the target variable information, then merge the two datasets.

(1 points) Load the data from the file (iris.data) into the DataFrame. Set the names of columns according to the column definitions given in Data Description.

(2 points) Data inspection.

Display the first 5 rows of the dataset and use any relevant functions that can help you to understand the data.
Prepare 2 scatter plots - sepal_width vs sepal_length and petal_width vs petal_length. Scatter plots should show each class in different color (seaborn.lmplot is recommended for plotting).
(2 points) Prepare the data for classification.

Using the pandas operators prepare the feature variables X and the response Y for the fit. Note that sklean expects data as arrays, so convert extracted columns into arrays.
(1 point) Split the data into train and test using sklearn train_test_split function.

(2 points) Run the fit using KNeighborsClassifier from sklearn.neighbors.

First, instantiate the model,
Then, run the classifier on the training set.
(3 points) Use learning model to predict the class from features, run prediction on X from test part.

Show the accuracy score of the prediction by comparing predicted iris classes and the Y values from the test.
Comparing these two arrays (predicted classes and test Y), count the numbers of correct predictions and predictions that were wrong. (HINTS: NumPy arrays can be compared using == operator. You can also use NumPy's operator count_nonzero to count number of non-False values).
(4 points) In this task, we want to see how accuracy score and the number of correct predictions change with the number of neighbors k. We will use the following number of neighbors k: 1, 3, 5, 7, 10, 20, 30, 40, and 50:

Generate 10 random train/test splits for each value of k
Fit the model for each split and generate predictions
Average the accuracy score for each k
Calculate the average number of correct predictions for each k as well
Plot the accuracy score for different values of k. What conclusion can you make based on the graph?
