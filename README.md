# Text Analytics Group Project (MSBA 2020/21)

The project analysed the correlation between customers' reviews of Airbnb properties and prices/rating scores. The analysis process, including data preparation, sentiment analysis, and topic modelling, was done in R. The result shows there is a significant relationship between the reviews and the property prices. However, the correlation is trivial.

---

## Data collection and preparation

### Text preparation workflow

![圖片](https://user-images.githubusercontent.com/43996798/135534439-ea5349b6-04a2-4060-8488-9f0622837b8a.png)

The Airbnb dataset was first downloaded using R with the Web crawling technique. After that, We extracted customers' *reviews*, *amenities*, *neighbourhood_cleansed*, *host_is_superhost*, *property_type*, *room_type*, *bed_type*, *cancellation_policy*, *price*, and *review_scores_rating* from the downloaded documents. Then, only English text were kept. We also removed documents that is too short to be analysed. Besides, We extracted some features, such as readability, number of punctuations, and number of digits, from the documents. Finally, We used a Udpipe model to remove stopwords and tokenise the text into tokens.

---

## Sentiment Analysis

In this section, We calculated sentiment scores of the given documents and then trained a regression with all the sentiment scores and the property prices as well as the property rating scores to inspect their correlations. The correlations did exist significantly.

---

## Topic Modelling

In this part, We used unsupervised method "topic modelling" to find out the best number of topics among the documents. The optimal number of topics is 9. After that, we labelled each documents with a topic and developed another regression model to predict the stock prices with topics. Eventually, we discovered that only 4 extracted topics significantly affect the property rating scores. However, there are 8 extracted topics 
