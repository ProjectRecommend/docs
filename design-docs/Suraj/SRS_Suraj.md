# Software Requirements Specification

    Product : Project Recommend
    Description : An offline music recommendation system
    Status : Under Review
    Development Status  : design phase
    Author : Surajnath Sidh

----

# Revisions

### Latest
    Current Version : 1.0
    Current Status : Under Review
    Date : 20-09-2016

### Revision History
- Version 0.0
    - Date : 14-09-2016
    - Reason For Changes : initial changes

----

# Table of Contents

##### 1
- 1.1 Purpose
- 1.2 Document Conventions
- 1.3 Intended Audience and Reading Suggestions
- 1.4 Product Scope
- 1.5 References

##### 2
- 2.1 Product Perspective
- 2.2 Product Functions
- 2.3 User Classes and Characteristics
- 2.4 Operating Environment
- 2.5 Design and Implementation Constraints
- 2.6 User Documentation
- 2.7 Assumptions and Dependencies

##### 3
- 3.1 User Interfaces
- 3.2 Hardware Interfaces
- 3.3 Software Interfaces
- 3.4 Communications Interfaces

##### 4
- 4.1 Use case diagram
- 4.2 Use case diagrams description table
- 4.3 Functional Requirements
- 4.4 System Features
    - music player
    - local storage
    - classifier
    - metadata updater


##### 5
- 5.1 Performance Requirements
- 5.2 Safety Requirements
- 5.3 Security Requirements
- 5.4 Software Quality Attributes
- 5.5 Business Rules

#### Comments
----


# 1 Introduction

## 1.1 Purpose

Project Recommend is a project to provide recommendation on your offline music collection that you have
in your computer locally.
This document describes Full system but it's emphasis is on Core part of system aka recommendation system

## 1.2 Document Conventions

- TBD - to be decided
- WIP - work in progress


## 1.3 Intended Audience and Reading Suggestions

This document is intended for Developers, Software architects, Testers, Project managers and Documentation Writers.
But anyone with programming background and some experience with UML can understand this document.

## 1.4 Product Scope

This software aims to solve the basic problem of providing recommendation on all of your offline music collection
it has some extra benefits like
- it works with low bandwidth connections
- it is not platform or service specific
- it is not bounded with any music provider services so it is suggestions are not limited to particular service

## 1.5 References

- TBD

# 2.Overall Description

## 2.1 Product Perspective

- This is self contained product, Project recommend is a music player with built in recommendation system
that also update metadata of songs if needed.
built in recommendation system  uses content based filtering as a technique to get recommendation for songs

#### Component Diagram
![](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/Component_Dirgram_PR.jpg)


## 2.2 Product Functions

- can listen to songs
- play, pause, forward playing songs
- get recommendation on songs
- update metadata of songs

## 2.3 User Classes and Characteristics

- there is no special user classes, anyone who case use a computer can use this software without any
issues.

## 2.4 Operating Environment

System Requirements
- Anything that can play music and have any of mentioned OS installed
- internet Connection is required for suggestions

OS
- GNU/Linux
- Windows


## 2.5 Design and Implementation Constraints

for building recommendation system we looked at few techniques that are used in recommendation systems.
that involves, Content based filtering, collaborative filtering and waveform analysis.
at the end we settled with content based filtering.
we couldn't implement collaborative filtering due to lack of data to train our classifier used in recommendation system, Waveform analysis is a topic of research right now and not matured yet, studies shows that if used with slightly wrong data it can give worse results then any other methods.
Spotify tried waveform analysis and got worse results then collaborative filtering.

## 2.6 User Documentation

Basic guide on How to use software will be available online and shipped with software help as well.
Software Source code will also be available along with it's Documentation under suitable Open Source license


## 2.7 Assumptions and Dependencies

we are not assuming anything other then clear assumptions.
##### Dependencies
- PyQT - Python building of Qt, used for GUI
- Mutagen - python library to manipulate ID3 tags
- MusicBrainz - for metadata


# 3 External Interface Requirements

## 3.1 User Interfaces

