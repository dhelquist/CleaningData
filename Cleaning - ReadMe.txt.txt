## READ ME

The purpose of this program is to read in data from 6 disparate tables, 3 from a training set and 3 from a test set.  Additionally, read in a conversion table which defines the activity names for the respective activity ID's in the tables and join/merge that to the tables to enable easy readability of the activities.  It combines all the tables, building first the training set, then the testing set, and then putting the two sets together into a master set.  

Once the master set is created, I selected specific columns which denote the mean and standard deviation measurements from the gyroscope in the smartphone (Samsung Galaxy S II) indicating the precise movements of the user.  I called that abreviated dataset of means & standard deviations 'masterMeans'.

I then created a table called 'AggMean' which calculates the mean of each mean/standard deviation column, and aggregates that by user ID and by Activity.

Below is the R code used to accomplish this purpose:

-----------------------------------------------------------

 ## Read Training Data
xtrain <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/train/X_train.txt")
ytrain <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/train/y_train.txt")
subtrain <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/train/subject_train.txt")
  ## Read Test Data
xtest <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/test/X_test.txt")
ytest <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/test/y_test.txt")
subtest <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/test/subject_test.txt")

  ## Set Column Labels for the X table. Remove parentheses, hyphens, and make lower:
xnames <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/features.txt")
xnames$V2 <- gsub("(", "", xnames$V2, fixed=TRUE)
xnames$V2 <- gsub(")", "", xnames$V2, fixed=TRUE)
xnames$V2 <- make.names(xnames$V2, unique=TRUE, allow_ = FALSE)
xnames$V2 <- tolower(xnames$V2)

  ## Load activities labels, merge with y data, and create column labels:
 yactivities <- read.table("~/Coursera Data Science/Cleaning Data/UCI HAR Dataset/activity_labels.txt")

  ## COMBINE COLUMNS FIRST, THEN COMBINE ROWS:
 ## First: Combine the Training Set:
names(xtrain) <- xnames[,2]
names(subtrain) <- c("SubID")
train <- cbind(subtrain, ytrain, xtrain)
trainM <- merge(train, yactivities, by.x="V1", by.y="V1")
trainM <- trainM[c(2,1,564,3:563)]
names(trainM)[2:3] <- c("ActID", "Activity")
 ## Second: Combine the Test Set:
names(xtest) <- xnames[,2]
names(subtest) <- c("SubID")
test <- cbind(subtest, ytest, xtest)
testM <- merge(test, yactivities, by.x="V1", by.y="V1")
testM <- testM[c(2,1,564,3:563)]
names(testM)[2:3] <- c("ActID", "Activity")
 ## Third: Combine the Training and Test set rows:
master <- rbind(trainM, testM)

  ## Pull out columns related to Mean & Standard Deviation:
masterMeans <- master[,c(1:9, 44:49, 84:89, 124:129, 164:169, 204:205, 217:218, 
                         230:231, 243:244, 256:257, 269:274, 297:299, 348:353, 
                         376:378, 427:432, 455:457, 506:507, 516, 562:564)] 
masterMeans <- masterMeans[,-2] ## Removing 'activity ID' column...it's unnecessary

 ## Calulate means aggregated by Sub ID & Activity:
AggMean <- aggregate(x=masterMeans, by=list(masterMeans$SubID, masterMeans$Activity), FUN="mean")
AggMean <- AggMean[,-(3:4)]
names(AggMean)[1:2] <- c("SubID", "Activity")

 ## Save the file:
write.table(AggMean, file="~/Coursera Data Science/Cleaning Data/Aggregated_Means.txt")

