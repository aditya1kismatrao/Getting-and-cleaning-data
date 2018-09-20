# Getting and Cleaning Data Project

The motive of this repo is to complete the assignment given at end of week 4. 
The main couple of steps are to download and unzip the data file in your working directory and to generate tidy data file using R programming.

### Overview
The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. A full description of the data used in this project can be found at 'The UCI Machine Learning Repository'(http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

*The source data for this project can be found here.*(https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)


### Code analysis and aim of the project
The goal of the project is to create one R script called run_analysis.
The code combined training dataset and test dataset,  and extracted partial variables to create another dataset with the averages of each variable for each activity.
Given are the various steps involved.

    1. Merges the training and the test sets to create one data set where rbind command is used.
    2. Extracts only the measurements on the mean and standard deviation for each measurement by using grep command.
    3. Uses descriptive activity names to name the activities in the data set by converting activity labels to commands.
    4. Appropriately labels the data set with descriptive activity names by giving selected descriptive names to variable columns.
    5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


### Varied Files included
* 'Readme.md' contains entire description and summary of the assignment.
* 'CodeBook.md' contains information on the variables, data set, transformations and work that was done to tidy up the data
* 'run_analysis.R' is the code for the R script used to complete the project goals
* 'FinalTidyData.txt' is the output from the 'runAnalysis.R' R script
