---
title: Technical approach
date: 2018-02-28 12:40:00 Z
permalink: "/the-project/technical-approach/"
navigation_order: 1
navigation_parent: The Project
---

FANDANGO will integrate and analyse big data silos for fake news detection assisting journalists, as well as people, to foster credibility in information and avoid mainpulation and social engineering practises through fake news. FANDANGO will build and provide an open software stack that will include a wide range of tools for fake news checking and verification from text content to images and videos and in structured and unstructured formats. Aiming to focus its efforts on the integration of the data and the value generation from cross-domain data setups FANDANGO will be build around and ontop of existing software solutions.

The platform is build around a well defined **Data Lake** architecture that incorporates all available data types found in the already identified data sources, i.e. free text, structured and unstructured data, images, videos and audio data from web sources, knowledge databases or corporate databases and knowledge.

![](/uploads/data-lake.png)

**Data shippers components** push raw data to the distributed **FANDANGO Data Lake** through **data preprocessing** and **data homogenisation** tools that follow well defined **data models** and the **data representation conventions** for the FANDANGO Data Lake. FANDANGO will put effort on defining and selecting well established data conventions and data model schemes and not just follow a “throw-everything-in-data-lake” process, which [typically fails to deliver what promised](http://usblogs.pwc.com/emerging-technology/data-lakes-and-the-promise-of-unsiloed-data/). The FANDANGO Data Lake will also incorporate ground truth data in order to initialise machine learning models. These learnable models will be further updated with respect to their learning acquisition as data are coming in on an online, iterative learning scheme.

The collected data are processed and analysed from a set of tools and services that aim to extract markers and cues in order to reveal fake or misleading news data chunks. Due to the variety of the collected raw data that need to be analysed with respect to fakeness, different analysis modules are filling the toolset of the FANDANGO software stack. Thus, the **advanced analytics services** of FANDANGO consist of the following:

- The **source credibility scores and profiles** module is responsible to score the data sources based on the history and the quality of the content that is propagated by each source. For instance, a web portal that is publishing news posts will be automatically scored for its credibility.

- The **misleading messages detection** module uses natural language processing (NLP) approaches and correlation of facts from knowledge bases to identify misleading parts of text and possible intent on passing fake or incomplete news.

- The **fake news identifiers** module builds indicator functions able to identify features that can act as cues for fakeness of a news post based on a machine learnable feature selection approach.

- The **multilingual text analytics** module translates news posts to a common vocabulary as a reference language and combine global sources of information for further analysis.

- The **Copy-move detection tools** applies image and video analysis techniques in order to identify malicious manipulation or forgery of the original image or video content. This information will act as a strong cue regarding the fakeness scoring of a multimedia related news.

- The **Social graph analysis** module provides algorithms for analysing social graph data for fake news diffusion detection. To do so, extraction of key graph nodes that play a dominant role in a graph will be evaluated and scored accordingly.

- The **spatio-temporal analytics** module enables direct verification of the validity of the news post in the context of spatial and temporal consistency with respect as well to previous relevant posts. This will provide the means to seek for reposting news in irrelevant temporal context.

- The **machine learnable scoring for fake news decision making** is the module that fuse the weighting of all collected cues so that a score function may be learned that permits the efficient decision making for the end users of FANDANGO.

- Finally, for the **visualisation of the discovery and analysis of fake news**, FANDANGO provides a set of front end web applications and data analytics visualisation with focus on the identified case studies. However, these tools are suitable for any kind of fake news discovery application. FANDANGO is a loosely integrated platform (i.e. a toolbox) constituted by well defined modules with clear functionalities and APIs interfaces that fully support the individual use of each single module or a set of them and a strait forward embedding of FANDANGO components into existing platforms and dashboards. Following, for instance the news agencies editorial desks needs to work in a transparent way in their well estabilished working established (e.g, news rooms and/or marketing and targeted advertising platforms)

The FANDANGO approach on deploying all these modules and services is to follow existing well established and widely used technologies such as the [Docker containers](https://www.docker.com/what-docker). The “dockerisation” of modules will permit the easy deployment in any cloud infrastructure with minimal effort while “hiding” any library or software dependencies to avoid conflicts in software deployment. An important point in favour of this approach is the elastic deployment of more nodes of one module, when this is needed, to handle for example a spike of incoming data. The container based approach permits also the independent development or deployment of components in any programming language as soon as they follow the interfacing requirements that will be defined. During the implementation time, FANDANGO will re-investigate various open source container management and orchestration frameworks such as the [Kubernetes](https://kubernetes.io/) and [Rancher](http://rancher.com/rancher-os/) for the efficient deployment using the most stable solution.

The FANDANGO Platform will benefit of some advanced interactive visualisation functionalities based on Dromic visual components, made available by Sindice Partner. Smart visualization is a key aspect for a successful Big data analystic application; for instance, the hierarchy data coming from data lakes, can be accessed in graphical form, which gives further hints on how FANDANGO data will be organized, helping dramatically in reaveling hidden connections among heterogenous data while digging for veracity.