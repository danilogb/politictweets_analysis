# Tweet Analysis: Networks and Natural Language Processing

Social network analysis is the process of investigating social structures through the use of networks and graph theory. It characterizes networked structures as _nodes_ and _edges_- users and their tweets directed at others, in this case.
This technique, along with others such as NLP, can be leveraged to help understand communication and behavior in online contexts.

## Project Goal
Explore unstructured social media data - tweets - using social network analysis and natural language processing in order to uncover relationships between users and help identify important actors in the network, as well as gain insights about the topics being discussed and the overall sentiment surrounding them.

## Implementation

Using the [TweetGrab](https://github.com/danilogb/tweetgrab) module, two searches for tweets were performed: one using the keyword "Lula" and the second using the keyword "Bolsonaro". The data was downloaded and stored in a SQLite database. It was then read into a Pandas dataframe and preprocessed (clean text, format datetime, read json info, extract hashtags).

A relationship was defined as one person being mentioned in another's tweet. This is a very basic and simplistic model, but acceptable in the context of this work.
With this being said, the network analysis ensued, using the NetworkX module for Python.

To find sentiment embedded in the text, a classifier was trained on a dataset containing 300.000 tweets in Portuguese with binary sentiment labels (pos, neg).

![The "Bolsonaro" keyword network](/bolsonaro_network.png)
<center><span style="color:gray"><i>The "Bolsonaro" network. The red dot is the central node.</i></span></center>

\
![Some NLP results](/nlp_results.png)
<center><span style="color:gray"><i></i></span></center>

There are several other - more complex and often better - ways to model online conversations. This was supposed to be a simple study that could illustrate the potential of NLP and social network analysis.