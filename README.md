It should run in a folder of the Samsung data (the zip had this folder: UCI HAR Dataset)
 The script assumes it has in it's working directory the following files and folders:
 * activity_labels.txt
 * features.txt
 * test/
 * train/
 
 The output is created in working directory with the name of tidy2.txt
 
 *Note:* the R script is built to run without including any libraries for the purpose of this course.
 
 ## run_analysis.R walkthrough
 It follows the goals step by step.
 
 * Step 1:
   * Read from activty_lables,subject_train,y_train,X_train,subject_test,y_test,X_test).
   * Merge subject,activity and features.
 
 * Step 2:
   * Collect information from activity,subject. Calculate Mean, Standard Deviation.
 
 * Step 3:
  * Read the activity labels from activity_labels.txt and replace the numbers with the text.

* Step 4:
  * Make a column list (includig "subjects" and "label" at the start)
  * Apply the now-good-columnnames to the data frame
  
* Step 5:
  * Create a new data frame by finding the mean for each combination of subject and Activity. It's done by `aggregate()` function.
    We create a new data set tidy.txt
  