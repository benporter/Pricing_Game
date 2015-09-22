**Predictive Modeling Subgroup**

*Getting Started*

The shortcut to using the training dataset (claims_data) is to just load up the data from the .RData file.  This data has certain columns removed that would perfectly predict the outcome and the policy number.  It also includes our agreed upon dependent variable, "claims."

set the working directory to where you have saved training.RData

    setwd("/folder/where/file/is/located/")

this will load the cleaned training set into memory

    load("training.RData")

verify that it worked by printing the first 6 records:

    head(claims_train)

*Saving your model*

Once you have created the final model ready for submission, save the model object, e.g. the results from the train() function.  In this example, the model object is named gbmFit1.  Prior to saving the model object, all other objects are removed from the workspace.

    allobjects <- ls()
    removeObjectList <- allobjects[allobjects  != "gbmFit1"]
    rm(list = removeObjectList)
    save.image("PorterBestModel.RData")

Submit your .RData by either doing a pull request, or email it to Ben.

*Evaluation Criteria*
- Ben will score your model using the pricing.csv data to compute the model performance.  (no peeking at priving.csv)
- We'll declare the winner based on the AUC and plot everyone's ROC curve on one chart.

