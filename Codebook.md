# Code Book

##Transformations performed by the Script

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Units

All units normalized and bounded within [-1,1]

##Variable name cleanup

As part of the tidying process the variable names are cleaned up using the following transformations using the guidelines described in the lesson (lower case, no underscores, descriptive names...):

# get rid of the parenthesis. Since there were no underscores or spaces, nothing else was required. I retained the dashes.
namedFeaturesWanted <- gsub('[()]', '', namedFeaturesWanted)

## Identifiers

* `subject` - The ID of the test subject
* `activity` - The type of activity performed when the corresponding measurements were taken

## Activity Labels

* `WALKING` (value `1`): subject was walking during the test
* `WALKING_UPSTAIRS` (value `2`): subject was walking up a staircase during the test
* `WALKING_DOWNSTAIRS` (value `3`): subject was walking down a staircase during the test
* `SITTING` (value `4`): subject was sitting during the test
* `STANDING` (value `5`): subject was standing during the test
* `LAYING` (value `6`): subject was laying down during the test


## Measurements: Just the names from the features file containing "mean" or "std"

tBodyAcc-mean()-X

Body acceleration signal derived in the time domain, mean, X-direction. Range: [-1,1]
tBodyAcc-mean()-Y

Body acceleration signal derived in the time domain, mean, Z-direction. Range: [-1,1]
tBodyAcc-mean()-Z

Body acceleration signal derived in the time domain, mean, Y-direction. Range: [-1,1]
tBodyAcc-std()-X

Body acceleration signal derived in the time domain, standard deviation, X-direction. Range: [-1,1]
tBodyAcc-std()-Y

Body acceleration signal derived in the time domain, standard deviation, Z-direction. Range: [-1,1]
tBodyAcc-std()-Z

Body acceleration signal derived in the time domain, standard deviation, Y-direction. Range: [-1,1]
tGravityAcc-mean()-X

Gravity acceleration signal derived in the time domain, mean, X-direction. Range: [-1,1]
tGravityAcc-mean()-Y

Gravity acceleration signal derived in the time domain, mean, Y-direction. Range: [-1,1]
tGravityAcc-mean()-Z

Gravity acceleration signal derived in the time domain, mean, Z-direction. Range: [-1,1]
tGravityAcc-std()-X

Gravity acceleration signal derived in the time domain, standard deviation, X-direction. Range: [-1,1]
tGravityAcc-std()-Y

Gravity acceleration signal derived in the time domain, standard deviation, Y-direction. Range: [-1,1]
tGravityAcc-std()-Z

Gravity acceleration signal derived in the time domain, standard deviation, Z-direction. Range: [-1,1]
tBodyAccJerk-mean()-X

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, mean, X-direction. Range: [-1,1]
tBodyAccJerk-mean()-Y

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, mean, Y-direction. Range: [-1,1]
tBodyAccJerk-mean()-Z

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, mean, Z-direction. Range: [-1,1]
tBodyAccJerk-std()-X

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, standard deviation, X-direction. Range: [-1,1]
tBodyAccJerk-std()-Y

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, standard deviation, Y-direction. Range: [-1,1]
tBodyAccJerk-std()-Z

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, standard deviation, Z-direction. Range: [-1,1]
tBodyGyro-mean()-X

Gyroscope signal derived in the time domain, mean, X-direction. Range: [-1,1]
tBodyGyro-mean()-Y

Gyroscope signal derived in the time domain, mean, Y-direction. Range: [-1,1]
tBodyGyro-mean()-Z

Gyroscope signal derived in the time domain, mean, Z-direction. Range: [-1,1]
tBodyGyro-std()-X

Gyroscope signal derived in the time domain, standard deviation, X-direction. Range: [-1,1]
tBodyGyro-std()-Y

Gyroscope signal derived in the time domain, standard deviation, Y-direction. Range: [-1,1]
tBodyGyro-std()-Z

