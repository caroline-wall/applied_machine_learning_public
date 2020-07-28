# July 22, 2020 Response

Boosted Trees:

1. A one-hot-encoded column is one in which categorical data has been transformed into numerical data, so all the features are defined as numbers for the model. The source values are discrete because they correspond to a label, meaning that there is a finite list of options.

2. A dense feature transforms the data stored in the variable example into an array of floats. This is useful as it provides uniformity in the data because each feature column now holds floats.

3. The logistic regression (the first set of graphs) predicted that most passengers did not survive. While the boosted trees model predicted the same thing, the predicted probabilities show that the prediction were more certain those of the logistic regression, as the majority of the probabilities lie very close to 0 or 1 with much fewer from 0.2 to 0.8. This may explain why the ROC curve for the boosted trees model lies closer to the top left corner than for the logistic regression, as the true positive rate climbs quicker than the false positive rate, meaning that a greater proportion of the model's predictions are true positives than are false positives. Additionally, the boosted trees model seems to have a greater AUC, which is a general measure of predictive accuracy and is correct here, as the boosted tree model has an accuracy of 81.8%, whereas the logistic regression has an accuracy of 76.5%.

<img width="344" alt="image" src="https://user-images.githubusercontent.com/67920492/88494218-f9b04b80-cf82-11ea-95a7-23d9577fec03.png">
<img width="347" alt="image" src="https://user-images.githubusercontent.com/67920492/88494246-32502500-cf83-11ea-95e6-49617edbcb68.png">
<img width="341" alt="image" src="https://user-images.githubusercontent.com/67920492/88494400-f4073580-cf83-11ea-822b-f57f0cde2808.png">
<img width="358" alt="image" src="https://user-images.githubusercontent.com/67920492/88494420-0aad8c80-cf84-11ea-8fc2-b60029bcf593.png">

Boosted Trees Continued:

1. The feature values contribution histogram shows how each feature affects the predicted probability for a specific passenger. The red bars represent features that have a negative affect on the probability. In this model, the probability spans from 0 to 1, with 1 meaning that there is 100% chance that the passenger survived. Therefore, negative features indicate subtractions in the probability, moving the probability prediction closer to 0, which coincides with having a 0% chance of survival, or a 100% chance of not surviving. The green bars represent features with the opposite effect, moving the probability closer to 1. Additionally, the length of each bar shows how big an effect that feature has on predicting survival. As you can see, sex plays a large role, and males have a lower chance of survival.

The violin plot shows similar patterns but instead of depicting the magnitude of each feature for a specific example, it shows the value for that example as well as the general distrubtion of each feature. The blue areas represent the range and distribution of each feature, so the example can be seen in context. For example, it can be seen that this passenger is a male and that there are more males than female and they are more likely to not survive.
