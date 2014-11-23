# Getting and Cleaning Data Course Project
##
##The data described in this codebook represent data collected from the accelerometers from the Samsung Galaxy S smartphone.
## 
According to the README file for the "Human Activity Recognition Using Smartphones Dataset" project:  
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS,  
WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured  
3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained  
dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.   

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap  
(128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body 
acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each 
window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.  

##The dataset includes the following files:  
* README.txt
* CodeBook.txt:  Information about the data on the tidy data output file
* run_analysis.R:  The R script for creating the tidy data output file

##The following files are read as input into the R script listed above (assuming the "UCI HAR Dataset" directory is open):

* 'activity_labels.txt':      Links the class labels with their activity name  
* 'features.txt':             List of all features.  
* 'test/X_test.txt':          Test set.  
* 'test/subject_test.txt':    Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.  
* 'test/y_test.txt':          Test labels.  
* 'train/X_train.txt':        Training set.  
* 'train/subject_train.txt':  Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.  
* 'train/y_train.txt':        Training labels.  

## The R script, run_analysis.R, executes the following steps:  

1. Merges the training and the test sets to create one data set.  The resulting dataset contains 10299 obs. of 563 var.
2. Extracts only the measurements on the mean and standard deviation for each measurement which was interpreted to be any column that contained the word "mean" or "std". 
The resulting dataset contains 10299 obs. of 68 var.  Note that the dplyr package is required to run the select statement in this step.
3. Uses descriptive activity names to name the activities in the data set.
4. Appropriately labels the data set with descriptive variable names. 
5. Creates an independent tidy data set with the average of each variable for each activity and each subject. The resulting dataset contains 180 obs. of 68 var. Note that the data.table package is required to run this step.

The R script generates a tidy data text file that meets the principles of:  
* Each variable you measure should be in one column
* Each different observation of that variable should be in a different row
* Each table/file stores data about one “kind” of observation
* If you have multiple tables, they should include a column in the table that allows them to be linked.

The code for reading this file back into R is as follows:
data <- read.table("finalGrouping.txt",header=T)