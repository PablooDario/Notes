# Metrics to Evaluate Machine Learning Algorithms

Evaluating our machine learning model is an essential step to know if we can apply this model to the whole dataset. If we apply the model to all the data before evaluating it, we may have erroneous results, as the model may be unbalanced, which would lead to overfitting or underfitting, making our results very poor. Before explaining the evaluation metrics, we'll see what underfit and overfit is.

## Underfit and Overfit

The error produced from the training set is known as Bias and the error by testing set is Variance.

In Underfit, the best fit line doesn’t cover many data points present. Thus, in the training dataset itself, there is a high chance of occurrence of error (high bias). And eventually in the testing dataset also (high variance).

In an overfit line, the best fit line covers every single data points, this may be well and good in the case of training dataset (low bias). But, when a testing dataset is provided to the same model, there will be a high error in the testing dataset (high variance).

But only a Good fit line, the best fit line will be in such a way that any point to be predicted will be accurately predicted. Consequently, it will still have a low bias and low variance.

![Precision&Acc](img/image3.png)

To avoid underfit and overfit we must have enough instances for generalization and several to ensure that the model performs well. Few instances will lead us to an underfit and too many to an overfit.

![Underfit&Overfit](img/image2.png)

Once we know why we have to evaluate our model, we will continue with some validation methods.

## Validation Methods

Before we apply the metrics to the model to see its performance we have to apply validation methods.Some of the most famous methods are:

- K Fold Cross Validation
- Leave One Out Cross Validation LOOCV
- Boostrap Sampling 

Finally after knowing the **validation methods** we are free to apply the validation metrics

## Metrics

The model may give satisfying results when evaluated using a metric say **accuracy_score** but may give **poor results** when evaluated **against other metrics** such as logarithmic_loss or any other such metric. That is why it's important to know the metrics and when to use them.

### Accuracy

It is the ratio of number of correct predictions to the total number of input samples. It works well only if there are equal number of samples belonging to each class.

For example, consider that there are 98% samples of class A and 2% samples of class B in our training set. Then our model can easily get 98% training accuracy by simply predicting every training sample belonging to class A. Classification Accuracy is great, but gives us the false sense of achieving high accuracy.

The real problem arises, when the cost of misclassification of the minor class samples are very high. If we deal with a rare but fatal disease, the cost of failing to diagnose the disease of a sick person is much higher than the cost of sending a healthy person to more tests.

$$\Huge Accuracy = \frac {Number of correct predictions}{Number of predictions made}$$

### Logarithmic Loss

Logarithmic Loss or Log Loss, works by penalising the false classifications. It works well for multi-class classification. When working with Log Loss, the classifier must assign probability to each class for all the samples. Suppose, there are N samples belonging to M classes, then the Log Loss is calculated as below :

$$\Huge Log Loss= \frac {-1}{N} \sum_{i=1}^{N}\sum_{j=1}^{M} y_{ij}*log(p_{ij})$$

Where:
- $y_{ij}\leadsto$ indicates whether sample i belongs to class j or not
- $p_{ij}\leadsto$ indicates the probability of sample i belonging to class j

Log Loss exists on the range [0, ∞); a result nearer to 0 indicates higher accuracy, whereas if the Log Loss is away from 0 then it indicates lower accuracy. In general, minimising Log Loss gives greater accuracy for the classifier.

### Presicion

It is the number of correct positive results divided by the number of positive results predicted by the classifier.

$$\huge Precision = \frac {TruePositives}{TruePositives + False Positives}$$

### Recall

It is the number of correct positive results divided by the number of all relevant samples (all samples that should have been identified as positive).

$$\huge Precision = \frac {TruePositives}{TruePositives + False Negatives}$$


### Confusion Matrix

Confusion Matrix as the name suggests gives us a matrix as output and describes the complete performance of the model.

![ConfusionMatrix](img/image15.png)

- **True Positives**: The cases in which we predicted YES and the actual output was also YES.
- **True Negatives**: The cases in which we predicted NO and the actual output was NO.
- **False Positives**: The cases in which we predicted YES and the actual output was NO.
- **False Negatives**: The cases in which we predicted NO and the actual output was YES.

Accuracy for the matrix can be calculated by taking average of the values lying across the “main diagonal” i.e

$$\Huge Accuracy = \frac {True Positive + True Negatives}{Number of predictions made}$$

There are a lot more, but the mentioned before are the most commonly used. Choosing the right metric depends on the type of problem you are addressing and your objectives. For example, if you are working on a spam detection problem, you may want to focus on accuracy and minimize false positives. If you are working on rare disease detection, you may be more interested in recovery to avoid false negatives.

In summary, choosing appropriate metrics is essential to evaluate the performance of your model and make informed decisions about the suitability of your model for your specific application. You should select metrics that best align with your objectives and take into account the context of the problem.