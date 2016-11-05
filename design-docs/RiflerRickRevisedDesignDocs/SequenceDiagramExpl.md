### Sequence Diagram Analysis

This Sequence diagram analysis is written in chronological order and so
please bear that in mind while reading through this doc.

![Sequence Diagram](C:/Users/riflerRick/Desktop/NiitUniversityCSE_course/3rdyr/semester5/softwareEngineering/project/gitRepos/docs/design-docs/images/Sequence_Diagram_PR.jpg)

User actions:

These are the actions that the user can actually do:
1. Play: The user can click the play button, thus being able to play the song
appearing before him/her.

Important point here is that we are not only are we playing the song but also searching other songs for recommendation.
So basically 2 jobs: playing the song and recommendation of similar songs both triggered by the same event

Class handling Event: **Control Music**

Triggers function: **Play(SongID:int):boolean**

Takes in parameter of SongID and passes it to the function

Next block of operations:

    {

        Class Handling Event: AccessLocalStorage

        Triggers function: Read(SongID:int):Dict

        Takes in the parameter of the songID and simply plays and returns a dictionary
        containing key value pairs of the song details.

        This function returns to Play function of ControlMusic class.
    }
    {
        Class Handling Event: **Managem
    }
