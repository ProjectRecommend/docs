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
The purpose of this document is to describe the implementation of the *Music Recommendation Software* whose requirements have been described in detail in the SRS document submitted before.

The *Music Recommendation Software* as specified earlier, is a music player software that not only plays music but also suggests music based on what the user is listening to, from the user's offline collection as well as online collection, which obviously, requires internet connection. Also it has been designed to update the metadata of the same.

The sections in this document will provide guidelines related to the structure and the design of the project and will contain the following too.

**Class Diagram** : specific information about the expected input, output, classes, and functions. The interaction between the classes to meet the desired requirements.

**Sequence Diagram** : specific information about how objects operate with one another and in what order.

## 1.2 Development Project Scope
- Name of the project is "Project Recommend". It is a Desktop App.

- Offline music recommendation is an area of application development that is yet to be fully explored as there has not been enough attempts to develop a software to fulfil this need. Browsing over the internet, one may get enough music recommenders online but that is the real catch here, they are mostly **_online_**. Here, our development team is trying to build an **_offline_** music recommender application to fulfil users need of getting music suggestions based on their already present music collection.

- Offline Music recommendation plays music and involves recommendation of familiar tracks and familiar genres of music available both on the internet and from offline library which is available inn user's machine.

##### Advantages
- It provides suggestions from local music library.
- Works with slower internet connection because it needs less bandwidth for providing recommendations.
- It uses [MusicBrainz][musicbrainz-website] database for getting metadata of all the music present in user's local library and recommend tracks.
- it is not platform or service specific.
- it is not bounded with any music provider services so it is suggestions are not limited to particular service.
- There are no specific audience for this software. Anyone can install it and use it.


## 1.3 Definitions, acronyms, and abbreviations
- TBD means "To be Decided", these are the components that are not yet decided.
- ** More abbreviations are to be written here, after the doc  completion**.
- Terminology definitions are given in the following table.

| Term | Description |
| --- | --- |
| User | Any living being who is interacting with the software is a _user_.|
| System | The package of all the components which takes input and gives output to demonstrate the features of the software is called System. |
| Database | Collection of information on different topics related to each other. |
| Library| The collection of tracks inside a directory or across multiple directories forms up a _library_.|
| Store | This is the persistence layer of whole system. |
| Metadata | The set of data which describes and gives information about the sound track. |
| Recommender system | A system which takes a track as input and outputs set of tracks closely related to the input. |
| Classifier| An algorithm that implements classification, especially in a concrete implementation. It is the part of _recommender system_. |
| Tags | A label attached to track which gives extra information about it. |
| NIC | A network interface card (NIC) is a computer circuit board or card that is installed in a computer so that it can be connected to a network |

## 1.4 References
- This document is written in github flavored Markdown.

- IEEE. IEEE Standard 1016 IEEE Recommended Practice for Software Design Specifications. IEEE Computer Society, 1998.

## 1.5 Overview
- This document is divided into sections 2, 3, 4, 5, 6 and 7 with intended readers being, the developers and software managers but sections have been written in a manner that it can be understood by anyone having little knowledge about software.

This *Software Design Specification* also includes:

- System architecture description.
- Detailed description of components. ( including the template description for each component)
- Reuse and relationships to other products.
- Design decisions and tradeoffs.
- Pseudocode for components.

The design has been made clear, using the class diagram and sequence diagram.

# 2. System architecture description

Recommend (Our Software/System) is strictly based on modular architecture, there is four modules
in system that are functionally connected to each other as per Cohesion rules and these components
are Coupled as per Data coupling

## Coupling and Cohesion of System

#### Data Coupling

As per Definition one System have Data Coupling when *modules share data through, for example, parameters. Each datum is an elementary piece, and these are the only data shared (e.g., passing an integer to a function that computes a square root)*

From Sequence Diagram[todo - add link] we can see that System passes Data around hence system have Data Coupling.

#### Functional Cohesion

todo - add links to components

As per definition one system is in Functional Cohesion  *when parts of a module are grouped because they all contribute to a single well-defined task of the module*

as we can see that in our system each module contains classes that all contribute in a single Task.

