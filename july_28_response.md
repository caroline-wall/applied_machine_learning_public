# July 28, 2020 Response

Word Embeddings:

1. One-hot encoding is when each word points to a vector in which it is encoded as 1 and the other words in the vocabulary are encoded as 0. This is inefficient, as it creates a vector for each word, but the vector is only giving information about that one word. That means that each vector is mostly made up of zeros, sparse vectors, so it is a waste of creating that many vectors. Instead, it would be more efficient to encode each word with a unique number, so the whole vocabularly could be encoded in one vector, a dense vector. Furthermore, dense vectors can be used to understand which words may have similar meanings by encoding each word as a set of floats. A similar vector of floats can indicate similar meaning between words.

2. According to the graphs of training and validation loss and accuracy, the model is clearly overfitting. This could possibily be because of padding, as zero-padding was used in the input, which could have affected the output. Additionally, the test data may have included words that the model had not seen in training that it was unable to properly embed. To help control overfitting, possibly a larger training dataset should have been used or a smaller model.

<img width="630" alt="image" src="https://user-images.githubusercontent.com/67920492/88712540-e10d7600-d0e7-11ea-8417-6291c7831e7a.png">
<img width="642" alt="image" src="https://user-images.githubusercontent.com/67920492/88712616-00a49e80-d0e8-11ea-944e-95b0b20c21b6.png">

Text Classification with an RNN:

1. The first model was compiled with one LSTM layer. This led to an overfit model, as seen in the first two graphs below. With another LSTM layer, the model continues to be just as overfit, as seen in the bottom two graphs, and in fact, is even more off on its prediction of the sample text than the original model. The validation accuracy and loss only stay with that of the training set for about one epoch, then it begins to reverse. Although the same thing occurs in the original model, the reversal in the validation accuracy and loss does not seem to be quite as sharp, indicating that that may be the better model of the two.

<img width="351" alt="image" src="https://user-images.githubusercontent.com/67920492/88815443-5da46100-d189-11ea-80ba-c8bf0dd35697.png">
<img width="345" alt="image" src="https://user-images.githubusercontent.com/67920492/88815540-71e85e00-d189-11ea-8db6-ada172b47802.png">

<img width="427" alt="image" src="https://user-images.githubusercontent.com/67920492/88819667-4c118800-d18e-11ea-9027-61354ec2873e.png">
<img width="425" alt="image" src="https://user-images.githubusercontent.com/67920492/88819715-5cc1fe00-d18e-11ea-96aa-4944951c6ef2.png">

