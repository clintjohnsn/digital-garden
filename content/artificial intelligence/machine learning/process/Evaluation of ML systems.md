## Performance Metrics
Will require [[Gold Standard Data]] in the case of [[Supervised ML]]
### Metrics for  [[Classification]]
#### Confusion matrix
TP, TN, FP, FN summary
![[Pasted image 20240211022201.png]]
#### precision & recall

precision = TP/ (TP + FP)

recall = TP/ (TP + FN)

precision : fraction of annotated items that are correct

recall : fraction of correct items that are annotated

#### F-Score
a.k.a. F-measure 

> Suitable if one class is more important than the other

F<sub>β</sub> = (β<sup>2</sup> + 1)PR/β<sup>2</sup>P+R

where P = precision, R = recall

> F-score is a conservative average (Weighted harmonic mean) of precision and recall.
##### F1-score
set β = 1 in F-Score
> β is almost always set to 1, so F1 score and F-score are used interchangeably.

F1 = 2PR/(P+R)
#### Accuracy
Measure of all correctly annotated instances. 

>Suitable if all classes are equally important.

Accuracy = (TP + TN)/ (TP + TN + FP + FN)

> Accuracy is misleading in imbalance classification problems

#### Micro and Macro averaging
used to calculate combined scores for multiple classes.

**Macro averaging**
- simply get average precision and recall scores for the classes and calculate the F-score from mean precision and recall scores
- does not consider class imbalance

**Micro averaging**: 
- get total TP, FP, FN across all classes and calculate precision and recall across classes and then calculate the F-score
- works better when there is a class imbalance

**Weighted averaging**:
- macro averaging but weighted according to class
- average weighted by the number of true instances for each class


> In the absence of [[Gold Standard Data]] Olympic judging can be used ![[Evaluation of Software Systems#Olympic judging]]

### Metrics for [[Regression]]
#### Root Mean Squared Error [[RMSE]]

![[RMSE]]
#### Mean Absolute Error [[MAE]]

![[MAE]]
