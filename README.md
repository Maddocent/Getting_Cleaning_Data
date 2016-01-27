## README for Getting_Cleaning_Data

### project repo belonging to "Project Assignment" Week 4 - Course 3, Coursera Specialization "Data Science"

### This repo contains:

* This README.md file
* A CodeBook: "CodeBook.md" belonging to the R script "run_analysis.R". CodeBook.md includes a description of the data, the variables, the transformations of the data and some details on the experiments performed to obtain the data
* An R script: "run_analysis.R" that downloads the data set to your currently set working directory, combines all the data to one dataset, selects certain variables and changes the variable names to more descriptive names and returns a tidy dataset with descriptive summary statistics of the data.
* A document called "Assigment.txt" which is the explanation of the  project assignment as it was copied from the Coursera Course 3 "Getting and Cleaning Data". 

to load the "run_analysis.R" script, download the file "run_analysis.R" to your working dir., open a new script and type
``` source("run_analysis.R") ```
in the R console or in an R source editor. Running this one line should execute the script and do the cleaning and summary of the data for you.
The dataset files will be in a newly created folder in your working dir. called "UCI HAR Dataset", the tidied datasets: both with selected variables and the summary wil be in the folder called "UCI data". The files will be called "selected_data.txt" for the file with the preselected variables from the original set. The summary file will be called "tidy_data.txt"
