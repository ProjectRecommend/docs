# Project Recommend

## Feasibility Study report




## Scope of Document

This document covers the economic and technical feasibility of "Project Recommend"

This report covers the following

- Analysis of problem (Why do we need this software?)
- Limitations and constraints
- Economical feasibility of product
- Public survey to validate our assumptions


## Analysis of problem (Why do we need this software?)

Music recommendation is a fairly normal thing nowadays, we see it all over the places like YouTube, SoundCloud
and all the other music provider services.
Then why do we need this software?
Here are few limitations of all those online Music recommendation that we are trying to overcome
- Recommendations as based on collaborative filtering which means you have to use that service quite often for it's recommendation service to give reliable results.
- Everything is limited to that service, means you get recommendations only on what they offer to the users.
- Most of their services are paid/subscription based.
- They require high internet bandwidth to stream music.

Following are the things we will do- to overcome those problems.
We are trying to provide recommendations on your offline music collection.
Music that you bought as a CD or from any other online music store, means we are not limited to an particular service.
We use content based filtering that doesn't require any user data for its working.
We only fetch metadata so that the software works with the low bandwidth internet connection.


## Limitations and Constraints


- Waveform Analysis  
This is one of the methods we could have used to classify music. In this method, we analyze and classify
the music wave into genres such as pop, jazz etc., but there is not enough training data available to
analyze the waveform. Also there is not enough research done in this field. Hence, this method could not
be used in practical (For instance, Spotify tried it and got worst results as compared to other techniques ).


- Collaborative Filtering  
Here, in this method, we use user data to recommend next set of songs to the user. But, due to lack of
time and resources we do not have enough user data to make this method feasible to use. If we did have
the user data, that data would have been used by the training model to recommend new songs based on that data.


- Availability of other basic requirements  
Internet is one of the basic requirements for our software to work, Lack of internet means
that our software will work like a plain music player. in lack of internet connection we can't provide recommendation but already cached recommendations will available to user with internet connection


## Economic Feasibility
This project is an open-source, we do not have any business goals, we do not have any intentions of making profit. The software will be available to everyone for free, anyone can use our work under mentioned license and improve on it. We also accept patches from anyone via GitHub and will merge them after reviewing. In this way, anyone can contribute to the development of this software.


## Conclusions From Our Survey

##### We surveyed 110 odd people, belonging to different sectors such as corporate, business etc. and belonging to different age groups. Given below is a list of questions we asked in our survey, and their corresponding responses, represented in the form of pie-charts.   


#### 1.

![Question 1](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q1.png)


#### Inference:
This pie-chart shows that most of the people prefer to listen to music almost all the time(app. 60% in our case).

#### 2.

![Question 2](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q2.png)

#### Inference:

This pie-chart shows that generally, people at least use a small proportion of their storage memory, for
storing music offline(over 32% people have music collection between 10-50 GBs and app. 39% people have collection <10 GBs, that is, the latter have got at least some music offline).


#### 3.

![Question 3](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q3.png)

#### Inference:

Nearly half of the people (approx. 45%), whom we surveyed, download music all the time. This result goes hand in
hand with our idea in a sense that, if upon recommendation their collection does not have a particular
song, they can download it, at that very instant. A larger part of remaining half(46%), do not download
music that very often, but still once in a while, they can download.


#### 4.

![Question 4](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q4.png)

#### Inference:

This pie-chart shows that a majority of people we surveyed(approx. 81%) prefer to discover music based on
their taste(which will be performed by a classifier in our case).


#### 5.

![Question 5](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q5.png)

#### Inference:

This pie-chart shows that almost half of the people(49% app.), find it difficult to search the songs
similar to the one they have in their offline music library. This suggests that they would like to get
recommendations based on their music taste, automatically, and then accordingly download that particular
kind of music.


#### 6.

![Question 6](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q6.png)

#### Inference:

This pie-chart shows that almost half of the people do not have a fully updated metadata(approx. 50%),
which made us to attach an extra component to our software, known as the Metadata Updater.


#### 7.

![Question 7](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/images/q7.png)

#### Inference:


Finally, here we ask people, if they want to use such a music player that recommends similar songs from
and outside of their offline music library. Seeing the number of people(76%) who want this to happen,
we concluded that our product is feasible for a majority.
