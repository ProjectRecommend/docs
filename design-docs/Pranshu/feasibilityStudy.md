# <u>Feasibility Study</u> - **Project Recommend**

A system is considered to be a decent one, if it performs up to the expectations. When we carry out a feasibility study for any software, that is under development, we need to make sure that, our final product is feasible, both economically as well as technically.  
<p>
A feasibility study report basically covers the following points:-
<ol>
<li> Analysis of the problem which led to the development of the software.</li>
<li> The constraints that developers have to deal with.</li>
<li> Results of the surveys carried out to test the feasibility.</li>
<li> Checking if our product is economically feasible.</li>

</ol>


### Analysis of the problem

<p>India currently is a country where the <i>internet speed</i> is not up to the mark at many places, with only 2g spectrum, covering most of the regions.
Sometimes, while listening to music, switching to a song of similar taste manually, from his/her whole collection of music.  
The recommendation systems that exist already, do recommend music, but that has to be played online, and these require a decent internet speed to play a particular song at decent bitrate, which is many a times not possible with 2g data speed. So, our idea is, basically, to use the offline music collection of a user, to play music. Of course, 2g network can be used to recommend songs(fetching those from Musicbrainz API, in our case), but those songs will be played from the user's local music collection, hence minimizing the need of using 2g data in order to play music, of good quality. <br>
Sometimes, it might happen the ID3 tags of a few songs are not updated. One part of our software (metadata updater), will update the metadata of the songs whose metadata is either not fully updated or does not exist.
This will replace those systems that are solely dependent on reliable internet speed, and will provide the benefit of music recommendations to those, who are bound in the regions covered under 2g/GPRS spectrum.
