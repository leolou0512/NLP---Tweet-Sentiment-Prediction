# NLP---Tweet-Sentiment-Prediction

This repository contains a sentiment analysis project that fine-tunes the BERT (bidirectional encoder representations from transformers) using c.a. 30,000 tweets. The goal of this project is to classify the sentiments of tweets into five categories: sadness, neutral, worry, love and happiness. 

## Example Showcase
Elon Musk, 17 May, 2023
```
Love to see Starlink providing great connectivity to those who had little or nothing before. 
As soon as you can access the Internet, you can learn almost anything, so it’s absolutely essential for education.
@khanacademy
 being a great example.
```
Sadness: -3.0802, neutral: -1.0553, worry: -0.8530,  love: 3.0702,  happiness: 1.5021

Sam Altman, 19 May, 2023
```
regulation should take effect above a capability threshold.
AGI safety is really important, and frontier models should be regulated.
regulatory capture is bad, and we shouldn't mess with models below the threshold. open source models and small startups are obviously important.
```
Sadness: -0.3042, neutral: 0.4411, worry: 4.5603,  love: -1.8420,  happiness: -2.2630

Donald Trump, 8 Jan 2021
```
I am asking for everyone at the U.S. Capitol to remain peaceful. No violence! Remember, WE are the Party of Law & Order – respect the Law and our great men and women in Blue. Thank you!
```
Sadness: -2.5776, neutral: 0.6452, worry: -0.1314,  love: 2.4554,  happiness: -0.3161


## Dataset and pre-processing
The original dataset was obtained from Kaggle (https://www.kaggle.com/datasets/pashupatigupta/emotion-detection-from-text?resource=download). The dataset contained 40,000 tweets which were manually sorted into 11 emotions. Since some of the 11 emotions only contained a small number of examples, these examples were discarded. The raw dataset can be found in tweet_emotions.csv file.

The following preprocessing steps were done: spell and slang correction, emoticons, replacing urls, reduce repetitions.


## Installation
Simply run all the cells in the tweet_analysis.ipynb, it should install all the related libraries and train the model.


## Acknowledgements
The BERT model implementation used in this project is based on the Hugging Face Transformers library.
