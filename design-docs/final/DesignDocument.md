<div align=center>
  <h1>Software Design Document</h1>
  <h2>Project Recommend</h2>
  <b> Music Recommendation System </b><br />
  <b> Version <i>1.0</i></b>
</div><br /><br />

#### Team Project Recommend

- **Surajnath Sidh**  U101114FCS146
- **Rajdeep Mukherjee**  U101114FCS115
- **Raghav Mittal**  U101114FCS111
- **Pranshu Sahijwani**  U101114FCS104
- **S. Shakthi**  U101114FCS196
- **Saumya Gupta**  U101114FCS126

#### NIIT University
##### 26-Oct-2016

<hr/><br />


# Table of contents
1. Introduction

    1.1 Purpose of this document

    1.2 Scope of the development project

    1.3 Definitions, acronyms, and abbreviations

    1.4 References

    1.5 Overview of document

2. System architecture description

    2.1 Overview of modules / components

    2.2 Structure and relationships

    2.3 User interface issues

3. Detailed description of components

    3.1 Component template description

    3.2 X Component (or Class or Function ...)

    3.3 Y Component (or Class or Function ...)

    3.n Z Component (or Class or Function ...)

4.0 Reuse and relationships to other products

5.0 Design decisions and tradeoffs

6.0 Pseudocode for components

7.0 Appendices (if any)

SDS component template

<hr />

---------------------------------
# 1. Introduction

## 1.1 Purpose

The purpose of this document is to describe the implementation of the *Project Recommend ( Music Recommendation Software )* whose
requirements have been described in detail in the SRS document submitted before.

The *Music Recommendation Software* as specified earlier, is a music player software that not only plays music but also 
suggests music based on what the user is listening to, from the user's offline collection as well as online collection, which
requires internet connection. During recommendation if required it will update metadata of the song.

The sections in this document will provide guidelines related to the structure and the design of the project and will contain the following too.

**Component Diagram** : information about the external and internal components of the system.

**Class Diagram** : specific information about the expected input, output, classes, and functions. The interaction between the 
classes to meet the desired requirements.

**Sequence Diagram** : specific information about how objects operate with one another and in what order.

## 1.2 Development Project Scope

- Name of the project is "Project Recommend". It is a Desktop App.

- Offline music recommendation is an area of application development that is yet to be fully explored as there has not been 
enough attempts to develop a software to fulfil this need. Browsing over the internet, one may get enough music recommenders 
online but that is the real catch here, they are mostly **_online_**. Here, our development team is trying to build an **_offline_** music 
recommender application to fulfil users need of getting music suggestions based on their already present music collection.

- Offline Music recommendation plays music and involves recommendation of familiar tracks and familiar genres of music available both on 
the internet and from offline library which is available inn user's machine.

##### Advantages

