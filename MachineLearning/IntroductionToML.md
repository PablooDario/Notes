# Introduction To Machine Learning
Term coined in 1959 by Arthur Samuel in the context of solving the checkers game through a Machine.

The **program** or the machine **can deduce information on its own and appy it in another time**. A program can learn to produce a behaviour for which it wasn't programmed and from which the programer can't be concious.

**Machine Learning** is a subtask of the Artificial Intelligence which is responsible of the induction of a model through a learning process.

Machine learning can also be defined as the process of solving a practical problem by gathering a dataset, and algorithmically building a statistical model based on that dataset

## Supervised Learning 
In supervised learning, the dataset is the collection of labeled examples. Each element $x_i$ among $N$ is called a feature vector. A feature vector is a vector in which each dimension $j = 1, \dots , D$ contains a value that describes the example somehow. That value is called a **feature** and is denoted as $x^{(j)}$. For instance, if each example $x$ in our collection represents a person, then the first feature, $x^{(1)}$, could contain height in cm, the second feature, $x^{(2)}$, could contain weight in kg, $x^{(3)}$ could contain gender, and so on. For all examples in the dataset, the feature at position $j$ in the feature vector always contains the same kind of information. The label $y_i$ can be either an element belonging to a finite set of classes $\{1, 2, \dots , C\}$, or a real number, or a more complex structure. For instance, if your examples are email messages and your problem is spam detection, then you have two classes {*spam, not_spam*}.

The goal of a **supervised learning algorithm** is to use the dataset to produce a model that takes a feature vector $x$ as input and outputs information that allows deducing the label for this feature vector. For instance, the model created using the dataset of people could take as input a feature vector describing a person and output a probability that the person has cancer.

### Classification problems
This algorithm **helps to predict a discrete value.** It can be thought, the input data as a member of a particular class or group. For instance, taking up the photos of the fruit dataset, each photo has been labelled as a mango, an apple, etc. Here, the algorithm has to classify the new images into any of these categories.

- **Naive Bayes Classifier**
- **Support Vector Machines**
- **Logistic Regression**

### Regression problems
These problems are used for **continuous data.** For example, predicting the price of a piece of land in a city, given the area, location, number of rooms, etc. And then the input is sent to the machine for calculating the price of the land according to previous examples. Examples-

- **Linear Regression**
- **Nonlinear Regression**
- **Bayesian Linear Regression**

## Unsupervised Learning

This learning algorithm is **completely opposite to Supervised Learning. In short, there is no complete and clean labelled dataset** in unsupervised learning. Unsupervised learning is self-organized learning. Its main aim is to explore the underlying patterns and predicts the output.  Here we basically provide the machine with data and **ask to look for hidden features and cluster the data in a way that makes sense.**

- **K – Means clustering**
- **Neural Networks**
- **Principal Component Analysis**

## Reinforcement Learning

It is neither based on supervised learning nor unsupervised learning. Moreover, here **the algorithms learn to react to an environment on their own.** It is rapidly growing and moreover producing a variety of learning algorithms. These algorithms are useful in the field of Robotics, Gaming etc.

For a learning agent, **there is always a start state and an end state.** However, to reach the end state, there might be a different path. In Reinforcement Learning Problem **an agent tries to manipulate the environment.** The agent travels from one state to another. The agent gets the reward(appreciation) on success but will not receive any reward or appreciation on failure. In this way, the agent learns from the environment.

![Types of Models](img/image.png)

|               |**Supervised**                 |**Unsupervised ML**                           	   |**Reinforcement ML**
|---            |---                            |---                                               |---
|**Definition**	|Learns by using labelled data	|Trained using unlabelled data without any guidance|	Works on interacting with the environment
|**Type of data**|Labelled data	                |Unlabelled data	                               |No – predefined data
|**Type of problems**|Regression and classification|Association and Clustering|	Exploitation or Exploration
|**Algorithms**|Linear Regression, Logistic Regression, SVM, KNN...|K – Means, C – Means, Apriori...|Q – Learning, SARSA...
|**Aim**|Calculate outcomes|Discover underlying patterns|Learn a series of action
|**Application**|Risk Evaluation, Forecast Sales|Recommendation System, Anomaly Detection|Self Driving Cars, Gaming, Healthcare
