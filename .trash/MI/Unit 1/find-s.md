
# Find S
Basic supervised algorithm for classifying objects.

It tries to find common properties among all the test data, and uses those attributes or classification.

| Sl No. | Sun | Wind | Rain | Enjoy Playing(result) |
| ------ | --- | ---- | ---- | --------------------- |
| 1      | Yes | Yes  | No   | Yes                   |
| 2      | No  | Yes  | No   | No                    |
| 3      | Yes | No   | No   | Yes                   |
| 4      | No  | No   | No   | Yes                   |
| 5      | Yes | Yes  | Yes  | No                    |
| 6      | Yes | No   | Yes  | No                    |

In this example, we first find out all the common properties in the entries that have a positive outcome. Our initial hypothesis is the rejection hypothesis. ${\{ \phi, \phi, \phi\}}$ and any time we see conflicting properties we put a $?$

| Sl No. | Current Hypothesis |
| ------ | ------------------ |
| 1      | {Sun, Wind, No}    |
| 3      | {?, Wind, No}      |
| 4      | {?, ?, No}         |

To Evaluate this Model We Take Negative outcome and see how many it could correctly reject.

| Sl No. | Prediction | Result |
| ------ | ---------- | ------ |
| 2      | Yes        | No     |
| 5      | No         | No     |
| 6      | No         | No       |

We get an accuracy of 66%, which is not too good. And this gets worse as the number of attributes increases or the dataset size increases



## Performance Learning



To measure the correctness of a model

 Error  $\epsilon = 1/n \Sigma(y- \hat{y})^2$
          $A = 1- \epsilon$

#### Types of Error
Type $I$ When the Prediction is true but the outcome is false
Type $II$ When the Prediction is false but the outcome is true


#### Confusion Matrix

|     | Predict +ve    | Predict -ve    |
| --- | -------------- | -------------- |
| +ve | True Positive  | False Negative |
| -ve | False Positive | True Negative  |

$Accuacy = \dfrac{TP + TN}{TP + TN +FP + FN}$

$Precision = \dfrac{TP}{TP+FP}$

$Recall = \dfrac{TP}{TP + FN}$

$Specificity =\dfrac{TN}{TN+TP}$

$F_1\ score = \dfrac{2*(recall*precision)}{recall + precision}$
#### Multi Class Confusion Matrix

| predicted -> | A   | B   | C   | D   |
| ------------ | --- | --- | --- | --- |
| A            | TP  | FN  | FN  | FN  |
| B            | FP  | TN  | TN  | TN  |
| C            | FP  | TN  | TN  | TN  |
| D            | FP  | TN  | TN  | TN  |

If there are $n$ classes, with respect to any class, only one cell is True Positive, $n-1$  cells are False Positive and False Negative, and $(n-1)^2$ are True Negative.



[[receiver-operating-class|Receiver Operating Class]]


