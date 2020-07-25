# July 20, 2020 Response

Problem Statement:

Cats and Dogs:

1. I used RMSprop as my optimizer and set the learning rate to 0.001. I chose RMSprop because it works better on larger datasets that are split into batches than other optimizers, namely rprop.

2. For my loss function I used binary cross-entropy. It works by taking the mean of the negative log of the probability of each data point. The probability of each data point is between 0 and 1, as binary cross-entropy applies to data with two classes, meaning that if the probability is 1, there is a 100% chance the data pint has the corresponding label (the true class), and if the probability is 0, there is a 100% chance the data point has the other label. This is an effective method of penalizing bad predictions because as the predicted probability gets closer to zero for the true class (as it gets less accurate), the loss increases exponentially. 

3. The metric argument determines how the model's performance is judged. Like with the optimizer and loss functions, there are multiple options to choose from to determine how this is implemented. For example, the argument accuracy calculates how often the model's predictions equal the actual labels.

4. The model had a training accuracy of almost 98% and a validation accuracy of 60%, so it is clearly very overfit. This is reflected in the graphs below, as the validation set starts to drastically differ from the training set for both accuracy and loss at about 7 epochs.

<img width="402" alt="image" src="https://user-images.githubusercontent.com/67920492/88466077-c85a5180-ce96-11ea-8b0b-7f55082658fb.png">

5. Overall, the model did not perform well in practice, as it was only able to correctly identify one of the three dogs. This is most likely because the model is overfit and unable to generalize enough to properly classify these images. To combat this, we could try employing image augmentation, so the model is trained on a greater sample of images, as images could be rotated, zoomed, or flipped to create more data. We could also apply dropout, which is a regularization technique that makes the distribution of weight values more regular.

Prediction: cat\
![image](https://user-images.githubusercontent.com/67920492/88466194-e2486400-ce97-11ea-9089-4e21e083ff9c.png)

Prediction: cat\
![image](https://user-images.githubusercontent.com/67920492/88466199-f0968000-ce97-11ea-861e-30719308da2d.png)

Prediction: cat\
![image](https://user-images.githubusercontent.com/67920492/88466210-fc824200-ce97-11ea-8d58-65a57f795215.png)

Prediction: cat\
![image](https://user-images.githubusercontent.com/67920492/88466215-086e0400-ce98-11ea-9ebd-2c33df92d530.png)

Prediction: cat\
![image](https://user-images.githubusercontent.com/67920492/88466223-12900280-ce98-11ea-8c91-31f3530cd125.png)

Prediction: dog\
![image](https://user-images.githubusercontent.com/67920492/88466229-1cb20100-ce98-11ea-8cf9-392a1ecf0e00.png)
