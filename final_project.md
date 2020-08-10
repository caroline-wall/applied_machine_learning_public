# Final Project

![image](https://user-images.githubusercontent.com/67920492/89720102-a84d8680-d99c-11ea-82e6-6182221ec9f0.png)

Problem Statement:

Fake news is a prevalent danger in today’s society. The inability to distinguish between factual information and made-up stories posing as news has led to misinformed citizens, and therefore, a misinformed electorate, which is a challenge to democracy. This issue has been exacerbated recently with the coronavirus pandemic, as misinformation has become a great danger to public health. To quell this problem, it is necessary to create a model that distinguishes between news written by professional journalists and that written by non-professionals hoping to spread fake information. The model will be able to predict what category an article falls into for a reader trying to avoid fake news. This can be done through natural language processing by looking for patterns in sentence structure, word choice, and tone. This will require tokenization as well as an embedding layer in the model.

Data:

The dataset used for this model was downloaded from [Kaggle.com](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). It consisted of two csv files, one containing fake news article and the other containing real news articles. The fake news dataset had 23,481 observation each with four features: title, text, subject, and date. The real news dataset had 21,417 observations with the same four features. The date column consisted of ordinal data, while the other features were all nominal data. All the fake news text included was published in 2015, 2016, or 2017, while the real news text was all published in 2016 or 2017. The data was imported into the script as separate pandas DataFrames. Only the text feature was used in the model, so for both sets of data, each observation from the text column was put into a list. Both lists were then combined into one array and shuffled. Additionally, each text was tokenized and padded at the end to match the length of the longest text. A second array was made in the same way to hold the label of fake or real for each text. Fake news was codified as 1, and real news was codified as 0. This array held the same order as the text array, so each text had a corresponding label. Of the total 44,898 observation, 35,000 were used for training, and the remaining 9,898 were used for testing.

Methods:

The model itself consisted of an embedding layer, a global average pooling layer, and two dense layers. A sigmoid activation was used in the final dense layer as the model is being used to predict probability, which exists between 0 and 1. Binary crossentropy was chosen as the loss function, and adam was chosen as the optimizer.

<img width="538" alt="image" src="https://user-images.githubusercontent.com/67920492/89745810-2769ba00-da84-11ea-8027-48c03497d60c.png">

Model Performance:

The model performed with a training accuracy of 0.9965, a training loss of 0.0166, a validation accuracy of 0.9958, and a validation loss of 0.215. This was higher than expected and means that, for the most part, the model was neither overfit nor underfit. In fact, this model unexpectedly performed better than the model found in [another study](https://onlinelibrary.wiley.com/doi/epdf/10.1002/spy2.9), in which n-grams, feature extraction, and other, more sophisticated methods were used. This difference is likely due to the dataset on which this model was trained. Most of the real news text was formatted in a way such that it began with the name of the city in which the news occurred in all caps. Therefore, it is likely had an easier time picking up on whether a text was fake or real, as it was able to rely on that significant formatting difference. This suspicion could easily be proven true or false if a different dataset was used for training.  

Project Proposal:

Ideally, this model will be able to be used as a real time fake news identifier in which internet users are able to copy and paste text into the detector's webpage and run the model or use an extention that runs the model. This would then have an output that is a percentage describing the likelihood that the text is fake. Therefore, readers will be able to immediately identify potentially fake news and avoid harmful misinformation. However, quite a bit more work and investigation would have to be done to reach this point. First and foremost, due to this potential issue mentioned above, the model would need to be rerun on a brand new dataset in which the fake news and real news are formatted identically and would need to be adjusted based on that performance until accuracy is increased and overiftting is minimized. This could also be done by including more preprocessing of the text as a method of formatting rather than attempting to find an already existing dataset that adheres to that criteria. Furthermore, a predictive component will need to be added after the model is trained, and this will need to formatted to a percentage so as to be more readable for users. Additionally, to do this, a path must be implented to load the submitted text into the predictive model.

