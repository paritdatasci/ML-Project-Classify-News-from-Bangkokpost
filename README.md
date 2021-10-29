# Machine Learning for Classifying-News-from-Bangkokpost
This project is to develope machine learning model to classify news category from Bangkokpost.com. News are seperated into three types which are Business News, Politics News and General News which would be used as label/target.

These are the steps that I took: 

1. I started collecting approximately 3,000 news from Bangkokpost.com through scraping process and put them to dataframe. There are 4 things that I collected. These are news title, news content, time release, and news category. Then save it to csv file.

2. After that I started to do feature extraction on both TF-IDF and CountVectorizer so that I can use them as a feature for training machine learning model. 

3. During the process of selecting machine learning model, I used cross validation score as a measure for deciding which model is the best. It appeared that Multinomial Naive Bayes provides the highest cross validation score, approximately 90%. The second best model is support vector machine - SVC(kernel='linear'), around 87-89%. Therefore, MultinomialNB was chosen.
 
4. After training MultinomialNB model in the first round by setting hyperparameter at default, it gave accuracy score around 0.942 running 500 times(please look at the histogram in Notebook). The model did best on general news prediction with F1- Score around 0.96.

5. After tuning the model by setting new hyperparameter as followed (estimator=MultinomialNB(alpha=1.0, class_prior=None,fit_prior=True)), it turned out that the model had slightly better performance. It provided accuracy score around 0.951 running 500 times. Moreover, other indicators such precision score, recall and F1-score also improved 


