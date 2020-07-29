# July 29, 2020 Response

NLP Sarcasm Classifier:

1. I selected three headlines each from CNN, MSNBC, and NPR. While only one of the headlines was overtly sarcastic, the classifier was still able to pick up on some of the snark present in these headlines. For example, one of the highest predictions came from the CNN headline "GOP congressman who frequently refuses to wear a mask tests positive." This is a factually true statement, but the classifier was still able to recognize the irony that CNN is trying to emphasize. Additionally, the classifier recognized, to some extent, headlines that referred to less serious topics, such as the MSNBC headline "Expert shopping: national lipstick day." However, the classifier was not always accurate, as the headline with the highest probability of sarcasm was "A landmark study shows what makes a successful relationship." While this was in fact a serious article about a real study, the headline could be interpreted as sarcastic, especially when compared to the subjects of other serious articles.

Text Generation with an RNN:

1. The text generator did a fairly good job of imitating the style of Shakespeare, however, the content does not actually make sense. The generator was best of replicating the format. The lines read like a Shakespeare play, with the speaker's name in all caps, commas at the end of most lines, and each new line beginning with a capital letter. Some common phrases the generator seemed to remember well, such as "O, good" or the beginning words of questions, but these were often followed by a nonsensical collection of words, so while the generator learned how to form different types of sentences, it was unable to chose content words that made sense.
