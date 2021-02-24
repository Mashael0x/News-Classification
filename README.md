# News-Classification

this dataset is called **20 news groups** it's a collection of 18000 documents on 20 topics.
I selected a subset of this dataset and choose these topics:
  - cryptography news
  - medical news
  - computer hardware-IBM news
  - computer hardware-Mac news
  - computer graphics news
  - sports-hockey news
  - sports-baseball news

**Some info about the dataset:**

you can fetch this dataset from `sklearn.datasets`. the dataset contains 3 columns which is text, target and title.
it doesn't have any null values.

## Exploratory Data Analysis
 let's start by looking at the distribtion of news text length.
 as we can see most of news are only contains 400 words or less.
 
 ![image](https://github.com/Mashael0x/News-Classification/blob/main/text%20distribtuion%20(5).png)

 I wanted to know what are the most common words in each topic of news by using `Counter` from `collections` package it was weasy to extract most common words.
 
 this plot shows most common words in Computer Graphics news.
 
 ![image](https://github.com/Mashael0x/News-Classification/blob/main/word%20frequency_Graphics_News.png)
 
 most common words in Crytpography news.
 
 ![image](https://github.com/Mashael0x/News-Classification/blob/main/word%20frequency_Cryptography_News.png)
 
 most common words in Baseball news
 
 ![image](https://github.com/Mashael0x/News-Classification/blob/main/word%20frequency_Baseball_News.png)
 
 you can see more plots on most common words for each topic in my Google Colab notebook.

## Text Cleaning

I used `nltk` to do text cleaning and prepare my data for the next step. 
the steps to clean my text are as follow:

     1. tokenize text
     2. lower the words
     3. remove punctuations
     4. remove non-alphabetic characters
     5. stem words using
     6. join words so it doesn't save as a list which will created problems later when transforming text and modeling it.
  ![image](https://github.com/Mashael0x/News-Classification/blob/main/text_clean_function.png)
     

## Modeling 
  I used CountVectorizer, tfidTransformer and Multinomial Naive Bayes in a pipeline and performed a grid scearch to explore best hyperparameters for my model.
  before choosing these 3 instances I experimented with many models such as SVM, linear SVM, SGDclassifier and knn without using grid search. they all have less accuracy score     than Multinmoial Naive Bayes, there was a choice to perform grid search on SGDclassifier and get a higher result but unfortanutly it will take many hours on my device
  to choose the best parameter so I stick to Multinomial Naive Bayes.

classification report:

![image](https://github.com/Mashael0x/News-Classification/blob/main/classification_report.png)
