# LSTM Numerical Example

This project provides a from-scratch Python implementation of a Long Short-Term Memory (LSTM) network. It processes a simple input sequence to demonstrate how an LSTM predicts the next value.

## Project Overview

The script calculates the internal states of an LSTM cell step-by-step for the input sequence X = [1, 2, 3]. The model architecture assumes an input dimension of 1 and a hidden state dimension of 1. During each time step, it computes the forget gate, input gate, output gate, and candidate values using predefined weights.

## Network Parameters

The implementation initializes the following arbitrary values for the LSTM parameters:

 
**Forget Gate Weights:** W_f = 0.5, W_hf = 0.1, b_f = 0 


 
**Input Gate Weights:** W_i = 0.6, W_hi = 0.2, b_i = 0 


 
**Candidate State Weights:** W_c = 0.7, W_hc = 0.3, b_c = 0 


 
**Output Gate Weights:** W_o = 0.8, W_ho = 0.4, b_o = 0 


 
**Initial States:** h_0 = 0, C_0 = 0 



## Prediction Mechanism

Because the model predicts a numerical sequence, the LSTM's output must be mapped to a real number. This is achieved by applying a linear transformation from the final hidden state to the predicted value.

**Linear Transformation Weights:** W_y = 4, b_y = 0 



## Final Output

At Time Step t=4, the script attempts to predict the next value in the sequence. After passing the sequence through the defined parameters and calculating the final linear transformation, the LSTM predicts 3.8. This value is close to 4, demonstrating that the model has successfully learned the underlying pattern.
