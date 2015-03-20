TITLE: CODEBOOK for Coursera Getting and Cleaning Data Course Project


-- Subject.ID - patients are labeled as subjects 1-30.


-- Activity - There are 6 activies, which were contained in "UCI HAR Dataset/activity_labels.txt"

1 WALKING

2 WALKING_UPSTAIRS


3 WALKING_DOWNSTAIRS


4 SITTING


5 STANDING


6 LAYING



After removing features not containing means or standard deviations, we are left with 66 feature variables, 
33 means and 33 standard deviations.  Original files are listed below the list of 66 included variables.

1) tBodyAcc-mean()-X 

2) tBodyAcc-mean()-Y 

3) tBodyAcc-mean()-Z 

4) tBodyAcc-std()-X 

5) tBodyAcc-std()-Y 

6) tBodyAcc-std()-Z

7) tGravityAcc-mean()-X 

8) tGravityAcc-mean()-Y 

9) tGravityAcc-mean()-Z 

10) tGravityAcc-std()-X 

11) tGravityAcc-std()-Y 

12) tGravityAcc-std()-Z

13) tBodyAccJerk-mean()-X 

14) tBodyAccJerk-mean()-Y 

15) tBodyAccJerk-mean()-Z 

16) tBodyAccJerk-std()-X 

17) tBodyAccJerk-std()-Y 

18) tBodyAccJerk-std()-Z

19) tBodyGyro-mean()-X 

20) tBodyGyro-mean()-Y 

21) tBodyGyro-mean()-Z 

22) tBodyGyro-std()-X 

23) tBodyGyro-std()-Y 

24) tBodyGyro-std()-Z 

25) tBodyGyroJerk-mean()-X

26) tBodyGyroJerk-mean()-Y 

27) tBodyGyroJerk-mean()-Z 

28) tBodyGyroJerk-std()-X 

29) tBodyGyroJerk-std()-Y 

30) tBodyGyroJerk-std()-Z 

31) tBodyAccMag-mean()

32) tBodyAccMag-std() 

33) tGravityAccMag-mean() 

34) tGravityAccMag-std() 

35) tBodyAccJerkMag-mean() 

36) tBodyAccJerkMag-std() 

37) tBodyGyroMag-mean()

38) tBodyGyroMag-std() 

39) tBodyGyroJerkMag-mean() 

40) tBodyGyroJerkMag-std() 

41) fBodyAcc-mean()-X 

42) fBodyAcc-mean()-Y 

43) fBodyAcc-mean()-Z 

44) fBodyAcc-std()-X

45) fBodyAcc-std()-Y 

46) fBodyAcc-std()-Z 

47) fBodyAccJerk-mean()-X 

48) fBodyAccJerk-mean()-Y 

49) fBodyAccJerk-mean()-Z 

50) fBodyAccJerk-std()-X 

51) fBodyAccJerk-std()-Y

52) fBodyAccJerk-std()-Z 

53) fBodyGyro-mean()-X 

54) fBodyGyro-mean()-Y 

55) fBodyGyro-mean()-Z 

56) fBodyGyro-std()-X 

57) fBodyGyro-std()-Y 

58) fBodyGyro-std()-Z

59) fBodyAccMag-mean() 

60) fBodyAccMag-std() 

61) fBodyBodyAccJerkMag-mean() 

62) fBodyBodyAccJerkMag-std() 

63) fBodyBodyGyroMag-mean() 

64) fBodyBodyGyroMag-std()

65) fBodyBodyGyroJerkMag-mean() 

66) fBodyBodyGyroJerkMag-std()


-- "UCI HAR Dataset/features.txt" contains all feature variables.  They are derived as follows:

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals 
tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a 
constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass 
Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration 
signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) 
using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk 
signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals 
were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, 
tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, 
fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to 
indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ 

tGravityAcc-XYZ 

tBodyAccJerk-XYZ 

tBodyGyro-XYZ 

tBodyGyroJerk-XYZ 

tBodyAccMag 

tGravityAccMag 

tBodyAccJerkMag 

tBodyGyroMag 

tBodyGyroJerkMag
 
fBodyAcc-XYZ 

fBodyAccJerk-XYZ 

fBodyGyro-XYZ 

fBodyAccMag 

fBodyAccJerkMag 

fBodyGyroMag 

fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 

mean(): Mean value 

std(): Standard deviation 

mad(): Median absolute deviation 

max(): Largest value in array 

min(): Smallest value in array 

sma(): Signal magnitude area 

energy(): Energy measure. Sum of the squares divided by the number of values 

iqr(): Interquartile range 

entropy(): Signal entropy 

arCoeff(): Autorregresion coefficients with Burg order equal to 4
 
correlation(): correlation coefficient between two signals 

maxInds(): index of the frequency component with largest magnitude
 
meanFreq(): Weighted average of the frequency components to obtain a mean frequency 

skewness(): skewness of the frequency domain signal 

kurtosis(): kurtosis of the frequency domain signal 

bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window 

angle(): Angle between to vectors

Only "mean()" and "std()" were used for the course project - all other columns of data were deleted.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the 
angle() variable:

gravityMean

tBodyAccMean

tBodyAccJerkMean

tBodyGyroMean

tBodyGyroJerkMean

None of these were used as they were not true means or stds.


-- "UCI HAR Dataset/train/X_train.txt"

Contains the data for the 70% of volunteers that were selected for generating the training data.
There were 7352 observations of 561 variables in this group.


-- "UCI HAR Dataset/train/y_train.txt"

Contains the labels (1-6) for the volunteers in the "training" group.  These are translated into text
using the conversion table in the file, "UCI HAR Dataset/activity_labels.txt", as above.


-- "UCI HAR Dataset/train/subject_train.txt"

Contains the subject who performed the training activity (1-30).


-- "UCI HAR Dataset/test/X_test.txt"

Contains the data for the 30% of volunteers that were selected for generating the test data.
There were 2947 observations of 561 variables in this group.


-- "UCI HAR Dataset/test/y_test.txt"

Contains the labels (1-6) for the volunteers in the "test" group.  These are translated into text
using the conversion table in the file, "UCI HAR Dataset/activity_labels.txt", as above.


-- "UCI HAR Dataset/test/subject_test.txt"

Contains the subject who performed the test activity (1-30).


NOTE:  The Inertial Signals data was not used as there were no means or standarad deviations in this group