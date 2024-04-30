<h2>Optimization in Neural Networks</h2>

<h3>Regression with a perceptron</h3>

We can model a regression problem to predict the price of a house given the size of the house as a single perceptron.To do this, we train a neural network using the gradient descent algorithm. The fundamental unit of neural networks is called a perceptron. The perception is going to take some inputs into some unknown outputs that we want to predict. 

The inputs to the perceptron here are going to be $x_1$ and $x_2$ corresponding to the size of a house and a number of rooms. If there were 100 inputs, it would simply be 100 notes $x_1$ all the way to $x_100$. We start with the inputs and then they plug into a summation function. Out of the summation function comes the output $\hat{y}$ and that's going to be what we predict to be the the price of the house.

<img src="Images/reg_with_perceptron.png" alt="Regression with a Perceptron" width="500" height="600">


![Regression with a Perceptron](https://github.com/chuksoo/Mathematics-for-Machine-Learning-and-Data-Science-Specialization/blob/main/Images/reg_with_perceptron.png)

What happens in the summation step is that each of these features, $x_1$ and $x_2$ is multiplied by a corresponding weight to determine how
important it is for the output. So for example, if the size of a house is way more important to predict the price of a house than the number of rooms, then this will have a higher weight than the number of rooms. So let's call the corresponding weights $w_1$ and $w_2$. And to combine these weights and the input, we simply add them. So we multiply $w_1$ the weight times $x_1$ the feature and we add $w_2$ times $x_2$. We then add the bias term to the summation function to get the output. 

In this model there's no activation function. The output is simply:

```math
\begin{equation}
    \hat{y} = w_1*x_1 + w_2*x_2 + b 
\end{equation}
```

where $\hat{y}$ is the predicted price of the house. The goal is to find the best $w_1$, $w_2$ and $b$ - the weights and bias respectively that will optimize predictions. i.e., the ones that will, when we plug in $x_1$ and $x_2$ give us the closest to the actual price for the entire data set. To do this, we minimize the error which is basically how far we are from the price of the house. The loss function is a little function that's going to tell us, how far are we from predicting the prices well.