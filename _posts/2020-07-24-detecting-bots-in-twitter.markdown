---
title: Detecting Bots in Twitter
date: 2020-07-24 10:49:00 Z
lead: UPM is working on a model to accurately predict whether a Twitter account is
  bot or not.
image: "/uploads/4518788990_5ace4f5637.jpg"
---

"Online bots are spreading disinformation on the coronavirus crisis across Europe", [the European Comissin alerts](https://ec.europa.eu/info/live-work-travel-eu/health/coronavirus-response/fighting-disinformation_en#dont-be-fooled-by-bots). "The massive increase of online disinformation and outright fake news concerning the coronavirus makes it very difficult to tell what is true and what is false. Some of the misleading information, massively spread via fake social media accounts including ‘bots’ that run automated tasks on the internet and social media, can potentially be very harmful to you and your loved ones".

Fandango's consortium partner Visual telecommunications applications research group ([GATV](http://www.gatv.ssr.upm.es/?lang=en)) at Universidad Politécnica de Madrid is currently working on a model to accurately predict whether a Twitter account is bot or not. In their own words:

*During the last years, the exponential growth of spreading misinformation throughout the social media platforms such as Twitter, Facebook or Instagram have fostered applied research in order to detect and consequently prevent the intrusion of these kind of content in such networks.  Thus, it is clear that Artificial Intelligence (AI) has a crucial role in this topic in order to support these platforms in order to automatically notify or restrict the access to those accounts that look suspicious according to a certain set of descriptors or features.*
  
*As an example of this, in 2019, Twitter had to remove more than 26 thousand of accounts since they were suspicious of spreading misinformation and/or non-appropriate content. So then, the question is, how AI may support end-users in the task of detecting suspicious accounts?*
  
To solve this first question, we need to first understand how a bot account and a normal account behaves and then try to find some descriptors that may distinguish both categories; this is what is call modelling in AI. Thus, the goal consists in creating a model or a function capable of properly separating these two classes using as input a collection of features. 
Focussing on Twitter, procedure of detecting bot accounts starts with a first glance or impression of some features (or combination of features) that are provided via the Twitter API or that can be computed using such data.*

*Figure X shows a comparative distribution diagram regarding the popularity metric, which is computed as a non-linear combination of the number of followers and friends that a given account has. As one may observe, both distributions contain different parameters in terms of mean (µ) and standard deviation (σ).* 

![Twitter_bots_1.png](/uploads/Twitter_bots_1.png)

*Figure X shows a boxplot of the same popularity metric. This representation is also useful to analyse the distribution of a given variable since it presents the different values of the quartiles and it is clear that these values are different for each distribution. Thus, this feature seems to be a priori useful to distinguish between bots and normal accounts.*

![Twitter_bots_2.png](/uploads/Twitter_bots_2.png)

*The second step consists in establishing a hypothesis due to at the end, this procedure is performed automatically by Machine or Deep learning approaches. The Null hypothesis here states that an input account is human or normal, whereas the alternative hypothesis will state the right opposite claim. However, to perform this hypothesis test process we need to have some feature or variable in order to carried out the verification of the Null hypothesis or its rejection according to a certain criteria.*

*Furthermore, this process is not enough since the amount of false positive and false negative may be considerable large since we are only analysing one feature. Thus, a second question arises, how can we select those features that better represent a distinction between these two classes? Once again, both Machine Learning and Deep Learning approaches are the key to solve this issue.*

*We need to pre-define a set of features to be considered from Twitter including the description of the user, the age of the account, the verification of the profile and the statistics related to the friends, followers, retweets etc. Subsequently, we need to pre-process these data since the ranges are completely different, the features have different nature (some of them are numerical other are Booleans or free text). At the end of this stage, we will have a potential feature map that can be feed into a ML or DL model in order to classify accounts as a binary problem (bot/human), where bot will be our positive class and human the negative one.* 

*Moreover, during the next training phase of our models, what it is actually happened is that the model is attempting to seek the best frontier or decision function to separate these classes according to the feature map that receives as input. The magical step once the model is trained is not only the fact that it can produce a probability of belonging a certain class but a new given account but it has created a more compact representation of the input features that seems to separate better these classes. This new representation is what it is called Embedding in the literature and which basically consists in a vector that has a more compact representation of the original feature map and it is generated as a result of the hidden layers of the model. The following Figure X shows an example of that after applying the so-called T-SNE projection algorithm to show the embedding as a 2-dimensional vector:*

![Twitter_bots_3.png](/uploads/Twitter_bots_3.png)

*Consequently, we have a good representation of Twitter accounts as a result of a combination of features that is provided by the trained model. Using this new representation, we can classify twitter accounts using the probabilities via the model itself, or we can just generate the embeddings of the account and search for similar previous annotated accounts in our large database to make the final decision. This process can be performed via efficient Information Retrieval algorithms such as approximations of the Nearest Neighbours algorithms such as Local Sensing Hashing.*

