# July 15, 2020 Response

Convolutional Horses and Humans:

1. The ImageDataGenerator() pulls data from the directory or subdirectory in which it is stored in order to use that data. The command takes the argument rescale, which normalizes the images by dividing 1 by the highest pixel, so all the values are between 0 and 1. To flow from the directory to the generated object you need to create a generator object that calls the flow_from_directory() command and pass in the directory, target size, batch size, and class mode. The target size sets the size for each image, so they are consistent as they are passed through the neural network. When setting the class mode argument, you should think about the number of classes in your data. For example, if you have two classes, you would set the class mode to binary. The only things that change in this code between the training and testing datasets is the name of the generator and the directory that you pass in.

2. For my model, I used three convolutional layers, one of 16, one of 32, and one of 64, and three pooling layers. With each convolutional layer, the output shape decreased by two pixels, and with each pooling layer, the size of the image was cut in half. For my output layer, I chose the function sigmoid, which works well for binary classifications like this one, as it sets the output to 0 for one class and 1 for the other. Additionally, the sigmoid function allows the model to operate with only one neuron in the final layer. In the model compiler, I used binary crossentropy as my argument for loss, RMSprop with a learning rate of .001 for my optimizer, and accuracy as my metric.

Regression:

1. This plot shows the relationship between each variable in the auto-mpg dataset. With this plot, you are able to determine which variable might be correlated, providing insight to the dataset as a whole. For example, it seems that weight increases as displacement increases and vice versa. On the diagonal, each variable is compared to itself, therefore, instead of showing a relationship, these plots show the distribution of the data for that variable. According to this plot, it seems that both MPG and weight have close to a normal distribution.

<img width="654" alt="image" src="https://user-images.githubusercontent.com/67920492/87842226-d8f83f80-c878-11ea-8f20-02ed68fc9854.png">

2. Looking at these observations, it seems as though the model became slighlty overfit around the 998th step, as that point both the MAE and MSE began to increase.

However, when looking at the change in MSE throughout the epochs, it appears that model actually became overfit much earlier, around 100 epochs, as that is when the validating MSE begins to increase compared to the training MSE.