- Music Player

    Music Player module handles functionality related to playing and handling music

- Local Storage

    Local Storage module functions as a Persistence Layer (Storage) of system.

- Meta Data

    Meta Data module handles all functionality related to Meta Data (ID3 Tags)

- Classifier

    Classifier handles all functionality related to Recommendation of songs for a songs



## 2.1 Overview of modules / components

The structure of our project is highly modularised. We have tried introducing as much functional cohesion as possible. For coupling we have tried to achieve data coupling.

Our components are: 
    
### Component: Music Player

##### Class: ManageSongs

| function                      | input                                                         | output                                                                      | description                                                                 |
|-------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| +add(SongPath:string):boolean | SongPath:absolute path to the music file                      | Status:Success or failure                                                   | adds song to Local Storage                                                  |
| +remove(SongId:int):boolean   | SongId: id of the corresponding music file from Local Storage | Status:Success or failure                                                   | Removes song from Local Storage                                             |
| +query():Dict                 | void                                                          | Dict: Dictionary containing key value pairs of all songs from Local Storage | Reads all entries from Local Storage and returns them in custom dictionary. |

##### Class: ControlMusic

| function                                                      | input                                                         | output                    | description                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------|---------------------------|----------------------------------------------------------------------------|
| +Play(SongID:int):boolean                                     | SongId: id of the corresponding music file from Local Storage | Status:Success or failure | fetches absolute path to song file from Local Storage and plays music file |
| +Pause():boolean [TODO:update class diagram on this function] | void                                                          | Status:Success or failure | Pause the currently playing music if its playing                           |
| +seek(minute:int, second:int): boolean                        | minute: target minute to seek second: target second to seek   | Status:Success or failure | Seeks currently playing song to required minute and second.                |
| +Stop():boolean [TODO:update class diagram on this function]  | void                                                          | Status:Success or failure | Stops the currently playing song if it is playing                          |


### Component: LocalStorage

##### Class: AcessLocalStorage

| function                        | input                                                         | output                                                                                      | description                                                                         |
|---------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Read(SongID: int):Dict          | SongID: id of the corresponding music file from Local Storage | Dict: Dictionary containing key value pairs of song data of given SongID from Local Storage | Reads entry of given SongID from Local Storage and returns it in custom dictionary. |
| Write(SongPath: String):boolean | SongPath:absolute path to the music file                      | Status:Success or failure                                                                   | Creates a new entry for music file in LocalStorage if it's  not in LocalStorage     |
| Update(SongID:int):boolean      | SongID: id of the corresponding music file from Local Storage | Status:Success or failure                                                                   | Updates entry of given SongID in Local Storage                                      |
| Delete(SongID:int):boolean      | SongID: id of the corresponding music file from Local Storage | Status:Success or failure                                                                   | Deletes entry of given SongID from Local Storage                                    |

### Component: Meta Data

##### Class: ManageMetaData

| function                                          | input                                                                           | output                                                                                       | description                                                                                            |
|---------------------------------------------------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| +ReadMetaData(SongID:int):Dict                    | SongID: an integer that defines the unique ID of the song  in the LocalStorage  | Dict: a dictionary containing the key value pairs of metadata that is returned from the song | Fetches path of the song from LocalStorage based on the ID and fetches the song metadata from the file |
| +WriteMetaData(SongID:int):boolean                | SongID:an integer that defines the unique ID of the song in the LocalStorage    | returns true if method could successfully write into the music file, false otherwise         | Fetches path of the song from the LocalStorage based on the songID and writes metadata into that song  |
| +FetchMetaDataFromMusicBrainz(SongID:int):boolean | SongID:an integer that defines the unique ID of the song in the LocalStorage    | returns true if method could successfully write into the music file, false otherwise         |                                                                                                        |

## 2.2 Structure and relationships

## 2.3 User interface issues



---------------------------------

# Extras

# References

- [Cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science)#Types_of_cohesion)

- [Coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming)#Types_of_coupling)

- [Why not to use Global Variables](http://wiki.c2.com/?GlobalVariablesAreBad)
