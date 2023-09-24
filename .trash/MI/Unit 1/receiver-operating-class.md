
# Receiver Operating Class
This is a technique used to evaluate the goodness of a model.

When we have data with outliers, we can have misidentified labels, where we draw the line i.e. threshold, between the classes can lead to either high false positives or high false negatives. 

We construct a curve with True Positive Rate(TPR) on the y axis and the False Positive Rate(FPR) on the x axis.
By connecting all the points for FPR-TPR graph, we get the **ROC** curve. The area under this curve is the **AUC**.

This can be used to identify the better model, as that model will have a higher AUC. An ideal model will have its AUC as 1. 


[[id3-algorithm| ID3 Algorithm]]