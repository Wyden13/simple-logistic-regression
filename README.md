# simple-logistic-regression
I implemented a simple logistic regression model class using Numpy for calculating vectorized values and matplotlib library for visualizing data points.
I document what I've learned and my understanding about it
## Sigmoid Function in Logistic Regression
$$h_\theta (x) = \frac{1}{1 + e^{(-\theta^T x)}} $$

Ideas:
- converting input into a value between 0 and 1 using Sigmoid Function, which denotes the probability
- The goal is to minimize the loss, which is the difference between the prediction and the actual value.
    - For label = 1: We want the predicted probability y = sigmoid(z) to be close to 1 (ideally > 0.5)
    - For label = 0: We want y = sigmoid(x) to be close to 0 (ideally < 0.5)

- Make the sigmoid output close to the true label(0 or 1) as much as possible --> The averaged loss across all samples is minimized
- How do we know if the sigmoid output is close enough to the actual value? We will use the log likelihood measurement to evaluate how good the model is. We would maximize the likelihood, or minimize the negative log likelihood in other words. The log likelihood measurement isn't used to directly change $$\theta$$; instead, we use it to derive the gradient, which tells us how to adjust θ to minimize the error.
- To minimize the loss -> adjust $$\theta$$ <- calculate the gradient with respect to $$\theta$$
- Once we have the gradient, we can use it in gradient descent to update $$\theta$$


