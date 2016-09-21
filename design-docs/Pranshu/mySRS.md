<div align=left>
  <h1>Software Requirements Specification</h1>
  <h2>Project Recommend</h2>
  <b> Version <i>1.0</i></b>
</div><br /><br />


### Prepared By:

#### **Pranshu Sahijwani**  U101114FCS104

#### NIIT University
##### 18-Sep-2016

<hr/><br />

# Table of contents
1. Introduction
1.1 Purpose
1.2 Document Conventions  
1.3 Intended Audience and Reading Suggestions   
1.4 Product Scope  
1.5 References
1.6 Terminology
2. Overall Description  
2.1 Product Perspective
2.2 Product Functions  
2.3 User Classes and Characteristics  
2.4 Operating System
2.5 Design and Implementation Constraints  
3. External Interface Requirements
3.1 User Interfaces
3.2 Hardware Interfaces  
3.3 Software Interfaces  
3.4 Communications Interfaces]  
4. System Features  
5. Other Nonfunctional Requirements
6. Other Requirements
   Comments

<hr />  


##### Product Name: Project Recommend
##### Description : A music player to recommend songs offline   
##### Status : Waiting for Review
##### Development Status  : Design phase

----

## Revisions

#### Latest Version
   Current Version : 1.0
   Current Status : Work in Progress
   Date : 18-09-2016





# 1. Introduction <a name="introduction"></a>
## 1.1 Purpose <a name="introduction-purpose"></a>
Here in this document we'll be discussing about the requirements and specifications, in a brief yet a precise manner, for a project known as "Project Recommend".

The various parts of our software are mentioned below:

- The back end of our software uses various libraries, mainly written in Python
- The programming language used is Python
- The libraries used for UI design
- Database used for music referencing and organization
- Classifiers used for classifying data and yielding recommendations


