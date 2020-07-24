---
title: Detecting Bots in Twitter
date: 2020-07-24 10:49:00 Z
published: false
---

"Online bots are spreading disinformation on the coronavirus crisis across Europe", [the European Comissin alerts](https://ec.europa.eu/info/live-work-travel-eu/health/coronavirus-response/fighting-disinformation_en#dont-be-fooled-by-bots). "The massive increase of online disinformation and outright fake news concerning the coronavirus makes it very difficult to tell what is true and what is false. Some of the misleading information, massively spread via fake social media accounts including ‘bots’ that run automated tasks on the internet and social media, can potentially be very harmful to you and your loved ones".

Fandango's consortium partner Visual telecommunications applications research group ([GATV](http://www.gatv.ssr.upm.es/?lang=en)) at Universidad Politécnica de Madrid is currently working on a model to accurately predict whether a Twitter account is bot or not. In their own words:

*During the last years, the exponential growth of spreading misinformation throughout the social media platforms such as Twitter, Facebook or Instagram have fostered applied research in order to detect and consequently prevent the intrusion of these kind of content in such networks.  Thus, it is clear that Artificial Intelligence (AI) has a crucial role in this topic in order to support these platforms in order to automatically notify or restrict the access to those accounts that look suspicious according to a certain set of descriptors or features.*
  
*As an example of this, in 2019, Twitter had to remove more than 26 thousand of accounts since they were suspicious of spreading misinformation and/or non-appropriate content. So then, the question is, how AI may support end-users in the task of detecting suspicious accounts?*
  
To solve this first question, we need to first understand how a bot account and a normal account behaves and then try to find some descriptors that may distinguish both categories; this is what is call modelling in AI. Thus, the goal consists in creating a model or a function capable of properly separating these two classes using as input a collection of features. 
Focussing on Twitter, procedure of detecting bot accounts starts with a first glance or impression of some features (or combination of features) that are provided via the Twitter API or that can be computed using such data.
Figure X shows a comparative distribution diagram regarding the popularity metric, which is computed as a non-linear combination of the number of followers and friends that a given account has. As one may observe, both distributions contain different parameters in terms of mean (µ) and standard deviation (σ) 

