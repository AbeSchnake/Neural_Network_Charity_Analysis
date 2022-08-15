# Neural Network Charity Analysis

## Overview
This was a machine learning analysis done to evaluate the chances of charity dollars being successfully used by the organizations receiving donations.
## Results
### Data Preprocessing
* The charity spending was evaluated using the IS_SUCCESSFUL variable from the dataset as the target for the model.
* The features were all the rest of the columns in the data set with the exceptions of EIN, NAME, and SPECIAL_CONSIDERATIONS
* EIN, NAME, and SPECIAL_CONSIDERATIONS were removed because EIN and NAME can not be reasonably expected to causally contribute to the success of a charity, and SPECIAL_CONSIDERATIONS is just an indicator of whether there were any special considerations without any indication of what they were or whether they were positive or negative.
### Compiling, Training, and Evaluating the Model
* I chose to use 4 hidden layers of 50 neurons each 1 output layer. The activation functions for the hidden layers were tanh, Leaky Relu, tanh, and Leay Relu respectively. The activation function for the output layer was Sigmoid. I chose to put tanh layers before Leaky Relu layers because tanh layers produce negative numbers and Leaky Relu layers are good at handling negative numbers. I chose the sigmoid function because that was by far the best performing of the 4 functions based on my trial and error. I chose 4 layers and 50 neurons because after changing the parameters a lot those were the numbers after which I hit diminishing (or even negative in the case of neurons) returns.
* I was not able to hit the target model performance.
* I eliminated the Special Considerations column in the dadta set, I changed the nuber of hidden layers, I changed the number of neurons in each layer, and I changed the activation functions of the layers.
## Summary
In summary, the model I ended up with had an accuracy of .729. This is an improvement over the previous performance of .727, but it did not meet the target metric. In order to solve this classification problem, I reccomend a random forest machine learning model, because those models can handle the raw data without having to convert categorical variables to numbers or scaling the numerical data.
