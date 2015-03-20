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

___________________________________________________________________________________________________________




The actual code is listed here:

run_analysis.R

## 1) READS DATA INTO R

activity_labels<-read.table("UCI HAR Dataset/activity_labels.txt")  
## Imports the different types of activities into R
features<-read.table("UCI HAR Dataset/features.txt")  
##  Reads the features data (i.e., "tBodyAcc-mean()-X") into R

train_set<-read.table("UCI HAR Dataset/train/X_train.txt")  
## Reads X-train data (training set) into R
train_labels<-read.table("UCI HAR Dataset/train/y_train.txt")  
## Reads training labels (1-6) into R
train_subject<-read.table("UCI HAR Dataset/train/subject_train.txt")  
## Reads subject who performed the training activity (1-30) into R

test_set<-read.table("UCI HAR Dataset/test/X_test.txt")  
## Reads X-test data (test set) into R
test_labels<-read.table("UCI HAR Dataset/test/y_test.txt")  
## Reads test labels (1-6) into R
test_subject<-read.table("UCI HAR Dataset/test/subject_test.txt")  
## Reads subject who performed the test activity (1-30) into R

## 2) COMBINES TRAIN AND TEST DATA

combined_set<-rbind(train_set, test_set)  
##  Combines train and test sets
combined_labels<-rbind(train_labels, test_labels)  
##  Combines train and test labels
combined_subject<-rbind(train_subject, test_subject)  
##  Combines train and test subjects

## 3) EXTRACTS ONLY FEATURES WHICH ANALYZE MEANS OR STANDARD DEVIATIONS

features_mean_only<-grep("-mean()", as.character(features$V2), fixed=TRUE)  
## A vector of integers - selects only the features data containing "mean".  
## Setting fixed=TRUE does not allow () to be interpreted as a metacharacter.  
## I am eliminating all fields with "meanFreq", by doing this, as these are not truly means
features_std_only<-grep("-std()", as.character(features$V2), fixed=TRUE)  
## A vector of integers - selects only the features data containing "std" - same rationale as above

features_mean_or_std<-sort(c(features_mean_only, features_std_only))  
## A vector of integers - selects only the features data containing either "mean" or "std"

## 4) CREATES FINAL WORKING DATA SET - NAMED "set"

set<-cbind(combined_subject, combined_labels, combined_set[features_mean_or_std])  
## the set we will be working with with columns combined and only means and stds included
## short name for this reason

## 5) CREATION OF TIDY DATA SET

tidydata<-aggregate(set[3:68], by=set[1:2], mean)  
##  Gets aggregate of data by test subject ID and activity
colnames(tidydata)<-c("Subject.ID", "Activity", as.character(features[features_mean_or_std,2]))  
## Labels all columns
tidydata<-tidydata[with(tidydata, order(Subject.ID, Activity)), ]  
## Puts the data in order by "Subject.ID and "Activity"
rownames(tidydata)<-NULL
tidydata[,"Activity"]<-activity_labels[tidydata[,"Activity"],2]  
##  Puts text of activity in column 2 (labeled "Activity") of the output

## 6) WRITES TABLE TO "tidydata.txt"

write.table(tidydata, file="tidydata.txt", sep="\t")  
## Writes the data to a file named "tidydata.txt", not incorporating row.names

## 7) READS DATA FROM "tidydata.txt" BACK TO "data_final"

data_final<-read.table("tidydata.txt")  
##Reads the "tidydata.txt" file back into R
View(data_final)