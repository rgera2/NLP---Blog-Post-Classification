# NLP---Blog-Post-Classification
# INTRODUCTION
Given the popularity of blogs, it would be useful if we could devise a content classification system to automatically suggest the blogs to the right audience in terms of age group. However, it is difficult to group text into categories because of freestyle natural language. Bloggers at different levels write whatever is appealing to their mind, thus inventing sometimes new vocabulary and grammar. Nevertheless, some bloggers intentionally deviate from rules of language and decorum to create a spectacle for the sake of attracting a larger audience.
In this project, we designed text classification models to categorize blogs into three user groups: ‘teenage’, ‘adults’ and ‘mature’. We used pure statistical learning methods to classify blogs conditioned on various feature vectorization techniques such as TF-IDF, count vectorizer and embeddings (Doc2vec and GloVe).Furthermore, we compared various machine learning and feature vectorization techniques to improve the content shown to users against randomly selected ones.

# Dataset
The dataset is acquired through "Kaggle.com – Blog Posts Labeled with Age and Gender". Since the labeled dataset contains 3 discrete age groups (less than 17, 23 – 27, 33 and above), this is a supervised multiclass classification problem.
Attributes - post, age, gender
25000 blogs taken

# Data Preprocessing
1. Converted the numeric age into discrete categories (Mature, Minor, Adult)
2. Used feature vactorization with Naive Bayesian (Bernoulli) model to capture baseline accuracy of 55%.
2. Removed punctuations, numbers, words whose length is <3 and >15, make them lower case but retained the stop words (as it was not making any difference and was computationally expensive).
3. Feature Vectorization - Tokenizing, Counting and Normalizing
4. Word embeddings used - GloVe and Doc2Vec

# Models used
Naive Bayes, SVM, Random Forest, Logistic Regression

# Evaluation Metrics 
Compared the models based on Test Accuracy with baseline model w.r.t. number of examples.

# Conclusion
1. Demonstrated feature selection and impacts
2. Multinomial Naive Bayes outperformed
3. Performance affected by quantity and quality of data
4. With less amount of data, tf-idf performed better than some popular word embeddings like GloVe and Doc2Vec
