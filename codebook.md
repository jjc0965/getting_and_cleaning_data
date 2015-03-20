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
33 of which were mean and 33 of which were standard deviation (std).  

Original files are listed below this list of the 66 included feature variables.

Legend: 
std = "standard deviation"
fds = "frequency domain signals"

1) tBodyAcc-mean()-X 			(mean time - body acceleration signal - X axis)

2) tBodyAcc-mean()-Y 			(mean time - body acceleration signal - Y axis)

3) tBodyAcc-mean()-Z 			(mean time - body acceleration signal - Z axis)

4) tBodyAcc-std()-X 			(std time - body acceleration signal - X axis)

5) tBodyAcc-std()-Y 			(std time - body acceleration signal - Y axis)

6) tBodyAcc-std()-Z			(std time- body acceleration signal - Z axis)

7) tGravityAcc-mean()-X 		(mean time - gravity acceleration signal - X axis)

8) tGravityAcc-mean()-Y 		(mean time - gravity acceleration signal - Y axis)

9) tGravityAcc-mean()-Z 		(mean time - gravity acceleration signal - Z axis)

10) tGravityAcc-std()-X 		(std time - gravity acceleration signal - X axis)

11) tGravityAcc-std()-Y 		(std time - gravity acceleration signal - Y axis)

12) tGravityAcc-std()-Z			(std time - gravity acceleration signal - Z axis)

13) tBodyAccJerk-mean()-X 		(mean time - body linear acceleration Jerk signal - X axis)

14) tBodyAccJerk-mean()-Y 		(mean time - body linear acceleration Jerk signal - Y axis)

15) tBodyAccJerk-mean()-Z 		(mean time - body linear acceleration Jerk signal - Z axis)

16) tBodyAccJerk-std()-X 		(std time - body linear acceleration Jerk signal - X axis)

17) tBodyAccJerk-std()-Y 		(std time - body linear acceleration Jerk signal - Y axis)

18) tBodyAccJerk-std()-Z		(std time - body linear acceleration Jerk signal - Z axis)

19) tBodyGyro-mean()-X 			(mean time - body angular velocity signal - X axis)

20) tBodyGyro-mean()-Y 			(mean time - body angular velocity signal - Y axis)

21) tBodyGyro-mean()-Z 			(mean time - body angular velocity signal - Z axis)

22) tBodyGyro-std()-X 			(std time - body angular velocity signal - X axis)

23) tBodyGyro-std()-Y 			(std time - body angular velocity signal - Y axis)

24) tBodyGyro-std()-Z 			(std time - body angular velocity signal - Z axis)

25) tBodyGyroJerk-mean()-X		(mean time - body angular velocity Jerk signal - X axis)

26) tBodyGyroJerk-mean()-Y 		(mean time - body angular velocity Jerk signal - Y axis)

27) tBodyGyroJerk-mean()-Z 		(mean time - body angular velocity Jerk signal - Z axis)

28) tBodyGyroJerk-std()-X 		(std time - body angular velocity Jerk signal - X axis)

29) tBodyGyroJerk-std()-Y 		(std time - body angular velocity Jerk signal - Y axis)

30) tBodyGyroJerk-std()-Z 		(std time - body angular velocity Jerk signal - Z axis)

31) tBodyAccMag-mean()			(mean time - body linear acceleration magnitude 3D signals)

32) tBodyAccMag-std() 			(std time - body linear acceleration magnitude 3D signals)

33) tGravityAccMag-mean() 		(mean time - gravity linear acceleration magnitude 3D signals)

34) tGravityAccMag-std() 		(std time - gravity linear acceleration magnitude 3D signals)

35) tBodyAccJerkMag-mean() 		(mean time - body linear acceleration Jerk magnitude - 3D signals)

36) tBodyAccJerkMag-std() 		(std time - body linear acceleration Jerk magnitude - 3D signals)

37) tBodyGyroMag-mean()			(mean time - body angular velocity magnitude - 3D signals)

38) tBodyGyroMag-std() 			(std time - body angular velocity magnitude - 3D signals)

39) tBodyGyroJerkMag-mean() 		(mean time - body angular velocity Jerk magnitude - 3D signals)

40) tBodyGyroJerkMag-std() 		(std time - body angular velocity Jerk magnitude - 3D signals)

41) fBodyAcc-mean()-X 			(mean fds - body acceleration signal - X axis)

42) fBodyAcc-mean()-Y 			(mean fds - body acceleration signal - Y axis)

43) fBodyAcc-mean()-Z 			(mean fds - body acceleration signal - Z axis)

44) fBodyAcc-std()-X			(std fds - body acceleration signal - X axis)

45) fBodyAcc-std()-Y 			(std fds - body acceleration signal - Y axis)

46) fBodyAcc-std()-Z 			(std fds - body acceleration signal - Z axis)

47) fBodyAccJerk-mean()-X 		(mean fds - body linear acceleration Jerk signal - X axis)

48) fBodyAccJerk-mean()-Y 		(mean fds - body linear acceleration Jerk signal - Y axis)

49) fBodyAccJerk-mean()-Z 		(mean fds - body linear acceleration Jerk signal - Z axis)

50) fBodyAccJerk-std()-X 		(std fds - body linear acceleration Jerk signal - X axis)

51) fBodyAccJerk-std()-Y		(std fds - body linear acceleration Jerk signal - Y axis)

52) fBodyAccJerk-std()-Z 		(std fds - body linear acceleration Jerk signal - Z axis)

53) fBodyGyro-mean()-X 			(mean fds - body angular velocity signal - X axis)

54) fBodyGyro-mean()-Y 			(mean fds - body angular velocity signal - Y axis)

55) fBodyGyro-mean()-Z 			(mean fds - body angular velocity signal - Z axis)

56) fBodyGyro-std()-X 			(std fds - body angular velocity signal - X axis)

57) fBodyGyro-std()-Y 			(std fds - body angular velocity signal - Y axis)

58) fBodyGyro-std()-Z			(std fds - body angular velocity signal - Z axis)

59) fBodyAccMag-mean() 			(mean fds - body linear acceleration magnitude 3D signals)

60) fBodyAccMag-std() 			(std fds - body linear acceleration magnitude 3D signals)

61) fBodyBodyAccJerkMag-mean() 		(mean fds - body linear acceleration Jerk magnitude - 3D signals)

62) fBodyBodyAccJerkMag-std() 		(std fds - body linear acceleration Jerk magnitude - 3D signals)

63) fBodyBodyGyroMag-mean() 		(mean fds - body angular velocity magnitude - 3D signals)

64) fBodyBodyGyroMag-std()		(std fds - body angular velocity magnitude - 3D signals)

65) fBodyBodyGyroJerkMag-mean() 	(mean fds - body angular velocity Jerk magnitude - 3D signals)

66) fBodyBodyGyroJerkMag-std()		(std fds - body angular velocity Jerk magnitude - 3D signals)


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