GUI is built using PyQt, python bindings of Qt framework

#### UI Mockup
![](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/mockup.png)


## 3.2 Hardware Interfaces

- Input device.
- Display.
- playback device for sound.
- Network Interface Card(NIC)

## 3.3 Software Interfaces

TBD

## 3.4 Communications Interfaces

- NIC for Internet Connection
- HTTPS for interfacing with MusicBrainz Database

# 4 System Features

Following is the use case diagram for the application
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

## Functional Requirements


| **Identifier for Requirement** | **Functional Requirement Name** | **Description** |
| --- | --- | --- |
| UC 03 | Manually recommend music | The user will be able to get recommendations of any track manually, i.e., simply by right clicking |
|  UC 04 | Edit fields in the song info | The user will be able to edit info of any track manually, i.e., simply by right clicking |
| UC 05 | Manually update metadata | The user will be able to update the metadata of any track manually, i.e., simply by right clicking |
| UC 06 | Volume control | The user will be able to increase or decrease or mute the volume of the playing track |
| UC 07 | Play music | The user will be able to play the track by selecting it or clicking on Play |
| UC 08 | Pause music | The user will be able to pause the track being able to play it again from the same timeline |
| UC 09 | Seek track | The user will be able to move anywhere in the timeline of the track |
| UC 10 | Stop music | The user will be able to stop the track which will close the track, in order for the user to play another track or exit software |
| UC 11 | Go to the next track | The user will be able to play the next track |
| UC 12 | Go to the previous track | The user will be able to play the previous track |
| UC 13 | Add songs | The user will be able to import music from his external music collection, to the application |
| UC 14 | Remove songs | The user will be able to remove any track from the playlist |


----

## Music player

Music player is used to handle and play music, this is the primary component that user has his control.
Music player is responsible for automatically triggering other component

## Local Storage

Local storage is persistence layer of system, all storage and information that need to be persisted goes to Local Storage,
it is core and essential for whole application to be functional.

## classifier
Classifier generates suggestions based on content and metadata of a track,
it utilizes MusicBrainz database to get similar songs and then orders local storage to cache to results
for a certain period of time.


## Metadata Updater
In some cases tracks does not have full or correct metadata, so in that scenarios classifier cannot function properly or provide relevant results, so metadata updater is responsible for
updating metadata of a track, it's a helper component that works hand in hand with other components.


# 5. Other Nonfunctional Requirements

### The non-functional requirements of the system are explained below.

----

| **Non-Functional Requirements** | **Name** | **Description** |
| --- | --- | --- |
| **5.1  Performance Requirements**   |
| NFR_01 | Quickness | System should be fast enough to play music and respond to any of the user action in any way without any shattering or buffering, else it will be not be a good experience. |
| NFR_02 | Robustness | System should be robust to deal and act accordingly with common error scenarios like no internet connection, unavailable metadata, unsupported file types. |
| NFR_03 | Failure Handling | In case of failures it should be able to fail or recover quickly. |
| **5.2  Safety Requirements**   |
| NFR_04 | Exception Handling | The software should be able to restrict or warn(in the first place) the user from doing things not suitable, like, increasing volume beyond threshold, or exiting the software w/o saving the changed data. |
| **5.3  Security Requirements**   |
| NFR_05 | Encrypted Connection | Connection between user and [MusicBrainz](https://musicbrainz.org/) servers should be Encrypted (HTTPS/TLS). |
| **5.4 Software Quality Attributes** |
| NFR_06 | Memory Management | System should not leak memory. |
| NFR_07 | Compatibility  | System should peacefully co-exist with other software |
| NFR_08 | Error Handling  | System should not cause or trigger any events that will leave Operating System in uNFRecoverable state |
| **5.5 Business Rules** |
| NFR_09 | Open Source | This software is an Open Source software. |
| NFR_10 | Guidelines | Unless required by applicable law or agreed to in writing, software distributed is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. |


----

# Comments from peers


#### Raghav


#### Saumya


#### Rajdeep


#### Shakthi


#### Pranshu
