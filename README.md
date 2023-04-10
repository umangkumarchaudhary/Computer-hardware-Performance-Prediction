# Computer-hardware-Performance-Prediction

This is a script in Python that performs several regression and classification models on a dataset.

The script starts by importing the necessary libraries: pandas, numpy, and matplotlib. Then, it reads a dataset from a file named "cpudata.data" into a pandas dataframe. The file is a tab-separated file, without headers, with missing values represented by "0". The script prints the number of missing values in each column of the dataframe and removes the first two columns (using axis=1) since they do not contain relevant information. After that, it assigns new column numbers based on the shape of the dataframe.

Next, the script replaces the missing values in the dataframe with the mean value of each column using the SimpleImputer from the sklearn.impute library. Then, the script normalizes the data using the MinMaxScaler from the sklearn.preprocessing library. It assigns the last column of the dataframe to a variable called target and the rest of the columns to a variable called data.

After that, the script uses the train_test_split function from the sklearn.model_selection library to split the data into training and testing sets, with a test size of 0.3. Then, the script applies four regression models to the data: KNN, SVM, Decision Tree, and Linear Regression, using the appropriate libraries from the sklearn library. The script calculates the Mean Squared Error (MSE) and the R2 score for each model, and prints them on the screen.

Next, the script applies a Logistic Regression model to the dataset, using the LogisticRegression library from sklearn.linear_model. The script converts the target variable to binary values (0 and 1) based on the median value of the target variable. Then, the script splits the data into training and testing sets, with a test size of 0.3. The script fits the logistic regression model to the training data and makes predictions on both the training and testing data. Finally, the script calculates the accuracy of the model on the training and testing data and prints them on the screen.

Finally, the script plots the actual versus predicted values for each regression model using matplotlib. It creates a 2x2 subplot, with one subplot for each regression model. In each subplot, it plots the actual values on the x-axis and the predicted values on the y-axis, with the training data in blue and the testing data in orange. It also adds a diagonal line to represent the perfect prediction.
