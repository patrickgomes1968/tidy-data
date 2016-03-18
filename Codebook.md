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

* `tBodyAcc-meanX`
* `tBodyAcc-meanY`
* `tBodyAcc-meanZ`
* `tBodyAcc-stdX`
* `tBodyAcc-stdY`
* `tBodyAcc-stdZ`
* `tGravityAcc-meanX`
* `tGravityAcc-meanY`
* `tGravityAcc-meanZ`
* `tGravityAcc-stdX`
* `tGravityAcc-stdY`
* `tGravityAcc-stdZ`
* `tBodyAccJerk-meanX`
* `tBodyAccJerk-meanY`
* `tBodyAccJerk-meanZ`
* `tBodyAccJerk-stdX`
* `tBodyAccJerk-stdY`
* `tBodyAccJerk-stdZ`
* `tBodyGyro-meanX`
* `tBodyGyro-meanY`
* `tBodyGyro-meanZ`
* `tBodyGyro-stdX`
* `tBodyGyro-stdY`
* `tBodyGyro-stdZ`
* `tBodyGyroJerk-meanX`
* `tBodyGyroJerk-meanY`
* `tBodyGyroJerk-meanZ`
* `tBodyGyroJerk-stdX`
* `tBodyGyroJerk-stdY`
* `tBodyGyroJerk-stdZ`
* `tBodyAccMag-mean`
* `tBodyAccMag-std`
* `tGravityAccMag-mean`
* `tGravityAccMag-std`
* `tBodyAccJerkMag-mean`
* `tBodyAccJerkMag-std`
* `tBodyGyroMag-mean`
* `tBodyGyroMag-std`
* `tBodyGyroJerkMag-mean`
* `tBodyGyroJerkMag-std`
* `fBodyAcc-meanX`
* `fBodyAcc-meanY`
* `fBodyAcc-meanZ`
* `fBodyAcc-stdX`
* `fBodyAcc-stdY`
* `fBodyAcc-stdZ`
* `fBodyAcc-meanFreqX`
* `fBodyAcc-meanFreqY`
* `fBodyAcc-meanFreqZ`
* `fBodyAccJerk-meanX`
* `fBodyAccJerk-meanY`
* `fBodyAccJerk-meanZ`
* `fBodyAccJerk-stdX`
* `fBodyAccJerk-stdY`
* `fBodyAccJerk-stdZ`
* `fBodyAccJerk-meanFreqX`
* `fBodyAccJerk-meanFreqY`
* `fBodyAccJerk-meanFreqZ`
* `fBodyGyro-meanX`
* `fBodyGyro-meanY`
* `fBodyGyro-meanZ`
* `fBodyGyro-stdX`
* `fBodyGyro-stdY`
* `fBodyGyro-stdZ`
* `fBodyGyro-meanFreqX`
* `fBodyGyro-meanFreqY`
* `fBodyGyro-meanFreqZ`
* `fBodyAccMag-mean`
* `fBodyAccMag-std`
* `fBodyAccMag-meanFreq`
* `fBodyBodyAccJerkMag-mean`
* `fBodyBodyAccJerkMag-std`
* `fBodyBodyAccJerkMag-meanFreq`
* `fBodyBodyGyroMag-mean`
* `fBodyBodyGyroMag-std`
* `fBodyBodyGyroMag-meanFreq`
* `fBodyBodyGyroJerkMag-mean`
* `fBodyBodyGyroJerkMag-std`
* `fBodyBodyGyroJerkMag-meanFreq`