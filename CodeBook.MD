# Getting and Cleaning Data Course Project

## Instructions for project
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

## Preliminary work: 
  
# 1. Download the file and put the file in the "data" folder

# 2. Unzip the file

# 3. unzipped file are in the folder UCI HAR Dataset. Get the list of the files

# See the README.txt file for the detailed information on the dataset.
# The files that will be used to load data are listed as follows:
# test/subject_test.txt
# test/X_test.txt
# test/y_test.txt
# train/subject_train.txt
# train/X_train.txt
# train/y_train.txt

# Read data from the files into the variables
# Read the Activity fles
# Read teh Subject files
# Read Fearures files

## Merges the training and the test sets to create one data set
# 1. Concatenate the data tables by rows
# 2. Set names to variables
# 3. Merge columns to get the data frame 'data' for all data. 

## Extract only the measurements on the mean and standard deviation for each measurement

# 1. Subset Name of Features by measurements on the mean and standard deviation
# taken Names of Features with ???mean()??? or ???std()???
subdataFeaturesNames<-dataFeaturesNames$V2[grep("mean\\(\\)|std\\(\\)", dataFeaturesNames$V2)]

# 2. Subset the data frame 'Data' by seleted names of Features
selectedNames<-c(as.character(subdataFeaturesNames), "subject", "activity" )
Data<-subset(Data,select=selectedNames)

# 3. Check the structures of the data frame 'Data'
str(Data)

## Uses descriptive activity names to name the activities in the data set

# 1. Read descriptive activity names from ???activity_labels.txt???
activityLabels <- read.table(file.path(path_rf, "activity_labels.txt"),header = FALSE)

# 2. facorize Variale activity in the data frame Data using descriptive activity names

# 3. Check

## Appropriately label the data set with descriptive variable names

# prefix t is replaced by time
# Acc is replaced by Accelerometer
# Gyro is replaced by Gyroscope
# prefix f is replaced by frequency
# Mag is replaced by Magnitude
# BodyBody is replaced by Body

# Check

## Create a second,independent tidy data set and ouput it



