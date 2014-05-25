{\rtf1\ansi\ansicpg1252\cocoartf1265\cocoasubrtf200
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 HelveticaNeue;}
{\colortbl;\red255\green255\blue255;\red38\green38\blue38;\red52\green110\blue183;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid1\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}
{\list\listtemplateid2\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid101\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid2}
{\list\listtemplateid3\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid201\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid3}
{\list\listtemplateid4\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid301\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid4}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}{\listoverride\listid2\listoverridecount0\ls2}{\listoverride\listid3\listoverridecount0\ls3}{\listoverride\listid4\listoverridecount0\ls4}}
\margl1440\margr1440\vieww19140\viewh21220\viewkind0
\deftab720
\pard\pardeftab720\sa300

\f0\fs30 \cf2 Code Book for the run_analysis.R script described on the Getting and Cleaning Data Course Project from Coursera.\
By Raul Goycoolea\
\pard\pardeftab720

\f1\fs28 \cf2 The included R script called run_analysis.R from thise Github repository does the following.\'a0\
\
\pard\tx220\tx720\pardeftab720\li720\fi-720
\ls1\ilvl0\cf2 {\listtext	1.	}Merges the training and the test sets to create one data set.\
{\listtext	2.	}Extracts only the measurements on the mean and standard deviation for each measurement.\'a0\
{\listtext	3.	}Uses descriptive activity names to name the activities in the data set\
{\listtext	4.	}Appropriately labels the data set with descriptive activity names.\'a0\
{\listtext	5.	}Creates a second, independent tidy data set with the average of each variable for each activity and each subject.\'a0
\f0\fs30 \cf2 \
\pard\pardeftab720\sa300
\cf2 \
The data source of the data set is: {\field{\*\fldinst{HYPERLINK "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"}}{\fldrslt \cf3 https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip}}\
The description of the how and about the data was obtained is on: {\field{\*\fldinst{HYPERLINK "http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones"}}{\fldrslt \cf3 http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones}}\
The execution of run_analysis.R script dot the following first to set the import the data from the data sets following the steps suggested on the project description:\
1. Merges the training and test sets to create one data set, namely train/X_train.txt with test/X_test.txt -- the result is a 10299 x 561 data frame, as in the original description ("Number of Instances: 10299" and "Number of Attributes: 561")\
\pard\tx220\tx720\pardeftab720\li720\fi-720
\ls2\ilvl0\cf2 2. Import the measurements and get only the mean and stddev from the features.txt \
\
3. Import the labels corresponding from the file activity_labels.txt to be used on the data set:\
\pard\pardeftab720\sa300
\cf2 	walking, walkingupstairs,walkingdownstairs,sitting,standing,laying\
\pard\tx220\tx720\pardeftab720\li720\fi-720
\ls3\ilvl0\cf2 4. The script also appropriately labels the data set with descriptive names: all attributes and activity names are converted to lower case, underscores and brackets () are removed.\
\
\pard\pardeftab720\sa300
\cf2 Following then merges the data frame containing features with the data frames of labels and IDs.\
The result is saved as merged_clean_data.txt, contains IDs, the second column activity names, and the rest of columns are measurements.  The measurement attributes names start with:\
tbodyacc-mean-x,tbodyacc-mean-y,tbodyacc-mean-z,tbodyacc-std-x,tbodyacc-std-y,tbodyacc-std-z,tgravityacc-mean-x,tgravityacc-mean-y\
\pard\tx220\tx720\pardeftab720\li720\fi-720
\ls4\ilvl0\cf2 5. 
\f1\fs28 \cf2 Creates a second, independent tidy data set with the average of each variable for each activity and each subject.}