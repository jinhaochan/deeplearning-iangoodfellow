## 1. Learning a XOR

Using a traditional linear model, its impossible for us to fit a nice linear line that separates the outputs of a XOR.

To recap, the XOR only outputs a 1 when only 1 of it's inputs is a 1. If both or none of the inputs are 1, then XOR outputs a 0

FF networks performs feature interation, and can collapse the feature space to a smaller one, thus making the data separable

## 2. Gradient Based Learning

FF networks are usually trained iteratively useing gradient based optimizers that drive the cost function to a low value.

## 2.1 Cost functions

1. Distribution Learning

The most commonly used cost function is cross-entropy, which calculates how different the distribution of the model's output is compared to the true output

Maximizing the Maximum Likelihood is the same as minimizing the cross entropy

2. Statistical Learning

The cost function can be **functional**, which means it maps functions to real numbers.

The neural network is thus seen as choosing the most optimal function, rather than the most optimal parameters

Using Mean Squared Error (MSE) and Mean Absolute Error (MAE) as cost functions lead to poor results when used with gradient based optimizers

Cross entropy is a more reliable cost function

## 2.2 Output units

Choice of the output unit is tightly coupled with the cost function

1. Linear Units: for Gaussian Output Distributions

2. Sigmoid Units: for Bernoulli Output Distributions

When using cost functions such as MAE and MSE, Sigmoid units saturates to 1 when the output is high, and saturates to 0 when the output is low.

When saturation happens, the gradients become very small and learning can become very slow. Thus it is better is use MLE

3. Softmax Units: for Multinoulli Output Distributions

Like the sigmoid unit, softmax units can saturate too when using MAE/MSE. Thus we should use MLE

## 3. Hidden units

1. ReLU and it's variant (Leaky ReLU, PReLU)

2. Logistic Sigmoid and Hyperbolic Tangent (tanH)



