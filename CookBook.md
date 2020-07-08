Code Book
=========

This code book that describes the variables, the data, and any transformations or work  performed to clean up the data

The R script called run_analysis.R  does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Design
------------

Here is a list of operations.

1. Download and Unzip the data set into the working program directory 
2. Load test (into subject_test, X_test and Y_test variables), training data sets (into into subject_train, X_train and Y_train variables). Then, load source variable names for test and training data sets. After, load the activity labels (features and activities variable)
3. Combine test and training data frames using rbind (load the result into data variable)
4. Pair  the data frames to  include the mean and standard deviation variables
5. Combine the data frames to produce one data frame containing the subjects, measurements and activities
6. Produce "first_tidy_data.txt" with the combined data frame as the 1st expected output
7. Create another data set using the data.table library to group the tidy data by subject and activity
8. Apply mean and standard deviation across the groups (store the result in calculatedData variable)
9. Produce "second_tidy_data.txt" as the 2nd expected output

The R code is available [here](https://github.com/vickkiee/datacleaning/blob/master/run_analysis.R) 

Variables
---------

1) subjectId: 1 to 30 that represents all participant in the study
2) activity: the activity of the participant measurement time
3) tBodyAcc-mean-X        
4) tBodyAcc-mean-Y
5) tBodyAcc-mean-Z
6) tBodyAcc-std-X
7) tBodyAcc-std-Y
8) tBodyAcc-std-Z
9) tGravityAcc-mean-X
10) tGravityAcc-mean-Y
11) tGravityAcc-mean-Z
12) tGravityAcc-std-X
13) tGravityAcc-std-Y
14) tGravityAcc-std-Z
15) tBodyAccJerk-mean-X
16) tBodyAccJerk-mean-Y
17) tBodyAccJerk-mean-Z
18) tBodyAccJerk-std-X
19) tBodyAccJerk-std-Y
20) tBodyAccJerk-std-Z
21) tBodyGyro-mean-X
22) tBodyGyro-mean-Y
23) tBodyGyro-mean-Z
24) tBodyGyro-std-X
25) tBodyGyro-std-Y
26) tBodyGyro-std-Z
27) tBodyGyroJerk-mean-X
28) tBodyGyroJerk-mean-Y
29) tBodyGyroJerk-mean-Z
30) tBodyGyroJerk-std-X
31) tBodyGyroJerk-std-Y
32) tBodyGyroJerk-std-Z
33) tBodyAccMag-mean
34) tBodyAccMag-std
35) tGravityAccMag-mean
36) tGravityAccMag-std
37) tBodyAccJerkMag-mean
38) tBodyAccJerkMag-std
39) tBodyGyroMag-mean
40) tBodyGyroMag-std
41) tBodyGyroJerkMag-mean
42) tBodyGyroJerkMag-std
43) fBodyAcc-mean-X
44) fBodyAcc-mean-Y
45) fBodyAcc-mean-Z
46) fBodyAcc-std-X
47) fBodyAcc-std-Y
48) fBodyAcc-std-Z
49) fBodyAccJerk-mean-X
50) fBodyAccJerk-mean-Y
51) fBodyAccJerk-mean-Z
52) fBodyAccJerk-std-X
53) fBodyAccJerk-std-Y
54) fBodyAccJerk-std-Z
55) fBodyGyro-mean-X
56) fBodyGyro-mean-Y
57) fBodyGyro-mean-Z
58) fBodyGyro-std-X
59) fBodyGyro-std-Y
60) fBodyGyro-std-Z
61) fBodyAccMag-mean
62) fBodyAccMag-std
63) fBodyBodyAccJerkMag-mean
64) fBodyBodyAccJerkMag-std
65) fBodyBodyGyroMag-mean
66) fBodyBodyGyroMag-std
67) fBodyBodyGyroJerkMag-mean
68) fBodyBodyGyroJerkMag-std