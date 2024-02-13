# Module 21 - Deep Learning Challenge
### Overview

The purpose of this analysis was to create a deep learning tool that will help the nonprofit foundation Alphabet Soup select applicants for funding with the best chance of success in their ventures. I created a binary classifier that can predict whether applicants will be successful if funded by alphabet soup.

### Results

* Data Preprocessing

  * **What variable(s) are the target(s) for your model?**
    * The column 'IS_SUCCESSFUL' was the target for the model as this is the binary metric that told us whether an applicant received an offer or not.
  * **What variable(s) are the features for your model?**
    * The rest of the table.
  * **What variable(s) should be removed from the input data because they are neither targets nor features?**
    * The EIN, NAME, STATUS and ASK_AMT columns.
  
* Compiling, Training, and Evaluating the Model
  
  * **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
    * I used 50 and 20 neurons in my 2 hidden layers, respectively, and the activation functions ReLU, Tanh, and sigmoid to start. I first played around with the activations functions. We are dealing with scaled values between 0 and 1, so the activation function ReLU for the hidden layers was appropriate. Then, I decided that since the output is binary of 0 or 1, the sigmoid function seemed to be the best option for the output layer. Once I determined that accuracy stalled around 70 epochs, I then played around with the number of neurons.
      * 100 epochs delivered an accuracy of 0.73 and a loss of 0.55.
      * 200 epochs delivered an accuracy of 0.72 and a loss of 0.55.
      * accuracy and loss stalled at around 70 epochs.
      * sigmoid 3x + 50 epochs = Loss: 0.5492346286773682, Accuracy: 0.7276967763900757
      * Hidden layers: 
        * 100 and 200 epoch tests above done with ReLU and Tanh
        * changing both layers to ReLU
  * **Were you able to achieve the target model performance?**
    * I was not able to reach 85% accuracy unfortunately.
  * **What steps did you take in your attempts to increase model performance?**
    * I first played around with the activations functions. We are dealing with scaled values between 0 and 1, so the activation function ReLU for the hidden layers was appropriate. Then, I decided that since the output is binary of 0 or 1, the sigmoid function seemed to be the best option for the output layer. Once I determined that accuracy stalled around 70 epochs, I then played around with the number of neurons. It didnt seem like changing the number of neurons created any effect in the model's accuracy. I ultimately decided that 100 neurons per layer and 200 epochs were the most effective changes to make as they increased the accuracy the most, albeit not much.

# Summary

In this challenge, I created a model that is does not produce reliable outputs. The best way I can think of to create a better model is to utilize the keras tuner to determine the optimal conditions for such a model via a function. 

### References

IRS. Tax Exempt Organization Search Bulk Data Downloads. [https://www.irs.gov/](https://www.irs.gov/charities-non-profits/tax-exempt-organization-search-bulk-data-downloads)
    -
