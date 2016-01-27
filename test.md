## CodeBook, belonging to "run_analysis.R" in this repository

The R script: run_analysis.R will tidy the UCI data set described below. When downloading the script to 
your working directory you can source the script by typing 

` source("run_analysis.R") `  

in the R console or R editor (e.g. RStudio).

This will result in the download of the dataset, the cleaning-up of the dataset ("UCI_data/selected_data.txt") and generates a summary (UCI_data/tidy_data.txt" files).

To load the generated "selected_data.txt" and "tidy_data.txt":
run if you do not have dplyr installed: 

`install.packages("dplyr")`
