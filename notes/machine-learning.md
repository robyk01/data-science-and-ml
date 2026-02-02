# Machine Learning
We use machine learning to make predictions around the data we have.

## Supervised Learning
When we have a set of data and provide with x **the input** and y **the label**. The goal for the model is to create relationship so that it can label data it hasn't seen before

- Regression
  Predicting a continuous number. Eg. predicting a house price
- Classification
  Predicting a discrete category. Eg. predicting if an email is spam or not

## Unsupervised Learning
We provide the computer only the inputs and let it set labels based on patterns and structures

- Clustering
  Grouping similar data points together. Eg classifying movies based on category
- Dimensionality Reduction
  Simplifying complex data. 

## Linear Regression
It's a supervised learning algorithm used to predict a continuous dependent variable. We draw a line and try to make it go straight through the middle of data points in a graph.

**Formula**: y = mx + b

### Loss Function
The computer uses a loss function to measure how wrong it is. For regression, we usually use **MSE** (Mean Squared Error).
To know if the line we drew is good or not:
- It looks at the residuals (the distance between the line and data points)
- If the dots are far from the line, the loss is high
- If the dots hug the line, the loss is low
- It squares the distance and takes the average of them


### Gradient Descent
To find the best line, the computer needs to minimize the MSE. It uses an algorithm called Gradient Descent.
It's the vector of partial derivatives. We move in the opposite direction to find the minimum error.


## Logistic Regression
It's a supervised learning algorithm used to predict a discrete variable. This is the most popular algorithm for Binary Classification (Eg spam filtering).
In Linear Regression our line (mx + b) can go to infinity. In Classification, we need a probability between 0 and 1.

To fix this, we pass the mx + b result through a Sigmoid Function:
σ(z) = 1 / 1 + e^-z
- If the mx + b is a huge positive number, the Sigmoid turns into 0.99 (99% probability)
- If it's a huge negative number, it turns into 0.01 (1% probability)
- If it's exactly 0, it turn into 0.5 (50% probability)

By default, the model uses 0.5 as the cutoff:
- Prob ≥ 0.5 -> Class 1
- Prob < 0.5 -> Class 0

