# News-Recommender
NewsRecommender
A news recommender system that recommends news articles to users based on their interests. I have used facebook's pre trained model of word2vec.



APPROACH :

A corpus containing news articles as documents.


  DATA CLEANING:
  
•	First task is data cleaning, which includes nlp tasks as removal of stop words, stemming, lemmatization etc. •	Second task includes named entity recognition as our articles contain lot of Indian names, places and numerical data as well. So we have to replace it with suitable words so that our model recognizes them. ( Removed them )


  TOPIC MODELLING:
  
•	After doing data cleaning we have to convert all the documents into vectors. For this we will use doc2vec approach. •	We will first calculate word2vec for every word in the document and tfidf scores for every document. Multiplying them we can obtain doc2vec i.e. vector for every document.


  USER PROFILER:
  
•	User profiler will be the bot that will explore a given user and fetch their interests on the basis of the articles (s)he reads and time and session spent on it. •	We will initially generate data by ourselves using Gaussian mixture model. User will be given randomly 10 articles from different clusters.


  RECOMMENDER BOT:
  
•	This bot will get input from USER PROFILER BOT about user interests and according to the article user likes, it will recommend similar articles. •	We can use cosine similarity between the ‘articles user likes’ and ‘the ones we have in our corpus’, and most similar ones will be recommended.(based on past history,similar users(collaborative filtering) and general trends)
