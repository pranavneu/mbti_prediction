# Myers-Briggs Personality Prediction

### Objectives and Significance:
The primary objective of this project is to explore potential connections between an individual's Myers-Brigg Type Indicator (MBTI) and their personal writing style in social media data. The Myers-Briggs Type Indicator is a personality assessment tool used to categorize individuals into one of 16 personality types. The goal of this project is to analyze the textual data using learning models such as logistic regression, support vector machine (SVM), and random forests to predict an individual’s MBTI type.
The possibility of a presence of patterns between MBTI types and personal writing styles gives insight into the general validity of the personality test's ability in analyzing, predicting, and categorizing behavior. Having a better understanding of one’s personality can be useful in a variety of ways such as improving personal counseling and education effectiveness, focused ad-marketing, and focused digital content. This large range of practical applications is one of the key motivators of this project. Additionally, although the Myers-Briggs Type Indicator is not a recent addition to the landscape of personality assessments, it has shown its ability to remain consistently relevant despite the countless newer tests created after. Thus, this project is also motivated by a desire to understand the rationale behind this steady relevance.
The data has been sourced from two distinct social media related datasets: the Personality Café Forum and Twitter. Following data collection, a range of features have been extracted from the comments utilizing diverse methods such as sentiment analysis and the application of natural language processing tools like nltk for grammatical tagging. Due to an imbalance in class distribution within the dataset, a Synthetic Minority Over-sampling Technique (SMOTE) has been employed to generate artificial samples for the minority classes. Upon completion of feature extraction, various modeling techniques, including logistic regression, decision trees/xgboost, naive bayes, and support vector machines, have been employed to facilitate predictions. Notably, the classification problem at hand is treated as a multilabel one, where each letter in the final label is considered an independent label. The outcomes of the models indicate comparable accuracies across all three approaches. Specifically, predictions for labels pertaining to Extroverted/Introverted and Sensors/Intuitive exhibit an accuracy of approximately 73%. In contrast, predictions for labels associated with Feelers/Thinkers and Judgers/Perceivers demonstrate a noticeable decrease to around 60%, signifying a substantial deviation compared to the accuracy achieved for the other two labels.
