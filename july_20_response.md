# July 20 Response

Problem Statement:

Cats and Dogs:

1. I used RMSprop as my optimizer and set the learning rate to 0.001. I chose RMSprop because it works better on larger datasets that are split into batches than other optimizers, namely rprop.

2. For my loss function I used binary cross-entropy. It works by taking the mean of the negative log of the probability of each data point. The probability of each data point is between 0 and 1, as binary cross-entropy applies to data with two classes, meaning that if the probability is 1, there is a 100% chance the data pint has the corresponding label (the true class), and if the probability is 0, there is a 100% chance the data point has the other label. This is an effective method of penalizing bad predictions because as the predicted probability gets closer to zero for the true class (as it gets less accurate), the loss increases exponentially. 

3. The metric argument determines how the model's performance is judged. Like with the optimizer and loss functions, there are multiple options to choose from to determine how this is implemented. For example, the argument accuracy calculates how often the model's predictions equal the actual labels.

4. <img width="402" alt="image" src="https://user-images.githubusercontent.com/67920492/88466077-c85a5180-ce96-11ea-8b0b-7f55082658fb.png">

The model had a training accuracy of almost 98% and a validation accuracy of 60%, so it is clearly very overfit. This is reflected in the graphs above, as the validation set starts to drastically differ from the training set for both accuracy and loss at about 7 epochs.