## 1.2 Document Conventions <a name="introduction-dc"></a>
- All terms are in italics style.
- Main features or important terms are in bold style.
- TBD means "To be Decided", these are the components that are not yet decided
- For more references see [Terminology](#introduction-terminology).

## 1.3 Intended Audience and Reading Suggestions <a name="introduction-iars"></a>
- Anyone with some basic knowledge of programming can understand this document. The document is intended for Developers, Software architects, Testers, Project managers and Documentation Writers.
But anyone with programming background and some experience with UML can understand this document.

- It is divided into 5 phases with sections 3, 4, 5 being intended for developers and software managers but other sections can be understood by anyone having little knowledge about software.

This Software Requirement Specification also includes:

- Overall description of the product
- External interface requirements
- System Features
- Other non functional requirements


## 1.4 Product Scope <a name="introduction-product-scope"></a>

- Talking about the research in the field of offline music recommendation, it is still not up to the mark, with only a very few papers published till now. Most of the music recommenders that are available are "online", but, here in this project, we will be building a music a recommender that will work with an internet connection that has a minimal speed(By minimal, I mean, the speed is not enough to play the music online, of a decent quality). The new music recommendations will be based on the familiar music taste of the listener, that is the kind of music(genre, artist, album etc.) he was previously listening to.

- Our software will be interfaced as a Desktop app, which will suggest music of similar kind as described above. the suggested songs might be available, in the user's offline music collection. if not, he can download them from the internet.

##### Advantages

There are various advantages that our software offers:

Mostly, the suggestions are from the offline collection. and it works with internet connections which are slow enough, and provide a low bandwidth. Since, it is not bounded by any particular music provider, any suggestion won't be limited to any particular service. We will be using the database of MusicBrainz, to update the metadata of the offline music collection of the user. This software can be used by anyone who wants recommendations on music and hence, audience of tis software is not limited.



## 1.5 References <a name="introduction- references"></a>
- This document is written in Markdown language, mostly, used on Github.

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
Our software will be implemented as a Desktop Application, and it will consist of the following components:

- **A Music player**:

This is a basic requirement for our software to work. This will be used to play/pause/stop/seek any sound track. This will be similar to any other music player that is available online.
- **Classifier**:

_Classifier_ is one of the most important components of this software, its job is to take in track's title and its metadata to provide suggestions, which may either be present offline or online.

- **Metadata updater**: _

Metadata updater_ is very similar to MusicBrainz's [Picard][picards-website] software. It takes a sound track or list of sound tracks as input and update their metadata information according to information available in [MusicBrainz database][musicbrainz-database-website]. This component needs internet for functioning.


#### Component Diagram
![Component_Diagram](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/Component_Dirgram_PR.jpg)


## 2.2 Product Functions <a name="od-pf"></a>
The following functions can be performed while using this software:
* You can use it like any other music player to play music.
* You can add/delete tracks.
* You can update the metadata of those tracks which lack the metadata.
* You can get music recommendations.      

## 2.3 User Classes and Characteristics <a name="od-ucc"></a>
To be specific, this software is meant for a music lover, especially those people who paly music in the background, while doing their own work, and since the only place where internet connection is required, is while updating the metadata. Hence, users with poor internet connection will be benefitted the most.


## 2.4 Operating Environment <a name="od-os"></a>

#### System Requirements

A few basic requirements are mentioned below:

* The operating system, that the user is currently using should be able to play music, and support a music player.

* Atleast a poor internet connection is required for metadata updation.  

#### Platforms Include


comments:

Rajdeep:
This product has nothing to do with bandwidth of the internet since we are not providing any download service for songs that we are suggesting. So essentially grounds of efficient bandwidth utilization has cannot be covered in the product perspective. product functions seems okay.


#### 2.4 <i>Operating Environment</i>

Talking about broader categories, our software will be compatible with  Windows and Linux based OSs.
1. Linux
<table>
<tr>
<td> <b>Criteria<b> </td><td><b>Requirements</b></td>
</tr>
<tr> <td>Operating system </td><td>Red Hat Enterprise Linux 4 or 5 with the latest patches and upgrades</td></tr>
<tr><td>CPU Type</td><td>Pentium 4 or higher; 2 GHz or higher</td> </tr>
<tr><td>Memory/RAM</td><td>1 GB minimum</td> </tr>
<tr><td>Hard Disk</td><td>4 GB minimum <td></tr>
</table>

2. Windows 7

 <table>
<tr>
<td> <b>Criteria</b> </td><td><b>Requirements</b></td>
</tr>
<tr> <td>Operating system </td><td>Windows 7</td></tr>
<tr><td>Processor</td><td>1 gigahertz (GHz) or faster 32-bit (x86) or 64-bit (x64) processor</td> </tr>
<tr><td>Memory/RAM</td><td>1 gigabyte (GB) RAM (32-bit) or 2 GB RAM (64-bit)</td> </tr>
<tr><td>Hard Disk</td><td>16 GB available hard disk space (32-bit) or 20 GB (64-bit)<td></tr>
</table>

----
comments:

Rajdeep: Operating Environment looks okay.


## 2.5 Design and Implementation Constraints <a name="od-di"></a>

For recommendations, we are using *content-based filtering* as this method uses the metadata of the songs (genre, mood, artist etc.), for suggestions.

We could have used *collaborative filtering* to recommend, but this requires user data in order to suggest music. Since, lack of user data is a limitation, this way could not be used to recommend music, as the training model won't have any training data available.  

Another way could have been *waveform analysis* where the wave is analyzed and classified into various categories such as pop, jazz, etc. , but this method is proved unusable due to lack of accuracy.   
## 2.6 User Documentation <a name="od-ud"></a>
* There will be a user manual which will explain the complete working of the software.
* Also, there will be a help option which will redirect the user to the website of our software.

## 2.7 Assumptions and Dependencies <a name="od-ad"></a>
TBD


# 3. External Interface Requirements <a name="eir"></a>

## 3.1 User Interfaces <a name="eir-ui"></a>

A python library, PyQt is used for the interface. The following diagram explains the major components of our software,.

#### UI Mockup
![](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/mockup.png)


## 3.2 Hardware Interfaces <a name="eir-hi"></a>
- Input device is needed for user to interact with system.
- Software needs a display device to interact with user.
- Music player needs playback device for sound output.
- Working Network Interface Card(NIC) for internet connectivity

## 3.3 Software Interfaces <a name="eir-si"></a>

TBD

## 3.4 Communications Interfaces <a name="eir-ci"></a>
- Internet Connection will be required by metadata updater, and classifier to communicate with the Musicbrainz API.
- Some kind of encryption will be used for the internet connection.
- Commonly used protocols will be HTTP/FTP.

# 4. System Features <a name="sf"></a>

Following is the use case diagram for the application
![use case diagram](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/final/images/PR_Use_case.jpg)

----


**Project Recommend** has the following set of system features



#### Local Store

The local store will use a SQL Database in order to store and organize music. Also, user can easily cache music into the local store and use it accordingly afterwards. The Local Store will be storing the the file path of the track, whether the track has been correctly tagged or not, the MusicBrainz track id and the id of the track. In case of the removal of the song from the app, that particular song will also be deleted from the local store.


#### Music player

This is the basic part of our software. Like any other music player, this will be used to play/pause/stop/seek/shuffle music. The user will be able to import music from his offline music collection which may simply refer to a hard-drive or a flash memory. User can remove a track from imported music and that will remove the corresponding entry from Local Store


#### Classifier

Classifier is one of the major components of our software, which does the important task of suggesting the appropriate songs to the user. The classifier can be triggered in two ways. Firstly, if the user is listening to a particular song, classifier will automatically be triggered to find the next set of suggestions. Also, user can manually trigger the classifier, to find suggestions similar to the song that user will select himself.   

#### User actions

Various user actions are defined as under:

* __Music management__

This refers to the addition and deletion of the songs, to and from the offline music library.


* __Manual updation of metadata__

In case, the metadata is not updated of some of the songs, or no metadata exists, this will correct those.  

* __Manual recommendation of music__

user can select any track from his music library, to suggest similar music.

The direct actions that the user can take is as follows:

* Actor: User

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



# 5. Other Nonfunctional Requirements <a name="onr"></a>




## 5.1 Performance and safety Requirements
 Performance requirements means whether the system is fast enough to play the music without any shattering or buffering. System should also be robust enough to report errors in case of lack of internet connection, unsupported file types etc. For security, we basically deal with the scenario where there is not enough enough metadata of the song. In such cases we will use AcoustID fingerprint. This will rarely be used although. But to prevent such scenarios, metadata should manually be updated.   

## 5.2 Security Requirements

Here we will certainly use asymmetric encryption between the user and MusicBrainz(HTTP/TCL).

## 5.3 Software Quality Attributes

If the system triggers any event that hinders with the regular working of the OS, the quality of the system is under suspicion. But, we will make sure, nothing like this happens. The software will mostly work without any failures, along with existing peacefully with rest of the softwares.  

## 5.5 Business Rules

The software is an Open Source software. If anyone wants to contribute, he can place a request via Github. But, this software is NOT fOR SALE.


# 6. Other Requirements <a name="otherreq"></a>

TBD


### Comments:

**Raghav**

Good work! Make it more descriptive, if possible. Use case diagram explains the relationships in a perfect way.

**Shakthi**

Provides enough descriptive details regarding the software. Appears to be a good SRS.


**Saumya**

Product perspective explained well.

**Suraj Nath**

Description given in a very understanding and precise manner. Keep it up!

**Rajdeep**

Non-functional requirements could have been presented better, but, all in all, decent work.
