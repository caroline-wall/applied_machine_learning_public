# Final Project

![image](https://user-images.githubusercontent.com/67920492/89720102-a84d8680-d99c-11ea-82e6-6182221ec9f0.png)

Problem Statement:

Fake news is a prevalent danger in today’s society. The inability to distinguish between factual information and made-up stories posing as news has led to misinformed citizens, and therefore, a misinformed electorate, which is a challenge to democracy. This issue has been exacerbated recently with the coronavirus pandemic, as misinformation has become a great danger to public health. To quell this problem, it is necessary to create a model that distinguishes between news written by professional journalists and that written by non-professionals hoping to spread fake information. The model will be able to predict what category an article falls into for a reader trying to avoid fake news. This can be done through natural language processing by looking for patterns in sentence structure, word choice, and tone. This will require tokenization as well as an embedding layer in the model.

Data:

The dataset used for this model was downloaded from Kaggle.com. It consisted of two csv files, one containing fake news article and the other containing real news articles. The fake news dataset had 23,481 observation each with four features: title, text, subject, and date. The real news dataset had 21,417 observations with the same four features. The date column consisted of ___ data, while the other features were all ___ data. All the fake news text included was published in 2015, 2016, or 2017, while the real news text was all published in 2016 or 2017. The data was imported into the script as separate pandas DataFrames. Only the text feature was used in the model, so for both sets of data, each observation from the text column was put into a list. Both lists were then combined into one array and shuffled. A second array was made in the same way to hold the label of fake or real for each text. Fake news was codified as 1, and real news was codified as 0. This array held the same order as the text array, so each text had a corresponding label. 

Methods:

A sigmoid activation was used as ___ .

Model Performance:

The model performed with a training accuracy of _ , a training loss of _ , a validation accuracy of _ , and a validation loss of _ . This was higher than expected and may be due to the dataset used. Most of the real news text was formatted in a way such that it began with the name of the city in which the news occurred in all caps. 

Project Proposal:



