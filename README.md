DecisionTree.ipynb- contains a general class for decision tree classification that can be applied to any sufficiently clean pandas data set with both categorical and numerical features.
This file also loads the titanic dataset after my preprocessing. I train one tree on the dataset, using 5-fold cross-validation (the data set only has 1000 training points) to tune
the optimal threshold to stop tree growth. This has about 78% predictive power on the kaggle titanic test set. Then I train a random forest using this class, this performs about 82%
predictive power on the training data.

Titanic_Processing.ipynb- this is where the titanic data is preprocessed. Some choices I make are dropping the ticket number column, binning the cabin numbers by their leading letter 
(I keep the NAs), bin the age groups into larger ranges, and we impute one missing fare by the average of its class. Apply the same cleaning to the test.

titanic_test_cleaned.csv- the cleaned test data to load into DecisionTree.ipynb.

titanic_train_cleaned.csv- the cleaned training data to load into DecisionTree.ipynb.
