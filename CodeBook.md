Getting and Cleaning Data Project
Description
The purpose of this project is to walk through data cleaning, data merging, subsetting data table  process. Additional information about the variables, data and transformations are at https://rstudio-pubs-static.s3.amazonaws.com/37290_8e5a126a3a044b95881ae8df530da583.html
Source Data
A full description is available at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Below is the link to the data. 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Description of Data Sets
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: [Web Link]
Attribute Information
For each record in the dataset it is provided: 
•	Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
•	Triaxial Angular velocity from the gyroscope. 
•	A 561-feature vector with time and frequency domain variables. 
•	Its activity label. 
•	An identifier of the subject who carried out the experiment.
Coding Logics
1.	download and unzip the zip file 
2.	merge the training and the test sets as one data set.
Read into tables the data located in
•	features.txt
•	activity_labels.txt
•	subject_train.txt
•	x_train.txt
•	y_train.txt
•	subject_test.txt
•	x_test.txt
•	y_test.txt
3.	Assign column names and merge (yTrain, subjectTrain, and xTrain) to create one training data set.
4.	create the final training set by combining all columns in each file: yTrain, subjectTrain, and xTrain
5.	Create the final test set by combining the xTest, yTest and subjectTest data
6.	Extract the mean and standard deviation for each measurement.
7.	Merge the finalData set with the acitivityType table to include descriptive activity names
8.	Updating the colNames vector to include the new column names after merge
9.	Reassigning the new descriptive column names to the finalData set
10.	Create a tidy data set  with the average of each variable for each activity and each subject.