- It provides suggestions from local music library.
- Works with slower internet connection because it needs less bandwidth for providing recommendations.
- It uses [MusicBrainz](https://musicbrainz.org/) database for getting metadata of all the music present in user's local 
library and recommend tracks.
- it is not platform or service specific.
- it is not bounded with any music provider services so it is suggestions are not limited to particular service.
- There are no specific audience for this software. Anyone can install it and use it.
- This software is open source which means anyone can contribute and suggest changes and features to the project.


## 1.3 Definitions, acronyms, and abbreviations

- TBD means "To be Decided", these are the components that are not yet decided.
- ** More abbreviations are to be written here, after the doc  completion**.
- Terminology definitions are given in the following table.

| Term | Description |
| --- | --- |
| User | Any living being who is interacting with the software is a _user_.|
| System | The package of all the components which takes input and gives output to demonstrate the features of the software is called System. |
| LocalStorage | This is the persistence layer of whole system. |
| Metadata | The set of data which describes and gives information about the sound track. |
| Recommender system | A system which takes a track as input and outputs set of tracks closely related to the input. |
| Classifier| An algorithm that implements classification, especially in a concrete implementation. It is the part of _recommender system_. |
| Cache | A software component in the system that preserves data for a defined life. |


## 1.4 References

- This document is written in github flavored Markdown.

- IEEE. IEEE Standard 1016 IEEE Recommended Practice for Software Design Specifications. IEEE Computer Society, 1998.

- Sample Software Design document for TheraWii, a software at [www.cs.drexel.edu](https://www.cs.drexel.edu/~dpn52/Therawii/design.pdf "Sample1").

- Sample Software Design document for a one runway airport, an air traffic controller simulation at [www.rivier.edu](https://www.rivier.edu/faculty/vriabov/CS552_SW_Design_Specification_Example.pdf "Sample2").


## 1.5 Overview

- This document is divided into sections 2, 3, 4, 5, 6 and 7 with intended readers being, the developers 
and software managers but sections have been written in a manner that it can be understood by anyone having 
little knowledge about software.

This *Software Design Specification* also includes:

- System architecture description.
- Detailed description of components. ( including the template description for each component)
- Reuse and relationships to other products.
- Design decisions and tradeoffs.

The design has been made clear, using the class diagram and sequence diagram.

# 2. System architecture description

Project Recommend (Our Software/System) is strictly based on modular architecture, there are four modules
in system that are functionally connected to each other as per Functional Cohesion paradigm and these components
are Coupled as per Data coupling.

## Coupling and Cohesion of System

#### Data Coupling

As per Definition one System have Data Coupling when *modules share data through, for example, parameters. Each datum is 
an elementary piece, and these are the only data shared (e.g., passing an integer to a function that computes a square root)*

From Sequence Diagram[todo - add link] we can see that System passes Data around hence system have Data Coupling.

#### Functional Cohesion

todo - add links to components

As per definition one system is in Functional Cohesion  *when parts of a module are grouped because they all contribute 
to a single well-defined task of the module*

as we can see that in our system each module contains classes that all contribute in a single Task.

- **Music Player**

    Music Player module handles functionality related to playing and handling music

- **Local Storage**

    Local Storage module functions as a Persistence Layer (Storage) of system.

- **Meta Data**

    Meta Data module handles all functionality related to Meta Data (ID3 Tags)

- **Classifier**

    Classifier handles all functionality related to Recommendation of songs for a songs


## 2.1 Overview of modules / components

The structure of our project is highly modularised. We have tried introducing as much functional cohesion as possible. 
For coupling we have tried to achieve data coupling.

## 2.2 Structure and relationships

## 2.3 User interface issues

-------------------------------------------------------

## 3. Detailed description of components

#### 3.1 Component template description

we are discussing components in below mentioned manner

## Component : Name of Component

Description of Component

### Class : Class X

Description of Class X

Description of class X functions in tabular form

| Function | input | output | Description |
| --- | --- | --- | --- |
| prototype | input parameters | return values and their types | description of function | 


### Class : Class Y

Description of Class Y

Description of class Y functions in tabular form

| Function | input | output | Description |
| --- | --- | --- | --- |
| prototype | input parameters | return values and their types | description of function |

-------------

Our components are: 

### 3.2 Component: MusicPlayer

Description: This component as a whole handles functionality related to playing music and controlling music.
Music Player functions are well defined by the methods that we have used in the corresponding classes. 

##### Class: ManageSongs

Description: Adds, Removes and queries songs from LocalStorage.

| function | input | output | description |
|----------|-------|--------|-------------|
| +add(SongPath:string):boolean | SongPath:absolute path to the music file | Status:Success or failure | adds song to Local Storage |
| +remove(SongId:int):boolean   | SongId: id of the corresponding music file from Local Storage | Status:Success or failure | Removes song from Local Storage |
| +query():Dict | void | Dict: Dictionary containing key value pairs of all songs from Local Storage | Reads all entries from Local Storage and returns them in custom dictionary. |

##### Class: ControlMusic

Description: Controlling of Music.

| function | input | output | description |
|----------|-------|--------|-------------|
| +Play(SongID:int):boolean | SongID: id of the corresponding music file from Local Storage | Status:Success or failure | fetches absolute path to song file from Local Storage and plays music file |
| +Pause():boolean  | void | Status:Success or failure | Pause the currently playing music if its playing |
| +next(SongID:int):boolean | SongID: id of the corresponding music file from Local Storage | Status:Success or failure | play the next song. |
| +prev(SongID:int):boolean | SongID: id of the corresponding music file from Local Storage | Status:Success or failure | play the previous song. |
| +seek(minute:int, second:int): boolean | minute: target minute to seek second: target second to seek   | Status:Success or failure | Seeks currently playing song to required minute and second. |
| +Stop():boolean  | void | Status:Success or failure | Stops the currently playing song if it is playing |
| +volControl(TargetVol: int):boolean | TargetVol: the target volume that must be chnaged is entered  | Status:Success or failure | Controls the volume |


### 3.3 Component: LocalStorage

Description: This is the persistence layer of the system. It holds data related to songs. 

##### Class: AcessLocalStorage

Description: Helper functions to access LocalStorage.

| function | input | output | description |
|----------|-------|--------|-------------|
| +Read(SongID: int):Dict | SongID: id of the corresponding music file from Local Storage | Dict: Dictionary containing key value pairs of song data of given SongID from Local Storage | Reads entry of given SongID from Local Storage and returns it in custom dictionary. |
| +Write(SongPath: String):boolean | SongPath:absolute path to the music file | Status:Success or failure | Creates a new entry for music file in LocalStorage if it's  not in LocalStorage |
| +Update(SongID:int):boolean | SongID: id of the corresponding music file from Local Storage | Status:Success or failure | Updates entry of given SongID in Local Storage |
| +Delete(SongID:int):boolean | SongID: id of the corresponding music file from Local Storage | Status:Success or failure | Deletes entry of given SongID from Local Storage |


##### Class: ManageLocalStorage

Description: Functions related to overall maintainence of the LocalStorage.

| function | input | output | description |
|----------|-------|--------|-------------|
| +Build():boolean | void | returns true if the LocalStorage is successfully built. | This function builds the database on first start up that is when the software is launched for the first time after installation |
| +Dump():boolean | void | returns true if successful in dumping the instance of LocalStorage and false otherwise | This function dumps the instance of the LocalStorage in case of un-installation of the software |
| +Connect():boolean | void | returns true if successful in connecting to the LocalStorage | Connects to the instance of the LocalStorage. This is done for each subsequent startup or launch of the application. |
| +Disconnect():boolean | void | returns true if successful in disconnecting from the LocalStorage | Disconnects from the LocalStorage. This is done for each closing of the application |
| +getIsConnected():boolean | void | returns the value of global variable isConnected.   | getter function for the isConnected global variable. Once connection is established isConnected variable is set. On disconnection isConnected variable is cleared  |
| +setIsConnected(isConnected):void | isConnected variable is set | void | setter function for the isConnected global variable. Once connection is established isConnected variable is set. On disconnection isConnected variable is cleared. |

### 3.4 Component: MetaData

Description: This module handles metadata Manipulation and updation in the system, It is also responsible for 
fetching metadata from external sources like MusicBrainz.

##### Class: ManageMetaData

Description: Helper functions related to metadata handling.

| function | input | output | description |
|----------|-------|--------|-------------|
| +ReadMetaData(SongID:int):Dict | SongID: an integer that defines the unique ID of the song  in the LocalStorage  | Dict: a dictionary containing the key value pairs of metadata that is returned from the song | Fetches path of the song from LocalStorage based on the ID and fetches the song metadata from the file |
| +WriteMetaData(SongID:int):boolean | SongID:an integer that defines the unique ID of the song in the LocalStorage    | returns true if method could successfully write into the music file, false otherwise | Fetches path of the song from the LocalStorage based on the songID and writes metadata into that song  |
| +FetchMetaDataFromMusicBrainz(SongID:int):boolean | SongID:an integer that defines the unique ID of the song in the LocalStorage    | returns true if method could successfully write into the music file, false otherwise | it fetches metadata form a song from MusicBrainz service |
| +EditMetaData(SongID:int):boolean | SongID: the unique id of the song in the LocalStorage | returns true for success and false for failure | updates song metadata. |
| +getIsUpdated():int | void | returns the value of IsUpdated variable | getter function for IsUpdated function  |
| +setIsUpdated(isUpdated) | isUpdated variable | void | sets the global variable IsUpdated |

### 3.5 Component: Classifier

Description: This component is the core of the system. It handles the part of recommendation of new songs based on a given song.

##### Class: GetRecommendation

Description: This class contains functions for fetching relevant songs of a song and predicting(recommending) new songs that user might like. 

| function | input | output | description |
|----------|-------|--------|-------------|
| +FetchRelevantSong(SongID:int):Dict | SongID: id of the corresponding music file from Local Storage | Dict: Dictionary containing key value pairs of data of relevant Songs of the Song. | Reads data of given songID and Triggers MetaData Updation if MetaData of Given Song is not Updated. if Metadata is already updated, it reads that metadata otherwise waits for MetaData Updation to complete and then Reads it.After reading of metadata it Fetches relevant songs from that metadata from MusicBrainz Database and returns them in Custom Dictionary  |
| +Predict(SongID: int, RelevantSongDict: Dict) : Dict | SongID: id of the corresponding music file from Local Storage.RelevantSongDict: Custom Dictionary of Relevent Songs Returned by *FetchRelevantSong* | Dict: Dictionary containing key value pairs of data of predicted(Recommended) Songs of the Song. | Takes the Result of *FetchRelevantSong* and returns the recommended song, this is the step that uses our trained Classifier to recommend Songs |


##### Class: ManageCache

Description: This class manages Cache of songs that are suggested by the GetRecommendation class.  

| function | input | output | description |
|----------|-------|--------|-------------|
| +ReadCache(SongID:int): Dict | SongID: id of the corresponding music file from Local Storage | Dict : Custom dictionary of recommended songs of given SongID from cache | Reads cache for Recommended songs of a given song and if these is a cache miss it will trigger the *GetRecommendation* to get recommendation, if it triggered *GetRecommendation* then when *GetRecommendation* will write result to cache it will tries again and gets result from Cache. |
| +WriteCache(PredictedSongDict:Dict) : boolean  | PredictedSongDict : Dictionary of Predicted (Recommended) Songs that is returned by *Predict* function. | Status:Success or failure | It Takes Dictionary of Predicted (Recommended) Songs that is returned by *Predict* function and Writes that into Cache. |
| +invalidateCache():boolean | Void | Status:Success or failure | It gets triggered on each startup,it removes entries from Cache that are older then our pre-defined cache lifetime |
| +dumpCache():boolean | Void | Status:Success or failure | It removes all entries from cache. |
| +DeleteCache(SongID:int):boolean | SongID: integer that uniquely identifies the song in the LocalStorage | Status:Success or failure | Deletes specific songs from the cache. |


---------------------------------

# 4.0 Reuse and relationships to their products
-------- TODO - Not Applicable Section--------

If a project is doing some enhancement work, it requires to look into reuse issues. This project is using the existing concept of a basic music player, which plays music, with the usual user requirements of playing previous, next songs, adding and removing songs, and volume control. In addition to that, the software will recommend music too, based on what the user is listening. We already have many tools doing that, such as Pandora, Spotify, SoundCloud etc. But these applications suggest music from their existing online libraries, demand an account to be created and also an internet connection.

So, the enhancement this project offers to the user is recommendation from the user's offline collection. This obviously, requires internet connection, if the recommendations are not cached. But once cached, it recommends music even when the user is offline.


# 5.0 Design decisions and tradeoffs
The source code is written in python language.
- **PyQT** - is a Python interface for QT, a cross-platform GUI library.
 - for the GUI framework of the music player. The project uses the multimedia helper classes.
 - networking module wherever networking connections are made.
 - multimedia module for multimedia access.
 - database connector module for local storage and cache.
- **mutagen**: is a python module used as a Python multimedia tagging library.
  - for accessing and handling audio metadata.
  - It has no dependencies outside the Python standard library.
- **Nose** - is a python unit test framework
  - for unit testing.
  - It is a good candidate for go-to test framework.
- **The MusicBrainz Client library** (libmusicbrainz) - also known as mb_client, is a development library.
  - for adding MusicBrainz's lookup capabilities to the software.
  - It supports Windows, Linux amd Mac OS X.

# 6.0 Pseudocode for components
# 7.0 Appendices



# Extras

# References

- [Cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science)#Types_of_cohesion)

- [Coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming)#Types_of_coupling)

- [Why not to use Global Variables](http://wiki.c2.com/?GlobalVariablesAreBad)

- [Control flow with in UML sequence Diagrams](https://msdn.microsoft.com/en-us/library/dd465153.aspx)
