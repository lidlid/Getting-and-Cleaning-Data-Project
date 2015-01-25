# Getting-and-Cleaning-Data-Project
Project for Coursera getting and cleaning data course

# Project Description
The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.

Specifically, one of the most exciting areas in all of data science right now is wearable computing - see for example an article http://www.insideactivitytracking.com/data-science-activity-tracking-and-the-battle-for-the-worlds-top-sports-brand/. Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. 

The data being used in this project represents data collected from the accelerometers from the Samsung Galaxy S smartphone with goal of preparing the data for further analysis.

# Files in the repository: 

* run_analysis.R: R script to transform raw accelerometer data collected from the Samsung Galaxy S to a tidy dataset
* README.md: this file
* CodeBook.md: a code book that describes the variables, data, and transformations performed to clean up the raw data

# Creating the tidy data set:
1. Clone this repository
2. Download raw data at https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
3. Unzip the raw data to a destination on the local machine
4. Open R and set the working directory to the repository containing the project data
5. Source the run_analisys.R script 

# Script operation
The run_analisys.R script checks the availability, installs and loads the necessary R packages including data.table and reshape2. 
It then loads both the training and test raw data, extracts the mean and standard deviation measurements only, sets activity labels and names and binds the data. Following that the script, merges the test and training data and prepares the tidy data