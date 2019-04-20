---
title: Automating fake news detection and fact-checking
date: 2018-02-28 12:40:00 Z
permalink: "/achievements/automation/"
navigation_order: 0
navigation_parent: Achievements
---

As part of the user requirement gathering phase, we have spent time exploring existing initiatives, tools and techniques, with a particular focus on those close to being deployed in the market. Understanding the state of the art in terms of machine learning and Big Data applied to the issue of misinformation is crucial to ensure that the user requirements leading FANDANGO development are feasible and will produce reliable results.

### Fake news and bias detection

Fake news detection is defined as the prediction of the chances of a particular news article (news report, editorial, expose, etc.) being intentionally deceptive. Establishing the reliability of information online is a daunting but critical challenge, often even for humans. In order to automate this process, two main methods have emerged:

- **Linguistic Approaches** in which the content of deceptive messages is extracted and analysed to associate language patterns with deception.

- **Network Approaches** in which network information, such as message metadata or structured knowledge network queries can be harnessed to provide aggregate deception measures.

Both forms typically incorporate machine-learning techniques for training classifiers to suit the analysis, and they work at the article level, without trying to understand and verify each particular sentence. FANDANGO’s Work Package 4 does explicitly include these techniques, among others. For an initial review of these methods, see N. Conroy et al. “[Automatic Deception Detection: Methods for Finding Fake News](https://onlinelibrary.wiley.com/doi/pdf/10.1002/pra2.2015.145052010082)”.

As an example of a linguistic approach, Horne and Adali, in their 2017 study "[This Just In: Fake News Packs a Lot in Title, Uses Simpler, Repetitive Content in Text Body, More Similar to Satire than Real News](https://arxiv.org/pdf/1703.09398.pdf)", analysed three small datasets ranging from a couple of hundred to a few thousand articles from a couple of dozen sources, comparing real news vs. fake news vs. satire, and found that the latter two have a lot in common across a number of dimensions. They found that fake news pack a lot of information in the title (as the focus is on users who do not read beyond the title), and use shorter, simpler, and repetitive content in the body (as writing fake information takes a lot of effort). Thus, they argued that the title and the body should be analysed separately. In their follow-up work, "[Sampling the News Producers: A Large News and Feature Data Set for the Study of the Complex Media Landscape](https://arxiv.org/pdf/1803.10124.pdf)", they created a large-scale dataset covering 136000 articles from 92 sources from opensources.com, which they characterized, based on 130 features from seven categories: structural, sentiment, engagement, topic-dependent, complexity, bias, and morality.

Similarly, R. Baly et al., “[Predicting Factuality of Reporting and Bias of News Media Sources](https://admin.govexec.com/media/emnlp-2018-predicting.pdf)”, follows this line. According to the authors, their study reveals key features of false news web sites that might be less visible to human fact checkers but can tab a bad news source. Among the features, they mention specific patterns of so-called “function words” that give a more spoken feel to a news article, as opposed to the far more common “content words.” "Mainstream news editors clamp down fast and hard on too many function words, but fake news sites may not be edited at all", they say.

Some of these methods were tested during the [Fake News Challenge](http://www.fakenewschallenge.org), a competition to foster development of tools to help human fact checkers using machine learning and natural language processing. But we didn’t find them deployed or under development in actual newsrooms, which may suggest a potential opportunity for FANDANGO.

### Automated fact-checking

By "automated fact-checking" (AFC), we mean the development of automated tools and technologies to assist journalists in vetting and verifying factual statements. Note that, unlike the techniques described in the previous section to detect fake news, **automated fact-checking works at the level of a particular statement or claim**.

According to Lucas Graves, senior research fellow at Reuters Institute and author of “[Understanding the Promise and Limits of Automated Fact-Checking](https://reutersinstitute.politics.ox.ac.uk/our-research/understanding-promise-and-limits-automated-fact-checking)”, automated fact-checking initiatives and research generally focus on one or more of three overlapping objectives:

> to spot false or questionable claims circulating online and in other media; to authoritatively verify claims or stories that are in doubt, or to facilitate their verification by journalists and members of the public; and to deliver corrections instantaneously, across different media, to audiences exposed to misinformation. End-to-end systems aim to address all three elements – identification, verification, and correction.

In 2015, Hassan et al., in “[The Quest to Automate Fact-Checking](https://www.researchgate.net/publication/301801279_The_Quest_to_Automate_Fact-Checking)”, define the “Holy Grail” of automated fact-checking as a computer-based system that is:

- **Fully automated**: It checks facts without human intervention. It takes as input the video/audio signals and texts of a political discourse and returns factual claims and a truthiness rating for each claim.

- **Instant**: It immediately reaches conclusions and returns results after claims are made, without noticeable delays.

- **Accurate**: It is equally or more accurate than any human fact-checker.

- **Accountable**: It self-documents its data sources and analysis, and makes the process of each fact- check transparent. This process can then be independently verified, critiqued, improved, and even extended to other situations.

As this report states,

> such a system mandates many complex steps–extracting natural language sentences from textual/audio sources; separating factual claims from opinions, beliefs, hyperboles, questions, and so on; detecting topics of factual claims and discerning which are the “check-worthy” claims; assessing the veracity of such claims, which itself requires collecting information and data, analysing claims, matching claims with evidence, and presenting conclusions and explanations.

In 2015, the most important computational hurdles to solve, according to this paper, were:

- **Finding claims to check**, including – potentially - going from raw audio/video signals to natural language, and extracting contextual information such as speaker, time, and occasion. Once a transcript is available, claims need to be extracted from the text, which depends on determining whether a claim is “checkable” and “check-worthy”.

- **Getting data to check claims**, where data refers both to 1) claims already checked by various organizations; 2) unstructured, semi-structured and structured data sources that provide raw data useful for checking claims, e.g., voting records, government budgets or crime records. For a given claim, relevant datasets (or even particular data items) need to be matched, and their quality, completeness, applicability and freshness evaluated, so the most valuable ones are surfaced.

- **Checking claims**, where challenges are how to remove (sometimes intentional) vagueness, how to spot cherry-picking of data (beyond correctness) or how to evaluate and how to come up with convincing counterarguments using data.

- **Monitoring and anticipating claims**. Given evolving data, we can monitor when a claim turns false/true. Can we anticipate what claims may be made soon? That way, we can plan ahead and be proactive.

In 2017, the authors updated their paper in “[Progress Toward “the Holy Grail”: The Continued Quest to Automate Fact-Checking](http://ranger.uta.edu/~cli/pubs/2017/factchecking-cj17-adair.pdf)” with an optimistic statement:

> the Holy Grail is no longer a distant dream [...] recent advances with the creation of a global database of structured fact-checks and fact-checking tools such as ClaimBuster and iCheck have laid a groundwork for additional advances in the next few years.

However, our evaluation of the field shows that a fully-automated system is beyond the current state of the art, and systems under development in the industry still rely on humans at critical points of the process.

Graves’ 2018 report for Reuters Institute gave the most comprehensive assessment to date about automated fact-checking initiatives and research. Depending on their purpose/focus, the report classifies current initiatives in two categories, "identifying claims" and "verifying claims".

### The current state of automated fact-checking

Because of its relevance, we reproduce Graves' report conclusions:

> The potential for automated responses to online misinformation that work at scale and don’t require human supervision remains sharply limited today. Researchers are exploring both more and less structured approaches to automated verification, reflecting wider divisions in the AI landscape. Despite progress, AFC techniques which emulate humans in comprehending the elements of a claim and checking them against authoritative references are constrained by both the current science and by a lack of data; researchers suggest one path forward is to build up recognition of different kinds of claims in a gradual and ad hoc way. Another family of techniques assesses the quality of information based on a complex array of network signals, making judgements about a message or its source in ways that may be opaque to humans. It is unclear how effective various unstructured approaches will prove in responding to different kinds of misinformation, for instance, false claims from political elites as opposed to viral online rumours. These approaches may also be vulnerable to mistakes from reputable sources, and raise difficult questions about protecting open and diverse political expression online.
