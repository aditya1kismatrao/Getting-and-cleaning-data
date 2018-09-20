# Tidy data set Description
This codebook gives a pretext of an assignment done in getting and cleaning data course. In this assignment,
we successfully create a tidy data set.

### The variables in the tidy data
Tidy data contains 180 rows and 68 columns. Each row has averaged variables for each subject and each activity.

### Only all the variables estimated from mean and standard deviation in the tidy set were kept.

* mean(): Mean value
* std(): Standard deviation

### The data were averaged based on subject and activity group.

Subject column is numbered sequentially from 1 to 30.
Activity column has 6 types as listed below.
1. WALKING
2. WALKING_UPSTAIRS
3. WALKING_DOWNSTAIRS
4. SITTING
5. STANDING
6. LAYING

## Code analysis 
The goal of the project is to create one R script called run_analysis.
The code combined training dataset and test dataset,  and extracted partial variables to create another dataset with the averages of each variable for each activity.
Given are the various steps involved.

    1. Merges the training and the test sets to create one data set where rbind command is used.
    2. Extracts only the measurements on the mean and standard deviation for each measurement by using grep command.
    3. Uses descriptive activity names to name the activities in the data set by converting activity labels to commands.
    4. Appropriately labels the data set with descriptive activity names by giving selected descriptive names to variable columns.
    5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


#### 1. MERGING TRAINING & TEST SETS
The following text files were imported and merged. Column names were assigned at the time each file was imported and prior to merge. Files were imported individually and applicable files were then merged into sets, first all files in the TRAINING set \(*_train.txt\) then all files in the TEST set \(*_test.txt\). This was done prior to merging the two sets into one larger data set. The features and activity_labels files had column names assigned but were not merged and will be used later.

#### Text Files Imported:

- 'features.txt'
- 'activity_labels.txt'
- 'subject_train.txt'
- 'x_train.txt'
- 'y_train.txt'
- 'subject_test.txt'
- 'x_test.txt'
- 'y_test.txt'

#### EXTRACTING MEASUREMENTS ON MEAN & STANDARD DEVIATION
A logical vector was created identifying TRUE for the ID, mean & stdev columns and FALSE for other values. Merged data was then subsetted to only keep the relevant columns

#### RENAME ACTIVITIES IN DATA SET WITH DESCRIPTIVE ACTIVITY NAMES
'activity_labels.txt' was merged with the subsetted data to add descriptive activity names to merged and subsetted data set. Values in 'activityId' column were then replaced with the matching values from the 'activityType' column in order to make the data easier to read. 

#### APPROPRIATELY LABEL DATA SET WITH DESCRIPTIVE ACTIVITY NAMES
Used the 'gsub' function to clean up the column names in merged & subsetted data set. 'activityType' column removed in order to tidy data further.

#### INDEPENDNENT TIDY DATA SET CREATED WITH AVERAGE FOR EACH VARIABLE & EACH SUBJECT
New table was created which contains average for each variable for each activity and subject.
