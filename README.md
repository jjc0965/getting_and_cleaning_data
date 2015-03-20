TITLE: README for Coursera Getting and Cleaning Data Course Project - Describes Variables


"activity_labels" imports the different types of activities (6 different types) into R.

"features" reads the features data (i.e., "tBodyAcc-mean()-X") into R.

"train_set" reads X-train data (training set) into R.

"train_labels" reads training labels (1-6) into R.

"train_subject" reads subject who performed the training activity (1-30) into R.

"test_set" reads X-test data (test set) into R.

"test_labels" reads test labels (1-6) into R.

"test_subject" reads subject who performed the test activity (1-30) into R.

"combined_set" combines train and test sets.

"combined_labels" combines train and test labels.

"combined_subject" combines train and test subjects.

"features_mean_only" is a vector of integers - selects only the features data containing "mean".
   I am eliminating all fields with "meanFreq", by doing this, as these are not truly means.

"features_std_only" is a vector of integers - selects only the features data containing "std" - 
   same rationale as above.

"features_mean_or_std" is a vector of integers - selects only the features data containing either "mean" or "std".

"set" is the working data set - columns combined and only means and stds included.

"tidydata" gets aggregate of data by test subject ID and activity.

The data is then written to a file named "tidydata.txt".

"data_final" reads the "tidydata.txt" file back into R.
