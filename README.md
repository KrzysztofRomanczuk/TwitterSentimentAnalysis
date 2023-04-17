# TwitterSentimentAnalysis
Twitter Sentiment Analysis using Transformers and Tweepy
This Python code imports the required libraries tweepy, transformers, and scipy.special to perform sentiment analysis on tweets related to "Biden". It first authenticates with Twitter API using the consumer_key, consumer_secret, access_token, and access_token_secret.

It then searches for 500 popular tweets related to "Biden" using the tweepy.Cursor function, and creates a list of the full text of each tweet. The time.sleep(1) function is used to avoid exceeding the Twitter API rate limits.

Next, the sentiment analysis model is defined using the cardiffnlp/twitter-roberta-base-sentiment pre-trained model from Hugging Face's Transformers library. The AutoModelForSequenceClassification.from_pretrained function loads the pre-trained model, while the AutoTokenizer.from_pretrained function loads the tokenizer.

The for loop then processes each tweet in the list by replacing Twitter handles with "@user" and URLs with "http". It then encodes the preprocessed tweet using the tokenizer, and passes it through the sentiment analysis model. The softmax function is used to convert the model's output scores into probabilities for each sentiment label.

Finally, the sentiment analysis results for each tweet are printed, with the tweet's full text followed by the probability scores for each sentiment label: "Negative", "Neutral", and "Positive".

Note: You will need to substitute your own Twitter API keys and tokens for the consumer_key, consumer_secret, access_token, and access_token_secret variables to run this code.
