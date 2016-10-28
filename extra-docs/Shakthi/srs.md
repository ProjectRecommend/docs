<div align=center>
  <h1>Software Requirements Specification</h1>
  <h2>Project Recommend</h2>
  <b> Music Recommendation System </b><br />
  <b> Version <i>1.0</i></b>
</div><br /><br />


#### Team Project Recommend
- **S. Shakthi**  U101114FCS196

#### NIIT University
##### 18-Sep-2016

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

----

# 1. Introduction <a name="introduction"></a>
## 1.1 Purpose <a name="introduction-purpose"></a>
The document provides a complete view of the Software requirement specification of the Software Project "Project Recommend".

The Main Aim of this project is to provide the user with Music track recommendations from offline Libraries.

Tools required for this project are Libraries for Front-end, Back-end, Database and Classifiers.

## 1.2 Document Conventions <a name="introduction-dc"></a>
- All terms are in italics style.
- Main features or important terms are in bold style.
- TBD means "To be Decided", these are the components that are not yet decided

## 1.3 Intended Audience and Reading Suggestions <a name="introduction-iars"></a>
- Anyone with some basic knowledge of programming can understand this document. The document is intended for Developers, Software architects, Testers, Project managers and Documentation Writers.
But anyone with programming background and some experience with UML can understand this document.

- It is divided into 5 phases with sections 3, 4, 5 being intended for developers and software managers but other sections can be understood by anyone having little knowledge about software.

This Software Requirement Specification also includes:

- Overall description of the product
- External interface requirements
- System Features
- Other Non-functional requirements


## 1.4 Product Scope <a name="introduction-product-scope"></a>

- Offline Music Recommendation is new and has not been explored much. Everyone can find a website _**Online**_ which would have a feature of recommendation but _**Offline**_ Music recommendation is something which our Team is up for which would recommend songs from one's Offline song Library on Local Disk.

- Offline Music recommendation will involve recommendation of familiar tracks and familiar genres of music available both on the internet and from offline library.

- Name of the project is "Project Recommend". It is a Desktop App.
- It plays music and provides suggestions based on track which user is listening to from both offline library which is available in user's machine as well as on internet.

##### Advantages
- It provides suggestions from local music library.
- Works with slower internet connection because it needs less bandwidth for providing recommendations.
- It uses [MusicBrainz][musicbrainz-website] database for getting metadata of all the music present in user's local library and recommend tracks.
- it is not platform or service specific
- it is not bounded with any music provider services so it is suggestions are not limited to particular service
- There are no specific audience for this software. Anyone can install it and use it.

## 1.5 References <a name="introduction-references"></a>
- This document is written using Markdown in Github.

- IEEE. IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society, 1998.

## 1.6 Terminology <a name="introduction-terminology"></a>
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


# 2. Overall Description <a name="od"></a>

## 2.1 Product Perspective <a name="od-pp"></a>
This system consists of three components packaged as one desktop application:

