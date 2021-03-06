## CodeBook, belonging to "run_analysis.R" in this repository
### Author: Dr. Marc A.T. Teunis, Utrecht, January 2016 

The R script: "run_analysis.R" will clean and tidy the UCI data set described below. When downloading the script to 
your working directory you can source the script by typing 

` source("run_analysis.R") `  
Run this one line of code to execute the sourced script in the R console or R editor (e.g. RStudio).

This will result in the installation of neccessary packages (if not already installed), the loading  of the packages and the download of the dataset, and the cleaning-up of the dataset ("UCI_data/selected_data.txt"). The script finally generates a summary of the "selected_data" frame ("UCI_data/tidy_data.txt").

To load the generated "selected_data.txt" and "tidy_data.txt" data files: 
load the "selected_data.txt" file:

` selected_data <- tbl_df(read.table(file = "./UCI_data/selected_data.txt", row.names = NULL, header = TRUE)) `

To view the "selected_data" table
` print(selected_data) `
` View(selected_data) `

load the "tidy_data.txt" file:
` tidy_data <- tbl_df(read.table(file = "./UCI_data/tidy_data.txt", row.names = NULL, header = TRUE)) `

To view the "tidy_data" table
` print(tidy_data) `
`View(tidy_data) `

## The experiment
As reference in the Readme.md file in this repository:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

Check the README.txt file in the dataset for further details about this dataset.

A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: [Web Link]

An updated version of this dataset can be found at [Web Link]. It includes labels of postural transitions between activities and also the full raw inertial signals instead of the ones pre-processed into windows.

## Attribute Information:
For each record in the dataset it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope.
- A 561-feature vector with time and frequency domain variables.
- Its activity label.
- An identifier of the subject who carried out the experiment.

## Relevant Papers:
Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra, Jorge L. Reyes-Ortiz. Energy Efficient Smartphone-Based Activity Recognition using Fixed-Point Arithmetic. Journal of Universal Computer Science. Special Issue in Ambient Assisted Living: Home Care. Volume 19, Issue 9. May 2013

Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. 4th International Workshop of Ambient Assited Living, IWAAL 2012, Vitoria-Gasteiz, Spain, December 3-5, 2012. Proceedings. Lecture Notes in Computer Science 2012, pp 216-223.

Jorge Luis Reyes-Ortiz, Alessandro Ghio, Xavier Parra-Llanas, Davide Anguita, Joan Cabestany, Andreu Català. Human Activity and Motion Disorder Recognition: Towards Smarter Interactive Cognitive Environments. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013.

Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. A Public Domain Dataset for Human Activity Recognition Using Smartphones. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013. 

## The data
The complete dataset can be downloaded here:
http://archive.ics.uci.edu/ml/machine-learning-databases/00240/UCI%20HAR%20Dataset.zip

## The variables
A complete list of variables can be found in the two file:
- features.txt 
- features_info.txt

The variables in the selected_data and tidy_data tables are:
` names(tidy_data) `
 [1] "subject"                                        
 [2] "activity"                                       
 [3] "body-acceleration-mean-x-time"                  
 [4] "body-acceleration-mean-y-time"                  
 [5] "body-acceleration-mean-z-time"                  
 [6] "body-acceleration-std-x-time"                   
 [7] "body-acceleration-std-y-time"                   
 [8] "body-acceleration-std-z-time"                   
 [9] "gravity-acceleration-mean-x-time"               
