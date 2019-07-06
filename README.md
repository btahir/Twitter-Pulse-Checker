# Twitter-Pulse-Checker

This is a quick and dirty way to get a sense of what's trending on Twitter related to a particular Topic. For my use case, I am focusing on the city of Seattle but you can easily apply this to any topic.

Use the GPU for this notebook to speed things up: select the menu option "Runtime" -> "Change runtime type", select "Hardware Accelerator" -> "GPU" and click "SAVE".

The code in this notebook does the following things:

Scrapes Tweets related to the Topic you are interested in.
Extracts relevant Tags from the text (NER: Named Entity Recognition).
Does Sentiment Analysis on those Tweets.
Provides some visualizations in an interactive format to get a 'pulse' of what's happening.
We use Tweepy to scrape Twitter data and Flair to do NER / Sentiment Analysis. We use Seaborn for visualizations and all of this is possible because of the wonderful, free and fast (with GPU) Google Colab.

A bit about NER (Named Entity Recognition)

This is the process of extracting labels form text.

So, take an example sentence: 'George Washington went to Washington'. NER will allow us to extract labels such as Person for 'George Washington' and Location for 'Washington (state)'. It is one of the most common and useful applications in NLP and, using it, we can extract labels from Tweets and do analysis on them.

A bit about Sentiment Analysis

Most commonly, this is the process of getting a sense of whether some text is Positive or Negative. More generally, you can apply it to any label of your choosing (Spam/No Spam etc.).

So, 'I hated this movie' would be classified as a negative statement but 'I loved this movie' would be classified as positive. Again - it is a very useful application as it allows us to get a sense of people's opinions about something (Twitter topics, Movie reviews etc).

To learn more about these applications, check out the Flair Github homepage and Tutorials: https://github.com/zalandoresearch/flair

Note: You will need Twitter API keys (and of course a Twitter account) to make this work. You can get those by signing up here: https://developer.twitter.com/en/apps

