**Predictive Modeling Subgroup**



Getting Started
 - The shortcut to using the training dataset is to just load up the data from the .RData file
 - test


set the working directory to where you have saved training.RData

    setwd("/folder/where/file/is/located/")

this will load the cleaned training set into memory

    load("training.RData")

verify that it worked by printing the first 6 records:

    head(train)

Saving your model

Evaluation Criteria
- Ben will score your model using the pricing.csv data to compute the model performance.  (no peeking at priving.csv)
- We'll declare the winner based on the AUC and plot everyone's ROC curve on one chart.

