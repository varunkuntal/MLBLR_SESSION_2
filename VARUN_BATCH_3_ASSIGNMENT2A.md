Session 2

0.mwp71v173u

>Welcome Everyone!
>

Administrative Stuff

    Assignments are shared already. Sorry for
    Google Drive link is also shared, you need to upload files to your respective batches.
    Deadline is tomorrow 11:30PM.
    Remember, only .md files would be recognized.

# Let's get started
## Normalization
## This is how filters look after training.

![Image](/images/image.png)

Value Chart
![Image](C:/Users/Marco/Desktop/S2MLBLR/images/image.png)

Do you see something wrong?

![Image](C:/Users/Marco/Desktop/S2MLBLR/images/image.png)

What is the difference in these two?
Without Normalization

image.gif
With Normalization

image.gif
Money distribution is normalized.
Back Propagation

Bacprop is something which can make you feel punching someone.

PUNCH

But there is hope!

image
Let's build things step by step.

After Session 1 we have some idea on how Neural Networks are built.

image
A NEURON/PERCEPTRON

A special block which can take multiple inputs and produces one output:

image
Let's build a few neurons

Let us assume that we got these inputs:
Variable Name 	Value
X1 	0
X2 	1
X3 	1
NEURON DYNAMICS OR HOW TO MAKE TEA?

SIMPLY JUST COMBINE (Combine 1 glass milk, 1 glass water, 1 glass sugar and 1 glass tea!)
Let us assume our neuron was programmed to output 1 if the sum below is more than 2:

sumsumsum = X1X_1X1​ + X2X_2X2​ + X3X_3X3​

DON'T SIMPLY JUST COMBINE, MIX WITH CARE (Build and then follow the recepie… I glass water, 1 Spoon Sugar…)

image

Instead of just adding these raw inputs, we assign them weights. Weights give importance to an input. To compute the putput, we will multiply input with respective weights
W1W_1W1​ = 0.5,
W2W_2W2​ = 1.5,
W3W_3W3​ = 0.7,
Variable Name 	Value 	Weight
X1 	0 	0.5
X2 	1 	1.5
X3 	1 	0.7

and compare with our threshold value:

sumsumsum = X1X_1X1​.W1W_1W1​ + X2X_2X2​.W2W_2W2​ + X3X_3X3​.W3W_3W3​
sumsumsum = 0∗0.5+1∗1.5+1∗0.70 * 0.5 + 1 * 1.5 + 1 * 0.70∗0.5+1∗1.5+1∗0.7 = 0+1.5+0.70 + 1.5 + 0.70+1.5+0.7 = 2.22.22.2

ADD SOME BIAS

Add some love to your Tea!

Each neuron also has a bias which can be thought of as how much flexible it is. It allows the line to move up or down to fir the prediction.

sumsumsum = X1X_1X1​.W1W_1W1​ + X2X_2X2​.W2W_2W2​ + X3X_3X3​.W3W_3W3​ + 111.bbb
ACTIVATION FUNCTION

IT takes the sum of weighted inputs as an argument and return the output of the neuron

image
FORWARD PROPAGATION, BACK PROPAGATION AND EPOCHS

Till now, we have computed the output and this process is known as Forward Propagation. But what if the estimated output is far away from the actual output (high error). In the neural network what we do, we update the biases and weights based on the error. This weight and bias updating process is known as Back Propagation.

Back-propagation (BP) algorithms work by determining the loss (or error) at the output and then propagating it back into the network. The weights are updated to minimize the error resulting from each neuron. The first step in minimizing the error is to determine the gradient (Derivatives) of each node w.r.t. the final output.

This one round of forward and back propagation iteration is known as one training iteration aka Epoch.
MULTILAYER PERCEPTRON

the single-layer network can do only so much. An MLP consists of multiple layers called Hidden Layers stacked in between the Input Layer and the Output Layer as shown below:
image
LETS MOVE ON TO THE THEORY NOW

BBT
But don't worry

bag
Broad Steps

Step 0: Read input and output
image

Step 1: Initialize weights and biases with random values (There are methods to initialize weights and biases but for now initialize with random values)

image

Step 2: Calculate hidden layer input:

hidden_layer_input = matrix_dot_product(X,wh) + bh

image

Step 3: Perform non-linear transformation on hidden linear input

hiddenlayer_activations = sigmoid(hidden_layer_input)

image

Step 4: Perform linear and non-linear transformation of hidden layer activation at output layer

output_layer_input = matrix_dot_product (hiddenlayer_activations * wout ) + bout output = sigmoid(output_layer_input)

image

Step 5: Calculate gradient of Error(E) at output layer

E = y-output

image

<div>

</div>

Step 6: Compute slope at output and hidden layer

`Slope_output_layer= derivatives_sigmoid(output)

Slope_hidden_layer = derivatives_sigmoid(hiddenlayer_activations)`

image

Step 7: Compute delta at output layer

d_output = E * slope_output_layer*lr

image

Step 8: Calculate Error at hidden layer

Error_at_hidden_layer = matrix_dot_product(d_output, wout.Transpose)

image

Step 9: Compute delta at hidden layer

d_hiddenlayer = Error_at_hidden_layer * slope_hidden_layer

image

Step 10: Update weight at both output and hidden layer

wout = wout + matrix_dot_product (hiddenlayer_activations.Transpose, d_output) * learning_rate

wh = wh+ matrix_dot_product (X.Transpose,d_hiddenlayer) * learning_rate

image

Step 11: Update biases at both output and hidden layer

bh = bh + sum(d_hiddenlayer, axis=0) * learning_rate

bout = bout + sum(d_output, axis=0)*learning_rate

image

REFERENCE

Hopefully this is how you are feeling :

image

And that's how it's done!
image
PYTHON FOUNDATION

Python 101

bit.ly/2F3fbkk
Assignment 2A

Rewrite the whole notebook with these rules:

    you can only use these variables: eip, mlblr, eip_in, eip_out, mlblr_in, mlblr_out, eip_list, eip_dict.
    once, you're done, you need to upload it to your Public Github account, learn how to commit a project to github, and then share the link to your assignment.
    deadline is t + 7 days.

Assignment 2B

    Write a python file to create the random needed to write the backprop table.
    Rewrite the Backpropagation table with new random values using MarkDown.
    Download Boostnote (or any markdown editor you prefer) and email back your file in this format FIRSTNAME_BATCH_X_ASSIGNMENT2B.md
    You can refer this link to learn about markdown: Markdown Cheatsheet

