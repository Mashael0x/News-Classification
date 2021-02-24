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

### Exploratory Data Analysis
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

### Text Cleaning



### Modeling 


