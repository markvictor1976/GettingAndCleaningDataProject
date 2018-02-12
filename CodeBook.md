Getting and Cleaning Data

Code Book

This code book summarizes the resulting data fields in tidy.txt.


Included in the code is the routine to remove clear the workspace of variables and
checking whether the zipped file is existing and download it if it is not and setup of
the working directory.



Attribute Information

For each record in the dataset it is provided:

    Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
    Triaxial Angular velocity from the gyroscope.
    A 561-feature vector with time and frequency domain variables.
    Its activity label.
    An identifier of the subject who carried out the experiment.

1. Merge the training and the test sets to create one data set.

After setting the source directory for the files, read into tables the data located in

    features.txt
    activity_labels.txt
    subject_train.txt
    x_train.txt
    y_train.txt
    subject_test.txt
    x_test.txt
    y_test.txt

Assign column names and merge to create one data set.

2. Extract only the measurements on the mean and standard deviation for each measurement.

Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. Subset this data to keep only the necessary columns.

3. Use descriptive activity names to name the activities in the data set

Merge data subset with the activityType table to cinlude the descriptive activity names

4. Appropriately label the data set with descriptive activity names.

Use gsub function for pattern replacement to clean up the data labels.

5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.

We only need to produce a data set with the average of each veriable for each activity and subject