Code Book for the run_analysis.R script described on the Getting and Cleaning Data Course Project from Coursera.
By Raul Goycoolea
The included R script called run_analysis.R from thise Github repository does the following. 

	1.	Merges the training and the test sets to create one data set.
	2.	Extracts only the measurements on the mean and standard deviation for each measurement. 
	3.	Uses descriptive activity names to name the activities in the data set
	4.	Appropriately labels the data set with descriptive activity names. 
	5.	Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

The data source of the data set is: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
The description of the how and about the data was obtained is on: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The execution of run_analysis.R script dot the following first to set the import the data from the data sets following the steps suggested on the project description:
1. Merges the training and test sets to create one data set, namely train/X_train.txt with test/X_test.txt -- the result is a 10299 x 561 data frame, as in the original description ("Number of Instances: 10299" and "Number of Attributes: 561")
2. Import the measurements and get only the mean and stddev from the features.txt 

3. Import the labels corresponding from the file activity_labels.txt to be used on the data set:
	walking, walkingupstairs,walkingdownstairs,sitting,standing,laying
4. The script also appropriately labels the data set with descriptive names: all attributes and activity names are converted to lower case, underscores and brackets () are removed.

Following then merges the data frame containing features with the data frames of labels and IDs.
The result is saved as merged_clean_data.txt, contains IDs, the second column activity names, and the rest of columns are measurements.  The measurement attributes names start with:
tbodyacc-mean-x,tbodyacc-mean-y,tbodyacc-mean-z,tbodyacc-std-x,tbodyacc-std-y,tbodyacc-std-z,tgravityacc-mean-x,tgravityacc-mean-y
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
