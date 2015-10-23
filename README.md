# TidyDataSet
Peer Assessment for Getting and Cleaning Data

Purpose

This script processes data from the Human Activity Recognition Using Smartphones Dataset to extract the average means and standard deviations of each variable for a given subject and activity, returning a tidy data frame containing these values.

The script was prepared to meet the requirements of an assignment in the Getting and Cleaning Data Course offered on Coursera

Source Data

credit for the Human Activity Recognition Using Smartphones Dataset to:

Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto. Smartlab - Non Linear Complex Systems Laboratory DITEN - Universit? degli Studi di Genova. Via Opera Pia 11A, I-16145, Genoa, Italy. activityrecognition@smartlab.ws www.smartlab.ws

Data available here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

With a full description here:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Assumptions

The script assumes the data will be found in the directory "./UCI HAR Dataset/" structured as it is in the linked archive. The script requires that the packages "plyr" and "reshape2" are available.

Use

To use the script at the prompt, call source("~/run_analysis.R") correcting for file location, then run_analysis(). Assigning the ouput of the script to a data frame is recomended, since the resulting table is too large to simply read on screen.


Steps Performed

The bulk of the steps done by the script involve loading the data provided from the source, and tidying this into a single data frame containing just the original data cells of interest, in the desired format. Only the final major step computes a new result from the tidied data, writing out subject ids, activites, and mean of all measures of interest.

Tidy Part 1

Get feature names and subset to only those features of mean or std measures

Tidy Part 2

Get the train and test feature sets and subset only the desired features

Tidy Part 3

Combine the two datasets into 1

Tidy Part 4

Attach column names to features

Tidy Part 5

Read and combine the train and test activity codes

Tidy Part 6

Get activity labels and attach to activity codes

Tidy Part 7

Get and combine the train and test subject ids

Tidy Part 8

Combine and name subjects and activity names

Tidy Part 9

Combine with measures of interest for finished desired data frame

Compute New Result

From the set produced for analysis, compute and report means of all measures, grouped by subject_id and by activity.
