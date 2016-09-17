# Software Requirements Specification

##### Approved Version 1.0
<< Annotated Version >><br>

## <u> Project Recommend <u>
(An offline/online music recommendation system)
<br>

### *Prepared by :* __Pranshu Sahijwani__

<p>Submitted in partial fulfillment of the requirements of our course <br> *CS301 Software Engineering*.</p>




### 1.0. **Introduction**

#### 1.1. *Purpose*

<p>The purpose of this SRS document is to provide a detailed description of this project.  This information includes its features, interfaces, working etc. This will also explain the overall purpose of this project in a detailed yet precise manner. This document can be used by both the *developers* and *users* of this software.</p>     

#### 1.2. *Document Conventions*

<p>Anything written within these doubly square brackets is won’t be a part of this SRS, but will be used to inrease the readability of the person reading this, and also will provide a better explanation of the point being made. </p>


#### 1.3. *Intended Audience And Reading Suggestions*

<p> The audience of this software could be anyone who wants music recommendations while listening music. And this document can be referred to by its writers, testers, users, developers. </p>

#### 1.4. *Product Scope*

<p> This software is designed in such a way, that it will improve the user experience drastically, as the music of his choice will be automatically queued up in his current playlist, depending on his taste in music, or the kind of music he has been listening to recently. The software after being installed will automatically update the metadata(song artist, genre of the song, album etc.) of the music in his offline music library, in a very short period of time, which otherwise had to be updated manually. After updating the metadata the software will start its work of recommendation. Hence, it will sufficiently enhance the productivity/efficiency of a normal music player, along with being easy to use and maintain.</p>

<p> The scope of this software basically covers every user, who doesn't want to update the metadata of the songs in his offline music library, who doesn't want to decide manually which track to play next, who believes in listening to some random music similar to his taste. </p>

#### 1.5. *References*
<p> to be added later. </p>

### 2.0 **Overall Description**
#### 2.1. *Product Perspective*
<p> India currently is a country where the internet speed is not up to the mark at many places, with only 2g spectrum, covering most of the regions. The recommendation systems that exist already recommend music, but that has to be played online, and these require a decent internet speed to play a particular song at decent bitrate, which is many a times not possible with 2g data speed. So, our idea is, basically, to use the offline music  of a user, to play music. Of course, 2g network can be used to recommend songs(fetching those from Musicbrainz API, in our case), but those songs will be played from the user's local music collection, hence minimizing the need of using 2g data in order to play music, of decent quality.
Sometimes, it might happen the ID3 tags of a few songs are not updated. One part of our software (metadata updater), will update the metadata of the songs whose metadata is not fully updatedor does not exist.
This was the context of our software. This will replace those systems that are solely dependent on reliable internet speed, and will provide the benefit of music recommendations to those, who are bound in the regions covered under 2g/GPRS spectrums.
 </p>

 #### 2.2. *Product Functions*
 The basic functions of this offline music recommender system can be summarized under:
 <ul>
<li>Automatically updating <u>ID3 tags</u> of existing music existing on local storage.</li>
<li> Recommending songs based on the music taste of the user.</li>

</ul>

#### 2.4 *Operating Environment*
Talking about broader categories, our software will be compatible with  Windows and Linux based OSs.
1. Linux
<table>
<tr>
<td> **Criteria** </td><td>**Requirements**</td>
</tr>
<tr> <td>Operating system </td><td>Red Hat Enterprise Linux 4 or 5 with the latest patches and upgrades</td></tr>
<tr><td>CPU Type</td><td>Pentium 4 or higher; 2 GHz or higher</td> </tr>
<tr><td>Memory/RAM</td><td>1 GB minimum</td> </tr>
<tr><td>Hard Disk</td><td>4 GB minimum <td></tr>
</table>

2. Windows 7

 <table>
<tr>
<td> **Criteria** </td><td>**Requirements**</td>
</tr>
<tr> <td>Operating system </td><td>Windows 7</td></tr>
<tr><td>Processor</td><td>1 gigahertz (GHz) or faster 32-bit (x86) or 64-bit (x64) processor</td> </tr>
<tr><td>Memory/RAM</td><td>1 gigabyte (GB) RAM (32-bit) or 2 GB RAM (64-bit)</td> </tr>
<tr><td>Hard Disk</td><td>16 GB available hard disk space (32-bit) or 20 GB (64-bit)<td></tr>
</table>
