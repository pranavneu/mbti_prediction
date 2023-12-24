# Myers-Briggs Personality Prediction

### Objectives and Significance:
The primary objective of this project is to explore potential connections between an individual's Myers-Brigg Type Indicator (MBTI) and their personal writing style in social media data. The Myers-Briggs Type Indicator is a personality assessment tool used to categorize individuals into one of 16 personality types. The goal of this project is to analyze the textual data using learning models such as logistic regression, support vector machine (SVM), and random forests to predict an individual’s MBTI type.
The possibility of a presence of patterns between MBTI types and personal writing styles gives insight into the general validity of the personality test's ability in analyzing, predicting, and categorizing behavior. Having a better understanding of one’s personality can be useful in a variety of ways such as improving personal counseling and education effectiveness, focused ad-marketing, and focused digital content. This large range of practical applications is one of the key motivators of this project. Additionally, although the Myers-Briggs Type Indicator is not a recent addition to the landscape of personality assessments, it has shown its ability to remain consistently relevant despite the countless newer tests created after. Thus, this project is also motivated by a desire to understand the rationale behind this steady relevance.
The data has been sourced from two distinct social media related datasets: the Personality Café Forum and Twitter. Following data collection, a range of features have been extracted from the comments utilizing diverse methods such as sentiment analysis and the application of natural language processing tools like nltk for grammatical tagging. Due to an imbalance in class distribution within the dataset, a Synthetic Minority Over-sampling Technique (SMOTE) has been employed to generate artificial samples for the minority classes. Upon completion of feature extraction, various modeling techniques, including logistic regression, decision trees/xgboost, naive bayes, and support vector machines, have been employed to facilitate predictions. Notably, the classification problem at hand is treated as a multilabel one, where each letter in the final label is considered an independent label. The outcomes of the models indicate comparable accuracies across all three approaches. Specifically, predictions for labels pertaining to Extroverted/Introverted and Sensors/Intuitive exhibit an accuracy of approximately 73%. In contrast, predictions for labels associated with Feelers/Thinkers and Judgers/Perceivers demonstrate a noticeable decrease to around 60%, signifying a substantial deviation compared to the accuracy achieved for the other two labels.

### Distinction of this Project:
While previous works have explored personality prediction using diverse personality tests, this project distinguishes itself through the integration of two distinct datasets. Unlike the literature surveyed, none have combined these particular datasets. The text data utilized for analysis are from PersonalityCafe.com and Twitter, both in social media post form. The primary source of the dataset was PersonalityCafe.com with specific samples of data from the Twitter dataset added to address imbalance issues. Also, VADER, a nltk module, was utilized to perform sentiment analysis due to its efficiency in social media data.
Before initiating the project, a preliminary examination of the data revealed a significant skew despite the added data. Some MBTI types had considerably more data than others. To address this imbalance, the project also employed SMOTE analysis to equalize the weighting of the data, mitigating disparities in class distribution.

### Methodology:
![Picture1](https://github.com/pranavneu/mbti_prediction/assets/154646829/108fd528-8e84-4117-abd6-31c2d657cd9f)
This project’s dataset was a combination of two datasets from Personality Café Forum and Twitter, respectively. Both of these datasets are now accessible on Kaggle as well. The Personality Café data set had around 8600 rows and the Twitter data set had over 7800 rows of data. The Personality Café data was used fully, but the imbalance was large. Thus, data relating to specific minority MBTI types were drawn from the Twitter dataset to achiever higher prediction accuracies. The final combined dataset consisted of approximately 12,555 rows, each row with posts from a unique user. Both datasets had “|||” pipelines within each row separating different comments made from users. Upon removal of the pipelines symbol, the entire dataset revealed a total of 975,145 posts. The initial column of the final dataset indicates the user’s MBTI type and the second column contains the individuals' posts.

### Findings:
The main objective of this research was to consider the efficacy of MBTI personality type prediction using text and sentiment analysis. This was done using various libraries and modules in Python such as pandas, sklearn and nltk. To reach the objective, sentiment analysis was combined with data balancing measures such as data set combination and SMOTE, general pre-processing measures, and detailed implementations of five machine learning classifiers
Notably, the strategic implementation of SMOTE yielded promising outcomes across all models. By generating synthetic instances of the minority class, SMOTE effectively addressed the skewed distribution, allowing the models to better capture the nuances of the minority classes. The observed stabilizing of the F1 score in the XGBoost algorithm as we increased the depth highlighted a crucial relationship between parameters, especially in the context of an imbalanced dataset. The flattening of the graph shows the relation between the depth of the model and the imbalanced dataset. This highlights the requirement of a large balanced dataset to increase the F1 score and build a better model.
The F1 score proved to be a pivotal metric in the context of data classification, it demonstrated reliable performance, but it could have improved. There were some interesting nuances in the data that indicated the need for improvements in the SVM models’ F1 accuracies. From the results section’s SVM Metrics table, the F1 scores’ basis, which leverages on the precision and recall scores, was unbalanced. For all four dichotomies, either the precision was high with a low recall or the opposite. These imbalances have a high chance of being due to imbalanced data. Additionally, in SVM, the AUC scores were low for two of the dichotomies: F/T and P/J. This could be due to class imbalance or insufficient feature representation in the data set. By creating a larger dataset with more information related to those in categories such as Extrovert, we would be able to better represent all MBTI types and achieve better scores in AUC, F1, and more.
Considering the target variables as independent made it feasible to use logistic regression. The binary models for personality traits exhibit varying performances. E/I and S/N show strong alignment between AUC and accuracy while F/T and J/P indicate complexities in classification. This variability in performance may be attributed to the potential inadequacy of the model in capturing sufficient information.
Looking forward, if we want to make improvements to the project, we could add more data sources to better correct data imbalances, especially in the minority classes. Advanced text analysis tools like tokenization and word2vec could also be implemented. It is also possible to try machine learning algorithms such as LSTMs to improve the predictions about MBTI personalities. Additionally, to improve the sentiment analysis we could implement new word-embedding techniques, such as BERT, which helps capture subtle meanings between words.





