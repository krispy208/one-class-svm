This is the README.txt for the OneClassSVM implementation, which aims to detect anomalies.

The model is trained on normal data and then tested on both normal and anomalous data.
This implementation utilizies the KDDCUP 10% subset as well as file containing the feature names.

Instructions:

Dataset
Files:
kddcup.names
kddcup.data_10_percent.gz

Run the cells from top to bottom
*Note the hyperparameter tuning will take to execute, under 15 minutes.

Required Libaries:
pandas==2.2.3
numpy==2.2.4
scikit-learn==1.6.1
matplotlib==3.10.0

Here is how to install:
pip install pandas==2.2.3 numpy==2.2.4 scikit-learn==1.6.1 matplotlib==3.10.0

Python version == 3.12.9


1.First,we load in the dataset and manually label the columns with feature name file as the dataset doesn't come labeled.
2.We create binary labels 0 for normal, 1 for attack.
3.Perform one-hot-encoding on the symbolic data.
4.Standardize the numerical features.
5.Split the normal part of dataset into a training and test set.
6.Do hyperparameter tuning and get the best hyperparameters.
7.Lastly, we evaluate the model and get our metrics.

You should be able to see the optimal hyperparameters that the tuning produces both gamma and nu. You should see 2 confusion matrices one based on the entirety of the anomaly data and one based on smaller subset. Below each confusion matrix, there should be evaluation metrics to show how well the model performed.

