# Spam_Classification

The purpose of this project was to fit a number of known benchmark models with data being processed minimally and get a spam classifier with as high scoring metric as possible.

A spam emails dataset from [here](https://www.kaggle.com/datasets/jackksoncsie/spam-email-dataset) has been taken. Then some preprocessing has been done. I didn't went through a rigorous preprocessing on the data like tf-idf, vector embeddings, etc. since I wanted to make a model with a less complex and non-dependent preprocessing.

After preprocessing, I fitted 5 benchmark models on it, including Naive Bayes, Logistic Regression, Random Forest, XGBoost and Support Vector Classifier. A grid search has also been used for hyperparameter tuning wherever required and are finetuned to give a maximum score on the desired metric. Finally, the models with their respective best hyperparameters has been evaluated on the testing dataset.

In a spam classification, we identify a given email as either a spam or a ham (not spam). Now in the scoring point of view, marking a ham as spam is much more worse than marking a spam as a ham, due to the fact that even if the customer receives a spam message as being marked important/relevant, it would not be much of an issue. But if the customer did not received an important email just because it was marked as a spam, it would be a bigger problem. Hence in the above models, we tried to minimize the False Positives as much as possible. This can be achieved by keeping the precision high as much as possible. On this, we worked on maximizing the f1 score while keeping the Precision high.