[10] "gravity-acceleration-mean-y-time"               
[11] "gravity-acceleration-mean-z-time"               
[12] "gravity-acceleration-std-x-time"                
[13] "gravity-acceleration-std-y-time"                
[14] "gravity-acceleration-std-z-time"                
[15] "body-acceleration-jerk-mean-x-time"             
[16] "body-acceleration-jerk-mean-y-time"             
[17] "body-acceleration-jerk-mean-z-time"             
[18] "body-acceleration-jerk-std-x-time"              
[19] "body-acceleration-jerk-std-y-time"              
[20] "body-acceleration-jerk-std-z-time"              
[21] "body-gyro-mean-x-time"                          
[22] "body-gyro-mean-y-time"                          
[23] "body-gyro-mean-z-time"                          
[24] "body-gyro-std-x-time"                           
[25] "body-gyro-std-y-time"                           
[26] "body-gyro-std-z-time"                           
[27] "body-gyro-jerk-mean-x-time"                     
[28] "body-gyro-jerk-mean-y-time"                     
[29] "body-gyro-jerk-mean-z-time"                     
[30] "body-gyro-jerk-std-x-time"                      
[31] "body-gyro-jerk-std-y-time"                      
[32] "body-gyro-jerk-std-z-time"                      
[33] "body-acceleration-magnitude-mean-time"          
[34] "body-acceleration-magnitude-std-time"           
[35] "gravity-acceleration-magnitude-mean-time"       
[36] "gravity-acceleration-magnitude-std-time"        
[37] "body-acceleration-jerk-magnitude-mean-time"     
[38] "body-acceleration-jerk-magnitude-std-time"      
[39] "body-gyro-magnitude-mean-time"                  
[40] "body-gyro-magnitude-std-time"                   
[41] "body-gyro-jerk-magnitude-mean-time"             
[42] "body-gyro-jerk-magnitude-std-time"              
[43] "body-acceleration-mean-x-frequency"             
[44] "body-acceleration-mean-y-frequency"             
[45] "body-acceleration-mean-z-frequency"             
[46] "body-acceleration-std-x-frequency"              
[47] "body-acceleration-std-y-frequency"              
[48] "body-acceleration-std-z-frequency"              
[49] "body-acceleration-jerk-mean-x-frequency"        
[50] "body-acceleration-jerk-mean-y-frequency"        
[51] "body-acceleration-jerk-mean-z-frequency"        
[52] "body-acceleration-jerk-std-x-frequency"         
[53] "body-acceleration-jerk-std-y-frequency"         
[54] "body-acceleration-jerk-std-z-frequency"         
[55] "body-gyro-mean-x-frequency"                     
[56] "body-gyro-mean-y-frequency"                     
[57] "body-gyro-mean-z-frequency"                     
[58] "body-gyro-std-x-frequency"                      
[59] "body-gyro-std-y-frequency"                      
[60] "body-gyro-std-z-frequency"                      
[61] "body-acceleration-magnitude-mean-frequency"     
[62] "body-acceleration-magnitude-std-frequency"      
[63] "body-acceleration-jerk-magnitude-mean-frequency"
[64] "body-acceleration-jerk-magnitude-std-frequency" 
[65] "body-gyro-magnitude-mean-frequency"             
[66] "body-gyro-magnitude-std-frequency"              
[67] "body-gyro-jerk-magnitude-mean-frequency"        
[68] "body-gyro-jerk-magnitude-std-frequency"  

The variables in the "selected_data" file can be found by typing:
` names(selected_data) ` 
and should be the same as the above list for "tidy_data"

## Transformations to the data
- No data transformations will be performed by the R script "run_analysis.R"
- The names of the variables will be changed to more human readable names
- The activity labels (1:6) will be converted to 6 'activity indicators'

the activity labels can be found by typing:
` as.factor(tidy_data) `
` levels(tidy_data$activity) `

## The "run_analysis.R" script: Consists of eight steps explained below:

STEP 1 - Installing packages used in this script: This step installs all the nessecary packages for the script to be able to execute all the written functions on the data.
The packages:
"curl" is needed for downloading the data, 
"dplyr" and "tidyr" to select appropriate variables, change the vraiable names, merge the diffrent data files to one and perform the 'group_by' summary statistics

STEP 2 - Getting the Data: Download the dataset (zip file) to a directory "data" in your current working directory. If the folder data does not exist the script will automatically create this directory.

STEP 3 - Merging the the training and the test sets to create one data set: combines the data from the subjects, the activities and the variables (features) of the "train" dataset with the subjects, activities and features of the "test" dataset.

STEP 4 - Extracting only the measurements with mean and standard deviation: From the 563 variables in the merged dataset, only the variables containing the words "mean" and "std" are selected. The variables "subject" and activity are alse both retained. The "selected_data" data frame will contain 68 variables. 

STEP 5 - Applying descriptive activity names to name the activities in the data set: This will change the labels of the activities variable (factor) to the activities: . The names will all be lower capitals, conform the tidy dat principle. 

to view the original labels and the new labels type:
` View(activities) `

STEP 6 - Appropriately labelling of the "selected_data" frame with descriptive variable names.

to see the names of the selected variables type:
` names(selected_data) `

STEP 7 - From the "selected_data" frame, a second, 
independent tidy data frame is created with the mean of each variable for each activity and each subject.
To view the tidy set
` print(tidy_data) `
This step also writes 2 data to the folder "UCI_data": "tidy_data.txt" and "selected_data.txt" 

STEP 8 - Cleaning the Glabal Environment
To get rid of the excess objects in the global envrionment the script closes off with:
` keep(selected_data, tidy_data, activities, sure = TRUE) `
which keeps only the data frames "selected_data", "activities" and "tidy_data"



## Other concerns and information
The script has been written with information from the Coursera Course 3: "Getting and Clenaing Data". Tutorials and exercises were particularly helpful. Part of the R code was adapted from https://github.com/sudar/UCI-HAR-Dataset-Analysis. 

## Adapted from Source:
Jorge L. Reyes-Ortiz(1,2), Davide Anguita(1), Alessandro Ghio(1), Luca Oneto(1) and Xavier Parra(2)
1 - Smartlab - Non-Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova, Genoa (I-16145), Italy.
2 - CETpD - Technical Research Centre for Dependency Care and Autonomous Living
Universitat Politècnica de Catalunya (BarcelonaTech). Vilanova i la Geltrú (08800), Spain
activityrecognition '@' smartlab.ws

