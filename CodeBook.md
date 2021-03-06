# CodeBook
This code book describes the variables, data, and transformations performed to clean up the raw data to tidy data format for further analysis

# The Data
Abstract: The data being used in this project represents data collected from the accelerometers from the Samsung Galaxy S smartphone with goal of preparing the data for further analysis. It is a Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors.

* Data Set Characteristics:  Multivariate, Time-Series
* Number of Instances: 10299
* Number of Attributes: 561
* Date Donated: 2012-12-10
* Associated Tasks: Classification, Clustering
* Source: Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto. Smartlab - Non Linear Complex Systems Laboratory. DITEN - Universit√  degli Studi di Genova, Genoa I-16145, Italy. activityrecognition '@' smartlab.ws. www.smartlab.ws 

# Dataset Information:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

Attribute Information: For each record in the dataset it is provided: 
* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
* Triaxial Angular velocity from the gyroscope. 
* A 561-feature vector with time and frequency domain variables. 
* Its activity label. 
* An identifier of the subject who carried out the experiment.

Original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  
Original description of the dataset: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

# Dataset Files:
* README.txt
* features_info.txt: Shows information about the variables used on the feature vector.
* features.txt: List of all features.
* activity_labels.txt: Links the class labels with their activity name.
* X_train.txt: Training set.
* y_train.txt: Training labels.
* X_test.txt: Test set.
* y_test.txt: Test labels.
* subject_train.txt: Each row identifies the subject who performed the activity for each window sample (range is from 1 to 30).
* total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the total_acc_x_train.txt and total_acc_z_train.txt files for the Y and Z axis.
* body_acc_x_train.txt: The body acceleration signal obtained by subtracting the gravity from the total acceleration.
* body_gyro_x_train.txt: The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

# Transformation operation
The run_analisys.R script:

1-Checks the availability, installs and loads the necessary R packages including data.table and reshape2.  
2-Loads both the training and test raw data  
3-Extracts the mean and standard deviation measurements only  
4-Sets activity labels and names and binds the data  
5-Merges the test and training data and prepares the tidy data
