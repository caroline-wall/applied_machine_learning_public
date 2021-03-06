# July 8, 2020 Response

1. The training set is the data and answers that the model is provided in order to infer the rules. Therefore, the computer knows the labels that correspond to each image in the training data. While this is necessary for the computer to learn, it is not possible to see how accurate the model is using only this data because the answers are already provided. Therefore, the test set is what is used to test the model. Based on what it learned using the training set, the model can predict what label is most likely to be accurate for each image in the test set. This way, the rules it determined are being applied to new data in order to see just how accurate those rules are generally.

2. The relu function gets rid of any negative outputs from neurons. It looks for outputs that are less than 0 and replaces them with 0. It does this in order to keep those negative outputs from canceling out positive outputs later on. The softmax function makes it easier for you to determine which label is most likely. Normally, you would get an array showing the probability of each label being correct, and you'd have to find which is the greatest to determine the answer. Softmax does this for you by setting the label with the highest probability to 1 and the rest to 0. The 10 neurons in the last layer correspond to the 10 labels. The last step in the network is determining which of these labels (in this case a numerical value) is most appropriate for the image.

3. The optimizer and loss functions are how the model assesses how well it's doing and how it adjusts accordingly. The loss function calculates the error, while the optimizer updates each neuron's initially random parameters to have more appropriate weight/bias. The optimizer continues to do this over each epoch as the output of the loss function gets smaller and smaller, therefore, minimizing the error and creating a more accurate model.

4. a. 60,000 images, 28x28

   b. 60,000 labels
   
   c. 10,000 images, 28x28
