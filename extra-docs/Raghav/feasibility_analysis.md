<H1 align="center">Feasibility Analysis Report</H1>
<H2 align="center">For Project Recommend</H2>
<h5> Prepared by<br/>
Raghav Mittal<br/>
U101114FCS111</h5>
<br/>

## Scope of Document
This document covers the economic and technical feasibility of "Project Recommend".
This report covers the following
- Analysis of problem (Why do we need this software?)
- Limitations and constraints
- Economical feasibility of product
- Public survey to validate our assumptions


## Analysis of problem (Why do we need this software?)
Nearly every internet user listen to music. Due to advancements in technology there is a huge increase in music production. This has led to too much tracks available online which often leads to lot of confusion and choice dilemma. There are many softwares and apps which help user in listening to songs of their likeness by providing suggestions and recommending songs. But all such available apps work online i.e. they require internet. User behaviour is recorded and on the bases of this, these apps suggest similar songs to one user is listening to.

Following are the things we will do- to overcome those problems.
We are trying to provide recommendations on your offline music collection.
Music that you bought as a CD or from any other online music store, means we are not limited to an particular service.
We use content based filtering that doesn't require any user data for its working.
We only fetch metadata so that the software works with the low bandwidth internet connection.


## Limitations and Constraints

For recommendation of music we are using metadata available in individual tracks which is an Implementation of [_**content based filtering**_][content_based_filtering_wikipedia].  

We could have implemented [_collaborative filtering_][collaborative_filtering_wikipedia] for generating suggestions which is more accurate then metadata approach but because we are not storing user data we cannot implement that.  

In [_content based filtering_][content_based_filtering_wikipedia], songs are grouped into different views on bases of their metadata(properties like genre, singer, mood etc) which is already available. Unlike _collaborative analysis_, user behaviour is not analyzed here and this may lead to less accurate results. Also this method needs a standard metadata schema over all the tracks that is the reason we are using [_MusicBrainz database_][musicbrainz-database-website] here.  

The other way is [_waveform analysis_](http://www.academia.edu/4631247/Waveform-Based_Musical_Genre_Classification). In this method sound tracks are analysed and grouped into different genres according to their waveform but it was found that this method is inaccurate. This technique is under research and development and is not proven successful.

Because we don't want to make it internet light software, we cannot use above methods.

## Economic Feasibility
This project is an open-source, we do not have any business goals, we do not have any intentions of making profit. The software will be available to everyone for free, anyone can use our work under mentioned license and improve on it. We also accept patches from anyone via GitHub and will merge them after reviewing. In this way, anyone can contribute to the development of this software.


## Conclusions From Our Survey

**We surveyed a group of 110 computer science undergrad students because undergrad often listen to music and are tech-savvy. Given below is a list of questions we asked in our survey, and their corresponding responses, represented in the form of pie-charts.**


#### 1.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q1.PNG" alt = "Question 1 and its response!" height = auto width = "400px" ></center>


#### Inference:
This pie-chart shows that most of the people prefer to listen to music almost all the time(app. 60% in our case).

#### 2.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q2.png" alt = "Question 2 and its response!" height = auto width = "400px"></center>

#### Inference:

This pie-chart shows that generally, people at least use a small proportion of their storage memory, for
storing music offline(over 32% people have music collection between 10-50 GBs and app. 39% people have collection <10 GBs, that is, the latter have got at least some music offline).


#### 3.

<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q3.png" alt = "Question 3 and its response!" height = auto width = "400px" ></center>

#### Inference:

Nearly half of the people (approx. 45%), whom we surveyed, download music all the time. This result goes hand in
hand with our idea in a sense that, if upon recommendation their collection does not have a particular
song, they can download it, at that very instant. A larger part of remaining half(46%), do not download
music that very often, but still once in a while, they can download.


#### 4.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q4.png" alt = "Question 4 and its response!" height = auto width = "400px" ></center>

#### Inference:

This pie-chart shows that a majority of people we surveyed(approx. 81%) prefer to discover music based on
their taste(which will be performed by a classifier in our case).


#### 5.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q5.png" alt = "Question 5 and its response!" height = auto width = "400px"></center>

#### Inference:


This pie-chart shows that almost half of the people(49% app.), find it difficult to search the songs
similar to the one they have in their offline music library. This suggests that they would like to get
recommendations based on their music taste, automatically, and then accordingly download that particular
kind of music.


#### 6.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q6.png" alt = "Question 6 and its response!" height = auto width = "400px" ></center>

#### Inference:

This pie-chart shows that almost half of the people do not have a fully updated metadata(approx. 50%),
which made us to attach an extra component to our software, known as the Metadata Updater.


#### 7.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q7.png" alt = "Question 7 and its response!" height = auto width = "400px" ></center>

#### Inference:


Finally, here we ask people, if they want to use such a music player that recommends similar songs from
and outside of their offline music library. Seeing the number of people(76%) who want this to happen,
we concluded that our product is feasible for a majority.

[collaborative_filtering_wikipedia]: https://en.wikipedia.org/wiki/Collaborative_filtering
[content_based_filtering_wikipedia]:https://en.wikipedia.org/wiki/Recommender_system#Content-based_filtering
