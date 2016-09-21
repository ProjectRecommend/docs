 <div align=center>
   <h1>Software Requirements Specification</h1>
   <h2>Project Recommend</h2>
   <b> Music Recommendation System </b><br />
   <b> Version <i>alpha</i></b>
</div><br /><br />

Prepared by Rajdeep Mukherjee
NIIT University  
17-Sep-2016  

<hr/><br />

# Table of contents
1. [Introduction](#introduction)  
1.1 [Purpose](#introduction-purpose)  
1.2 [Document Conventions](#introduction-dc)  
1.3 [Intended Audience and Reading Suggestions](#introduction-iars)   
1.4 [Product Scope](#introduction-product-scope)  
1.5 [References](#introduction-references)  
1.6 [Terminology](#introduction-terminology)
2. [Overall Description](#od)  
2.1 [Product Perspective](#od-pp)  
2.2 [Product Functions](#od-pf)  
2.3 [User Classes and Characteristics](#od-ucc)  
2.4 [Operating System](#od-os)  
2.5 [Design and Implementation Constraints](#od-di)  
3. [External Interface Requirements](#eir)  
3.1 [User Interfaces](#eir-ui)  
3.2 [Hardware Interfaces](#eir-hi)  
3.3 [Software Interfaces](#eir-si)  
3.4 [Communications Interfaces](#eir-ci)  
4. [System Features](#sf)  
5. [Other Nonfunctional Requirements](#onr)
6. [Other Requirements](#otherreq)  
[_Appendix_](#appendix)  
<hr />    




# Introduction<a name="introduction"></a>
### Purpose<a name="introduction-purpose"></a>

This software requirement specification describes how our development team has been able to come up with the tools and techniques to build this application.

Tools include:
* Programming language
* Libraries used for back end control of application
* Libraries used for UI and UX design of the application
* Database used for music referencing
* Classifiers used for classifying data and yielding recommendations

### Document Conventions<a name="introduction-dc"></a>


### Intended Audience and Reading suggestions<a name="introduction-iars"></a>
Intended for developers aspiring to build software involving the use of machine learning in order to classify files based on their metadata. This project includes an amalgamation of file metadata updation(in case of incorrect metadata in the corresponding file) and also classifier recommendation.

This Software Requirement Specification includes:
* Overall description of the product
* External interface requirements
* System Features
* Other non functional requirements

### Product Scope<a name="introduction-product-scope"></a>
Offline Music Recommendation is an area of application development that is yet to be fully explored as there has not been enough attempts to develop a software to fulfil this need. Browsing over the internet one may get enough music recommenders online but that is really catch here, they are mostly **_online_**. Here our development team is trying to build an **_offline_** music recommender application to fulfil users need of getting music suggestions based on their already present music collection.

Offline Music recommendation will involve recommendation of familiar songs and familiar genres of music available both on the internet and from offline library

Recommendation will involve suggestions based on the tags present for a particular song. This would mean that we would have to update the tags or in general the metadata of the song incase they are not appropriate.

The overall goal of this project will simply be to enhance listening experience of users so that they get all their favorite music collections in one place without having to scramble over the net to find music of their tastes. Now it is super easy just within a few clicks away in the same window

### References<a name="introduction-references"></a>
IEEE. IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society, 1998.


This Software Requirement specification has been entirely written with markdown([check it out](https://guides.github.com/features/mastering-markdown/) or [learn](http://www.markdowntutorial.com/)).

----
comments:
Raghav : First of all we should include Terminology as a section as is seen in most professional SRS documents. Also make sure to add 

# Overall description<a name="od"></a>
### Product Perspective<a name="od-pp"></a>
This is a new self contained product and therefore has nothing to do with a larger subsystem. The major subsystems of the overall application can be the following:
* Music player
* Updation of metadata of the music file in case of incorrect tags
* Music recommendation based on the user specified music

### Product Functions<a name="od-pf"></a>
The user will be able to include music files and folders into the application and play them, get suggestions for the music that he wants and update the metadata of the music in order to get the right recommendations of the music that he/she plays.

In short the user can do the following things:

>* Add files and folders containing music
* Play the music of his/her choice
* Request suggestions of a particular music or a whole collection of music
* In order to get the preferred music recommendations it may be required to update the metadata of the music so that it he/she can get the right suggestions.

### User Classes and Characteristics<a name="od-ucc"></a>
Almost any user will be able to easily get going with this application as it is perfectly meant for an average music lover. Music lovers especially interested in playing various genres of music in a playlist for background music playing for instance will be benefitted more than ever by this application as it does not require internet for playing the music.

Countries with poor internet connectivity will benefit even more because the only place we require internet connection is where we are required to update the metadata of the music for giving correct suggestions.

### Operating Environment<a name="od-oe"></a>
Platforms include:

* Linux

> Operating System	Red Hat Enterprise Linux 4 or 5 with the latest patches and upgrades
CPU Type	Pentium 4 or higher; 2 GHz or higher
Memory/RAM	1 GB minimum, up to the system limit
Hard Disk	4 GB minimum

* Windows

> Processor: 1 gigahertz (GHz) or faster.
RAM: 1 gigabyte (GB) (32-bit) or 2 GB (64-bit)
Free hard disk space: 16 GB.
Graphics card: Microsoft DirectX 9 graphics device with WDDM driver.
A Microsoft account and Internet access.

A stable internet connection.

### Design and Implementation Constraints<a name="od-dic"></a>
In this application we are using music metadata in order to classify music according to its corresponding parameters so that the application can suggest the correct type of music for the listener.

There are three approaches that had come to our mind:
* Collaborative filtering
> A standard approach used by most recommender applications for suggesting music to users. However in our case we are **not** going for storage of user data in any database. We do hope to bring upgrades of our version thus including that feature as well. We do not have enough time and resources to collect user data.

* Waveform analysis
> This technique is in its nascent stage and hence **cannot** be used as a **foolproof** method of recommender application to sort out music

### User Documentation<a name="od-ud"></a>
Users can find helpful resources about how and why they should use the software [here](www,resourcesMusicRecommender.com)

### Assumptions and Dependencies<a name="od-ad"></a>
We used various online open source material for most of our project work. We integrated various components from other projects in order to make the application work as a whole.

The following lists the various open source material we had referred to:
> * Music database [**_musicbrainz_**](https://musicbrainz.org/)
* music tagging application [**_MusicBrainz Picard_**](https://github.com/metabrainz/picard)
* Handling of audio metadata using [**_mutagen_**](https://github.com/nex3/mutagen)
* Music player [**_cherrymusic_**](https://github.com/devsnd/cherrymusic)
* Python cross platform GUI toolkit [**_PyQt_**](https://github.com/pyqt)

# External Interface Requirements<a name="eir"></a>
### User interfaces<a name="eir-ui"></a>
For user interface and user experience we used the PyQt toolkit as it had all the specific requirements that will be required for our application development. PyQt brings together the Qt C++ cross-platform application framework and the cross-platform interpreted language Python.
Qt is more than a GUI toolkit. It includes abstractions of network sockets, threads, Unicode, regular expressions, SQL databases, SVG, OpenGL, XML, a fully functional web browser, a help system, a multimedia framework, as well as a rich collection of GUI widgets.
Qt classes employ a signal/slot mechanism for communicating between objects that is type safe but loosely coupled making it easy to create re-usable software components.

TODO
### Hardware interfaces<a name="eir-hi"></a>
TODO

### Software interfaces<a name="eir-si"></a>
TODO

### Communication interfaces<a name="eir-ci"></a>
TODO

# System Features<a name="sf"></a>
Offline music recommender comes with the following set of system features:

The following is the use case diagram for the application:
![use case diagram](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/PR_Use_case.jpg)

> #### Music player
Built into the offline music recommender system is a music player that can play music with a number of controls including **play, pause, stop, play next song and volume**.

> The user must first be able to import music from his offline music collection which may simply refer to a hard-drive or a flash memory.

> On importing the song, the metadata of the file will be uploaded into the local mysql database that will be running.

> The user may also remove a song or the details of the song from the local database but this would mean that the next time the song is played it would have to be imported first and updated into the local database that would also involve an overhead.


> #### Local database
The user will be able to essentially cache data into a local database while trying to import a song into the application.
The database will be storing the **the file path of the song, whether the song has been correctly tagged or not, the musicBrainz track id and the id of the song.**

> On adding a song or importing a song from the offline music library of the user to the application the song will be added into the database.

> On removing the song from the application the song will also be removed from the database. In short the database maintains the library of the application.

> #### Music metadata Updater
This component of the application is simply involved with updating the metadata or tags of music optionally.

> This component is involved in 2 different situations:
* Firstly if the user plays a song automatically the metadata updater is going to attempt to update the tags of the song so that it can yield correct suggestions for that song.
* Secondly the user can actually get recommendation for songs that are not being played.

> #### Classifier
The classifier is the core of this application as it is gonna take the heavy lifting of suggesting the right songs for the user.

> The classifier comes into effect in 2 different situations:
* Firstly when the user chooses to play the music the music should automatically be used for getting suggestions.
* Secondly the user can get suggestions on a song that he/she is not playing. In that case also the classifier will be used. The user can manually get suggestions on a song.

> #### Musicbrainz database
The Musicbrainz database is gonna be the primary database for collection of **correct** music metadata and it contains almost every single song.
This database will be of use during metadata updation only.

This section will state all the use cases of the application and what the user will be able to do with the application.

**Music management**
> The user will be able to manage music import and export. The user will be able to import music files from offline music collection and also remove music files from the application.

**Control music**
> The user can control music in the music player component by the following actions:
* play music
* pause music
* control volume
* go to the next song
* go to the previous song

**manual updation of metadata**
> The user will be able to manage metadata of the songs that he/she chooses.

**manual recommendation of music**
> The user will be able to get recommendation of a music by manually simply by clicking on a song.

A summary of the direct actions that the user can take is as follows:

**Actor: User**

| action | description |
| --- | --- | --- |
| import music from external system | the user will be able to import music from his external music collection, simply a hard drive or a flash drive |  
| remove music from the application | The user will be able to remove any music from the application |
| play music | Part of the music player |
| pause music | Part of the music player |
| stop music | Part of the music player |
| go to the next song | Part of the music player |
| go to the previous music | Part of the music player |
| volume control | Part of the music player |
| manual metadata update | The user can update the metadata of the song simply by right clicking |
| manual recommendation of song | The user can also get recommendations of the songs manually |

The following are the use cases and how the actor: user interacts with them:
* **Use case: Manage songs**

> Brief Description:
The user manages songs import and remove from the application

> User interaction:
* The user can import songs from offline music collection
* The directories, sub directories and files are added to the application
* The local store updates the song
* The user can remove the song from the application
* The local store updates itself deleting the song


 * **Use case: Control Music**

> Brief Description:
The user can control music which means he/she can play, pause, stop, go to the next track, go to the previous track, control the volume

> User interaction:
* Click events trigger all controlling of music operations.
* On playing a song, the user triggers an event that gets recommendations for the song
* The system checks whether the metadata is already updated or not, if not then the metadata is updated in the song
* The system connects to the Musicbrainz database to update the song metadata.
* The system fetches tags of the song.
* After metadata updation the local store is updated for the current song.
* The system then runs classifier on the song and gets all suggestions for that song.
* The suggestions are updated into the local store.

* **Use case: Manually get recommendation**

> Brief Description:
The user can manually get recommendation that of a song other than the song that is being played.

> User interaction:
* The user triggers event of getting recommendation of a song.
The system checks whether the metadata is already updated or not, if not then the metadata is updated in the song
* The system connects to the Musicbrainz database to update the song metadata.
* The system fetches tags of the song.
* After metadata updation the local store is updated for the current song.
* The system then runs classifier on the song and gets all suggestions for that song.
* The suggestions are updated into the local store.


* **Use case: Edit metadata**

> Brief Description
The user can also manually edit his/her song's metadata

> User interaction:
* The user defined metadata of a song is going to be updated in the local store.

* **Use case: Manually update metadata**

> Brief Description:
The user can manually update metadata of a song such that he/she can simply click on a file(song) and update the metadata.

> User interaction:
* The user triggers an event of manually updating the  metadata of a song
* The system connects to the Musicbrainz database.
* The system fetches the metadata of a song from the database
* The system then updates the metadata into the local store.