- **Music player**: for playing music from local library.
- **Classifier**: It will generate suggestions as per the songs being played.
- **Metadata updater**: It will update the metadata of the songs present in the user's library. This is done using already available online database like "[MusicBrainz][musicbrainz-website]".
- **Local Store**: It is implemented as a [SQLite](https://www.sqlite.org) database which acts as a map between track titles, paths and keeps a check on each track for its metadata information.

With _music player_ user can play/pause/stop/seek a track. It is a fully functional music player like any other music player currently available.

Classifiers need some requirements to be functional in form of inputs which may be any field detail of the song such as the name of the song, movie name to which it belongs and so on. And the basis of these inputs it would suggest songs from the local library or from the Internet.

Metadata updater is very similar to MusicBrainz's [Picard][picards-website] software. It takes sound track or list of sound tracks as input and update their metadata information according to information available in [MusicBrainz database][musicbrainz-database-website]. This component needs internet for functioning.

Local database maintains a list of tracks along their path in system which user wants to listen and mark them as updated and not updated on the bases of their synchronization with MusicBrainz database. This helps the system to keep all the tracks updated and minimizes the need of updating whole user library at once which may slow down the system.

#### Component Diagram
![](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/Component_Dirgram_PR.jpg)


## 2.2 Product Functions <a name="od-pf"></a>
Using this app, user can play tracks available in offline library. While playing music user can get a list of suggested tracks which are most closely related with the present track in terms of their metadata tags like singer, genre, release year, rating etc. These tracks may be present in offline library or online sources.

Functions available to the user:

- play/pause/stop/seek, control volume
- add tracks/ remove tracks
- update metadata
- get recommendation



## 2.3 User Classes and Characteristics <a name="od-ucc"></a>
Almost everyone in this world is a music lover hence this application will be beneficial to all and particularly to those who prefer listening to a particular genre of songs.

Users with poor internet connectivity will benefit even more because the only place we require internet connection is where we are required to update the metadata of the music for giving correct suggestions.


## 2.4 Operating Environment <a name="od-os"></a>

#### System Requirements

- Operating System should be capable of playing music and have any of mentioned OS installed
- Internet Connection is required for suggestions and metadata updation

#### Platforms Include

##### GNU/Linux

- CPU Type : Pentium 4 or higher; 2 GHz or higher
- Memory/RAM : 1 GB minimum, up to the system limit
- Hard Disk : 4 GB or higher
- Graphics : X Window server or similar graphics server

##### Windows

- Processor: 1 gigahertz (GHz) or faster.
- RAM: 1 gigabyte (GB) (32-bit) or 2 GB (64-bit)
- Free hard disk space: 16 GB.
- Graphics card: Microsoft DirectX 9 graphics device with WDDM driver.


## 2.5 Design and Implementation Constraints <a name="od-di"></a>

For recommendations the updated metadata is used.

Filtering is done in various ways:
- Content Filtering in which tracks are grouped on the basis of information (Metadata) available about the music track.
- Collaborative Filtering in which only metadata of the music is used completely. Unlike the content filtering where the user data is also taken leading to less reliable results.
- Waveform Analysis in which the Music track is analysed and mostly gives results inaccurately.


## 2.6 User Documentation <a name="od-ud"></a>
- The User Manual explain the various features and ways to use them.
- "Help" option is also available to the user.

## 2.7 Assumptions and Dependencies <a name="od-ad"></a>

The following lists the various open source material we had referred to:

- Music database
- music tagging application
- Handling of audio metadata using
- Music player
- Python cross platform GUI toolkit
- Sci-kit learn for learning about Classifiers


# 3. External Interface Requirements <a name="eir"></a>

## 3.1 User Interfaces <a name="eir-ui"></a>

User interface is implemented in PyQt that is a python library. There is one front page which interacts with user. It is divided into frames for different functions. There may be

#### UI Mockup
![](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/mockup.png)


## 3.2 Hardware Interfaces <a name="eir-hi"></a>

- Input device is needed for user to interact with system.
- Software needs a display device to interact with user.
- Music player needs playback device for sound output.
- Network interface card will also be used.

## 3.3 Software Interfaces <a name="eir-si"></a>

TBD

## 3.4 Communications Interfaces <a name="eir-ci"></a>
- The Internet connection is used by metadata updater and classifier.
- Internet communication will be Encrypted.
- All Network Communications will use HTTPS/TLS.

# 4. System Features <a name="sf"></a>

Use case Diagram:
![use case diagram](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/PR_Use_case.jpg)

----

##### Use case description table

| Use Case Title (ID) | Description | Remarks |
| --- | --- | --- |
| Manage Songs (UC1) | generalization of Manage songs |   |
| Control Music (UC2) | generalization of control songs |   |
| Manually Get Next recommendation (UC3) | user triggered recommendation |   |
| Edit Metadata (UC4) | user edits metadata |   |
| Manually update metadata (UC5) | user manually triggers metadata updation service |   |
| Control Volume (UC6) |  use controls volume |   |
| Play (UC7) | user can play music |   |
| Pause (UC8) | user can pause |   |
| Seek (UC9) | user can seek into timeline of playing track |   |
| Stop (UC10) | user can stop the playing track |   |
| Next Track (UC11) | user can change to next track |   |
| Previous Track (UC12) | user can go to previous track |   |
| Add songs (UC13) | user can add songs |   |
| Remove Songs (UC14) | user can remove songs from list |   |
| Access Local Storage (UC15) | components can access local storage for persistence  |   |
| Read from local Storage (UC16) | components can read from local storage |   |
| Write into local Storage (UC17) | components can write into local storage |   |
| Update into local Storage (UC18) | components can update data into local storage |   |
| Delete from local Storage (UC19) | components can delete items from local storage |   |
| Run Classifier (UC20) | components can run classifier on a track |   |
| Get data from MusicBrainz (UC21) | components can get metadata of a track from musicbrainz servers |  |
| Get Recommendation (UC22) | components can get recommendation on a track |   |
| Update Metadata (UC23) | components can update metadata of tracks |   |


----

**Project Recommend** comes with the following set of system features

#### Music player

The Music player is a part of the offline music recommender which has various functionality similar to a Normal music player.
The user will import music from the local storage which will be furthur inserted to the local store. And through the local store we can add and remove songs.

#### Local Store

Local Store is persistence layer of application, it will be implemented as SQLite Database.
it will store all the information required for software to work.The user will be able to essentially cache data into a local store while importing a track into the application.
The Local Store will be storing the **the file path of the track, whether the track has been correctly tagged or not, the MusicBrainz track id and the id of the track.**
On adding a track or importing a track from the offline music library of the user to the application the track will be added into the local store.
On removing the track from the application the track will also be removed from the Local store. In short the Local store maintains the library of the application.
It will not be available for user to direct interaction, This component will be used by other components internally.

#### Music Metadata Updater

This component of the application is simply involved with updating the metadata or tags of music optionally from MusicBrainz database.
This component is involved in 2 different situations:
   - Firstly if the user plays a track and Classifier gets triggered and if metadata for that track is not updated This component will be triggered by classifier.
   - Secondly the user can Manually trigger metadata updation.

#### Classifier

The classifier is the core of this application as it takes the heavy lifting of suggesting the right tracks for the user.
The classifier comes into effect in 2 different situations
   - Firstly when the user chooses to play the music, the currently playing track will automatically be used for getting suggestions, play process will trigger the classifier.
   - Secondly the user can get suggestions on a track that he/she is not playing. In that case also the classifier will be used. in that case use will manually trigger Classifier on particular track.

#### Musicbrainz database

The Musicbrainz database is the primary database for collection of **correct** music metadata and it contains almost every single track.
This database is used during metadata updation and getting data for classifier to generate suggestions.

#### User actions

This section will state all the use cases of the application and what the user will be able to do with the application.

**Music management**

The user will be able to manage music, import and export. The user will be able to import music files from offline music collection and also remove music files from the application.

**Control music**

The user can control music in the music player component by the following actions:

- play music
- pause music
- control volume
- go to the next track
- go to the previous track
- seek a playing track

**manual updation of metadata**

The user will be able to manage metadata of the tracks that he/she chooses.

**manual recommendation of music**

The user can get recommendation of a track manually by clicking on it.

A summary of the direct actions that the user can take is as follows:

**Actor: User**

| action  | description |
| --- | --- | --- |
| import music from external system | the user will be able to import music from his external music collection, simply a hard drive or a flash drive |  
| remove tracks from playlist | The user will be able to remove any track from the playlist |
| play music | Part of the music player |
| seek track | seek a playing track |
| pause music | Part of the music player |
| stop music | Part of the music player |
| go to the next track | Part of the music player |
| go to the previous music | Part of the music player |
| volume control | Part of the music player |
| manual metadata update | The user can update the metadata of the track simply by right clicking |
| manual recommendation of track | The user can also get recommendations of the tracks manually |

#### User Interactions

**Use case: Manage tracks**

**Brief Description**

The user manages tracks, can import and remove them from the application.

**User interaction**

- Import tracks from offline music collection
- Add directories, sub directories and files to the music player.
- The user can remove the track from the application
- The local store updates itself deleting the track

**Use case: Control Music**

**Brief Description**

The user can control music which means he/she can play, pause, stop, go to the next track, go to the previous track, control the volume

**User interaction**

- Click events trigger all controlling of music operations.
- On playing a track, the play process triggers an event that gets recommendations for the track
- The system checks whether the metadata is already updated or not, if not then the metadata is updated in the track
- The system connects to the Musicbrainz database to update the track metadata.
- The system fetches tags of the track.
- After metadata updation the local store is updated for the current track.
- The system then runs classifier on the track and gets all suggestions for that track.
- The suggestions are updated into the local store.

**Use case: Manually get recommendation**

**Brief Description**

The user can manually get recommendation of a track other than the track that is being played.

**User interaction**

- The user triggers event of getting recommendation of a track.
The system checks whether the metadata is already updated or not, if not then the metadata is updated in the track
- The system connects to the Musicbrainz database to update the track metadata.
- The system fetches tags of the track.
- After metadata updation the local store is updated for the current track.
- The system then runs classifier on the track and gets all suggestions for that track.
- The suggestions are updated into the local store.


**Use case: Edit metadata**

**Brief Description**

The user can also edit the metadata of the songs.

**User interaction**
- Whatever metadata the user updates in also gets updated in local store.

**Use case: Manually update metadata**

**Brief Description**

The user can manually trigger updation of metadata of a track such that he/she can simply click on a track and update the metadata.

**User interaction**

- The user triggers an event of manually updating the  metadata of a track
- The system connects to the Musicbrainz database.
- The system fetches the metadata of a track from the database
- The system then updates the metadata into the local store.


# 5. Other Nonfunctional Requirements <a name="onr"></a>


## 5.1 Performance Requirements

- System should be fast enough to play music without any shattering or buffering, otherwise
that will result in undesirable experience.
- System should be robust to deal and act accordingly  with common error scenarios like no
internet connection, unavailable metadata, unsupported file types.
- In case of failures it should be able to fail or recover gracefully.
- System should be usable and fast enough to response to user action or give feedback to action, ideally under 1/60 second hence achieving 60 Frames Per Second.


## 5.2 Safety Requirements

- In scenario when there is not enough data to automatically tag Metadata we rely [AcoustID](https://acoustid.org/) and [MusicBrainz](https://musicbrainz.org/) for metadata
based on AcoustID fingerprint, in some but rare scenarios it can result in incorrect metadata of song,
to prevent that scenarios user can manually edit metadata of songs when it see an incorrect tagged song

## 5.3 Security Requirements

- Connection between user and [MusicBrainz](https://musicbrainz.org/) servers should be Encrypted (HTTPS/TLS).

## 5.4 Software Quality Attributes

- Memory leak should be prevented.
- Co-existence of the Systems together.

## 5.5 Business Rules

- This software is an Open Source software.
- Unless required by applicable law or agreed to in writing, software distributed is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

## 6 Other Requirements

TBD
----------------------------------

## Comments

#### Suraj :
- Use proper links of the sources beside the point itself.

#### Rajdeep :
- Write the table of contents according to the general syntax used as everyone.

#### Raghav :
- Inside the OS Requirements mention everything in detailed format along with features like disk requirements.

#### Pranshu :
- The Non Functional requirements are to be done as discussed in meeting.

#### Saumya :
- Highlight the important words.

## Actions taken

#### Implemented all the changes mentioned by team members.
