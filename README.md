# Apple Sentiment Twitter Analysis
### Team Members:
- Sean Harris, Technical Lead
- Stuart Clark, GitHub Lead
- Rajesh (Raj) Reddy, Presentation Lead

  
## Business Situation
We have been tasked with analyzing Twitter 2011 data from SXSW and creating a model of positive and negative tweets. We want to figure out how consumers feel about their products. The data set has been provided to us and already has some classification applied to the tweets such as brand and sentiment.

## Explore the data.
- Develop a model on positive and negative consumer sentiment.
- Provide recommendations to Apple’s Marketing and Product Design teams.

## Data Overview
We used a dataset from data.world provided by CrowdFlower which contains 9,093 tweets about Apple and Google from the South by Southwest (SXSW) Conference. The tweet labels were crowdsourced and reflect which emotion they convey and what product/service/company this emotion is directed at based on the content.

### Filtering
- The data is filtered to only include Apple products based on the newly calculated field called 'new_brand'.
- Dropped 1 tweet that had null value.
- Filtered out neutral to focus on positive and negative sentiment for this first model.

### Data Limitations
- Data only from 2011
- Imbalanced data
- Target column not always accurate

## Data Analysis 
![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/67396ce3-0038-4025-a901-81cc6a081ec8)

We started by assigning a brand to each tweet depending on what product was being talked about. 
As you can see the majority of users were talking about Apple products and we had plenty of tweets to work from. Using this we filtered down the tweets only discussing apple. We then decided to look at the most common words in these tweets. 

- From this chart. We found that **store**,  **app**, and **new** were the most three common words used. However, this didn't really tell us how people were feeling.

![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/6ae56362-ea02-4316-b918-c0864a2ab513)

We then created word clouds to see the positive and negative on apple products

![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/a3106e1d-1ca7-4e36-a419-7c54036691c7)
![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/f34e6c26-6c46-4567-bfcc-c71c3e08bd60)


![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/861e5a37-5ffe-4611-8efc-091fcab24aed)
![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/9cc63675-7c1e-496a-84fe-67b32b86a6ec)


## Modeling
- The models we ran were Logistic Regression, Naive-Bayes, Gradient Boost, Random Forest, Decision Tree, and Stochastic Gradient Descent.
- We decided on Stochasic Gradient Descent as our final model which gave us an F1-Score of 80%
- We chose the f1 score as our metric because of the  imbalanced data we f1 balances out both precision and recall to give us one score
- Our SGD model showed a strong performance in recognizing positive tweets while minimizing false positives and false negatives.

![image](https://github.com/sclarkHOU/Phase_4_Project/assets/56837718/9a109b7e-91b2-4d22-82f4-11bb103091db)


## Conclusion
We were able to get an F1 score of 80% by using stochastic gradient descent (SGD) and if we continue to develop this model and the underlying data we can improve this score further. Based on the word clouds we suggest that Apple's product development team and marketing team focus on app functionality, improving battery life and ensure design is appealing to customers. We can use this model to test small changes to apps by utilizing new twitter data.

## Next Steps 
- Acquire recent data from Twitter.
- Look into alternate ways of dealing with the imbalanced data.
- Use deep learning models to capture complex patterns in the data.
- Hand review target/sentiment to imporve sentiment classification.

  
## For More Information
 If you have any questions, please contact our team:

 [Rajesh Reddy](https://github.com/rredd002)

 [Stuart Clark](https://github.com/sclarkHOU)

 [Sean Harris](https://github.com/smharris312)

### Repository Structure

├── Data

├── Twitter Sentiment Analysis .pdf

├── Analysis of Apple Sentiment on Twitter.ipynb

├── Analysis of Apple Sentiment on Twitter.pdf

├── README.md

├── gitignore.txt

































