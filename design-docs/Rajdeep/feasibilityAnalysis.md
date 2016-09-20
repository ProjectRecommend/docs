# ProjectRecommend

## Feasibility Analysis:
#### Rajdeep Mukherjee
#### NIIT University
##### 18 Sep 2016

## Analysis of the Problem:
Music lovers all across the world and even people trying to bide their time listening to music always want a continuous flow of music so that they don't have to go over to their phones or desktops changing the next music to their taste, this is were we thought we would come in.
A recommendation system is such that it can suggest music to anyone based on their current taste of music. It is powerful tool that can automatically give you feedbacks of what music you would like to download and make a playlist of without having you to go through all the songs yourself.
Online music recommendation systems include youtube, soundcloud, gaana and so on.. There are mainly 2 limitations of these services:
- Firstly an important point to be noted here is that these recommenders only recommend music from outside your own music collection.
- Secondly, most of these services are paid or you need to subscribe to get the service.

## Limitations and constraints:
We had come up with 3 different approaches to music recommendation:
- Collaborative filtering:
In this technique user data in a requirement. Users provide data in terms of a few parameters like the genre of music the user listens to often and so on but due to lack of time and resources we do not have that user data to go for collaborative filtering although it is generally the goto approach for music recommendation.
- Waveform Analysis:
In this technique we analyze the waveform and specify the float values to various music genres and we can recommend songs comparing those float values to other songs. Although it seems to be a good technique it is currently under research and hence is in it nascent stage, so we are not taking this into consideration.

## Economic Feasibility:
This is an open source software and hence we do not have any intentions of making profit through it as of now. Although we do intend to scale it later, we do not plan to earn revenue. People interested in this project can contribute on [github](https://github.com/ProjectRecommend).

## Conclusions from survey:
 In order to get an clear idea of what people may think about this product, we conducted a survey.
 110 responses were collected and here is a summary of what they thought of the idea.
 - 1.
<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q1.PNG" alt = "Question 1 and its response!" height = auto width = "400px" ></center>

As expected most people often wants to listen to music everytime.

- 2.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q2.png" alt = "Question 2 and its response!" height = auto width = "400px"></center>

It seems that almost 40 percent of people have a music collection of less than 10 gb and 33 percent have a music collection of 10 to 50 gb. This gives us an idea of our local store design and no of track metadata that we will have to keep in order to provide a good user experience.


- 3.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q3.png" alt = "Question 3 and its response!" height = auto width = "400px" ></center>

It seems music lovers often download music and add it to their collection. However a major lot actually does not do it all that often.

- 4.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q4.png" alt = "Question 4 and its response!" height = auto width = "400px" ></center>

Their is no conflict that most people are absolutely thrilled about music and would like to discover new music all the time.
- 5.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q5.png" alt = "Question 5 and its response!" height = auto width = "400px"></center>

Most people are of the opinion that they find it difficult to search songs similar to  the offline music library and so they would like to have an application do it for them.
- 6.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q6.png" alt = "Question 6 and its response!" height = auto width = "400px" ></center>

So most people it seems do not have an offline music library fully updated with the latest metadata. The ones which have probably buys songs from paid sources like gaana plus.

- 7.<center><img src="https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/q7.png" alt = "Question 7 and its response!" height = auto width = "400px" ></center>

For the final question more than three fourth of the people wanted to have an offline music recommendation system that can actually suggest similar songs for them.

## Conclusion

This survey was super important as it laid out the our feasibility for planning the project. If the project was not really wanted by people, there would be absolutely no use in making this project.
