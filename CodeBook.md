##Data
Site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Data used for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

##Cleaning Data
*run_analysis.R* script performs the following steps to clean the data:

* Read data by using the *read.table()* function and merge data by using the *rbind()* function. 
2. Using the *grep()* functin to get only columns with *mean()* or *std()* in their names. Then subset the desired columns and 
correct the column names, taken from *features.txt*.
3. As activity data is addressed with values 1:6, we take the activity names and IDs from *activity_labels.txt*
and they are substituted in the dataset.
4. Then those columns with vague column names are corrected in the whole dataset.
5. At the end we create a new dataset, named *averages_data.txt*, with all the average measures for each subject and activity type 

##Variables
* *x_train, y_train, x_test, y_test, subject_train* and *subject_test* contain unaltered data from the downloaded files
* *x_data, y_data* and *subject_data* merge the original datasets
* features contains the correct names for the *x_data* dataset
* *mean_std_features* is a numeric vector and extracts the desired data from the whole dataset
* activities contains the correct activity names through the activities variable
* *all_data* merges *x_data, y_data* and *subject_data* in a one dataset
* *averages_data* contains the averagesGetting and Cleaning Data Course Project