Gyroscope signal derived in the time domain, standard deviation, Z-direction. Range: [-1,1]
tBodyGyroJerk-mean()-X

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, mean, X-direction. Range: [-1,1]
tBodyGyroJerk-mean()-Y

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, mean, Y-direction. Range: [-1,1]
tBodyGyroJerk-mean()-Z

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, mean, Z-direction. Range: [-1,1]
tBodyGyroJerk-std()-X

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, standard deviation, X-direction. Range: [-1,1]
tBodyGyroJerk-std()-Y

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, standard deviation, Y-direction. Range: [-1,1]
tBodyGyroJerk-std()-Z

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, standard deviation, Z-direction. Range: [-1,1]
tBodyAccMag-mean()

Body acceleration signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
tBodyAccMag-std()

Body acceleration signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
tGravityAccMag-mean()

Gravity acceleration signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
tGravityAccMag-std()

Gravity acceleration signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
tBodyAccJerkMag-mean()

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
tBodyAccJerkMag-std()

Body acceleration signal derived in the time domain, body linear acceleration (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
tBodyGyroMag-mean()

Gyroscope signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
tBodyGyroMag-std()

Gyroscope signal derived in the time domain, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
tBodyGyroJerkMag-mean()

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
tBodyGyroJerkMag-std()

Gyroscope signal derived in the time domain, angular velocity (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
fBodyAcc-mean()-X

Body acceleration signal derived in the frequency domain, mean, X-direction. Range: [-1,1]
fBodyAcc-mean()-Y

Body acceleration signal derived in the frequency domain, mean, Y-direction. Range: [-1,1]
fBodyAcc-mean()-Z

Body acceleration signal derived in the frequency domain, mean, Z-direction. Range: [-1,1]
fBodyAcc-std()-X

Body acceleration signal derived in the frequency domain, standard deviation, X-direction. Range: [-1,1]
fBodyAcc-std()-Y

Body acceleration signal derived in the frequency domain, standard deviation, Y-direction. Range: [-1,1]
fBodyAcc-std()-Z

Body acceleration signal derived in the frequency domain, standard deviation, Z-direction. Range: [-1,1]
fBodyAccJerk-mean()-X

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, mean, X-direction. Range: [-1,1]
fBodyAccJerk-mean()-Y

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, mean, Y-direction. Range: [-1,1]
fBodyAccJerk-mean()-Z

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, mean, Z-direction. Range: [-1,1]
fBodyAccJerk-std()-X

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, standard deviation, X-direction. Range: [-1,1]
fBodyAccJerk-std()-Y

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, standard deviation, Y-direction. Range: [-1,1]
fBodyAccJerk-std()-Z

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, standard deviation, Z-direction. Range: [-1,1]
fBodyGyro-mean()-X

Gyroscope signal derived in the frequency domain, mean, X-direction. Range: [-1,1]
fBodyGyro-mean()-Y

Gyroscope signal derived in the frequency domain, mean, Y-direction. Range: [-1,1]
fBodyGyro-mean()-Z

Gyroscope signal derived in the frequency domain, mean, Z-direction. Range: [-1,1]
fBodyGyro-std()-X

Gyroscope signal derived in the frequency domain, standard deviation, X-direction. Range: [-1,1]
fBodyGyro-std()-Y

Gyroscope signal derived in the frequency domain, standard deviation, Y-direction. Range: [-1,1]
fBodyGyro-std()-Z

Gyroscope signal derived in the frequency domain, standard deviation, Z-direction. Range: [-1,1]
fBodyAccMag-mean()

Body acceleration signal derived in the frequency domain, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
fBodyAccMag-std()

Body acceleration signal derived in the frequency domain, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
fBodyAccJerkMag-mean()

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
fBodyAccJerkMag-std()

Body acceleration signal derived in the frequency domain, body linear acceleration (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
fBodyGyroMag-mean()

Gyroscope signal derived in the frequency domain, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
fBodyGyroMag-std()

Gyroscope signal derived in the frequency domain, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]
fBodyGyroJerkMag-mean()

Gyroscope signal derived in the frequency domain, angular velocity (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, mean. Range: [-1,1]
fBodyGyroJerkMag-std()

Gyroscope signal derived in the frequency domain, angular velocity (Jerk) signal, magnitude of three-dimensional signal using Euclidian norm, standard deviation. Range: [-1,1]