# July 9, 2020 Response

1. TF Hub is a library that gives you access to parts of machine learning models and datasets. For this script, we used TF Hub to create the first layer of our neural network, which embeds a sentence and stores the embedding in a vector.

2. The optimizer and loss functions are how the model calculates its error and adjusts the parameters of each neuron from their initial random values, so the model's error decreases. The model had an accuracy of 87%, which was fairly good for how basic the model was.

3. https://github.com/caroline-wall/applied_machine_learning_public/issues/1#issue-655455805
The first graph shows how the loss changed over the course of the epochs for both the training data and the testing data. For both, the loss tends to decrease, showing that the model is becoming more accurate with each epoch as the parameters are adjusted. However, the validation loss starts to even out, as the model becomes unable to get more accurate. This shows that the model may be overfit, as the model does better on the training data than data it has not seen before, so it is unable to adjust for the new data after a certain point. 

4. The second graph shows how the accuracy changed over the course of the epochs for the training data and the testing data. For both, the accuracy is incresing, showing that the model is becoming more accurate with each epoch as the parameters are adjusted. However, the validation accuracy starts to plateau at about 12 epochs. Similarly to the previous graph, this shows that the model may be overfit because it is doing better on the training data than on the testing data.
