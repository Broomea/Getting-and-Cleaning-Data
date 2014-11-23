# CodeBook - Getting and Cleaning Data Course Project
##
##The data described in this codebook represent data collected from the accelerometers from the Samsung Galaxy S smartphone.
## 
## This data table is wide, with the mean data first and the standard deviation data second.
##
## The features_info.txt file contains the following description of the raw data from the original files:
##
###The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
###
###Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
###
###Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 
###
###These signals were used to estimate variables of the feature vector for each pattern:  
###'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.
###
* tBodyAcc-XYZ
* tGravityAcc-XYZ
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag

###The set of variables that were estimated from these signals are: 
###
###mean(): Mean value
###std(): Standard deviation
###
###Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:
###
###tBodyAccMean
###tBodyAccJerkMean
###tBodyGyroMean
###tBodyGyroJerkMean
###
##
## Some modifications were made to the original data from the study to create a tidy data file containing only mean and standard deviation data. 
* The Column Names in this dataset were changed to remove invalid characters:  for example:  ()
* For columns that end in X, Y, or Z, specified Xaxis, Yaxis, and Zaxis per the description in the features_info.txt document to better describe the data
* Column names with a ‘t’ prefix indicate the time domain signals so the 't’ prefix was changed to Time as documented in the features_info.txt document.
* Changed the column names with a ‘f’ prefix to Fast (short for Fast Fourier Transform) as documented in the features_info.txt document.
* Changed the column names that included BodyBody to contain only a single Body because the features_info.txt document contains no reference to a BodyBody measurement.
##
## The following is a list of the columns included in the tidy data file:
## 
1.  Activity - 6 Activities were measured in this study:  
    WALKING  
    WALKING_UPSTAIRS  
    WALKING_DOWNSTAIRS  
    SITTING  
    STANDING  
    LAYING  
2.  Subject - There were 30 subjects participating in this study
3.  TimeBodyAccMeanXaxis
4.  TimeBodyAccMeanYaxis
5.  TimeBodyAccMeanZaxis
6.  TimeGravityAccMeanXaxis
7.  TimeGravityAccMeanYaxis
8.  TimeGravityAccMeanZaxis
9.  TimeBodyAccJerkMeanXaxis
10. TimeBodyAccJerkMeanYaxis
11. TimeBodyAccJerkMeanZaxis
12. TimeBodyGyroMeanXaxis
13. TimeBodyGyroMeanYaxis
14. TimeBodyGyroMeanZaxis
15. TimeBodyGyroJerkMeanXaxis
16. TimeBodyGyroJerkMeanYaxis
17. TimeBodyGyroJerkMeanZaxis
18. TimeBodyAccMagMean
19. TimeGravityAccMagMean
20. TimeBodyAccJerkMagMean
21. TimeBodyGyroMagMean
22. TimeBodyGyroJerkMagMean
23. FastBodyAccMeanXaxis	
24. FastBodyAccMeanYaxis
25. FastBodyAccMeanZaxis
26. FastBodyAccJerkMeanXaxis
27. FastBodyAccJerkMeanYaxis
28. FastBodyAccJerkMeanZaxis
29. FastBodyGyroMeanXaxis
30. FastBodyGyroMeanYaxis
31. FastBodyGyroMeanZaxis
32. FastBodyAccMagMean
33. FastBodyAccJerkMagMean
34. FastBodyGyroMagMean
35. FastBodyGyroJerkMagMean
36. TimeBodyAccStdXaxis
37. TimeBodyAccStdYaxis
38. TimeBodyAccStdZaxis
39. TimeGravityAccStdXaxis
40. TimeGravityAccStdYaxis
41. TimeGravityAccStdZaxis
42. TimeBodyAccJerkStdXaxis
43. TimeBodyAccJerkStdYaxis
44. TimeBodyAccJerkStdZaxis
45. TimeBodyGyroStdXaxis
46. TimeBodyGyroStdYaxis
47. TimeBodyGyroStdZaxis
48. TimeBodyGyroJerkStdXaxis
49. TimeBodyGyroJerkStdYaxis
50. TimeBodyGyroJerkStdZaxis
51. TimeBodyAccMagStd
52. TimeGravityAccMagStd
53. TimeBodyAccJerkMagStd
54. TimeBodyGyroMagStd
55. TimeBodyGyroJerkMagStd
56. FastBodyAccStdXaxis
57. FastBodyAccStdYaxis
58. FastBodyAccStdZaxis
59. FastBodyAccJerkStdXaxis
60. FastBodyAccJerkStdYaxis
61. FastBodyAccJerkStdZaxis
62. FastBodyGyroStdXaxis
63. FastBodyGyroStdYaxis
64. FastBodyGyroStdZaxis
65. FastBodyAccMagStd
66. FastBodyAccJerkMagStd
67. FastBodyGyroMagStd
68. FastBodyGyroJerkMagStd
