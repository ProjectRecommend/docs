## CS301  Software Engineering Project

**Requirements Traceability Matrix (RTM) Document**

**Version: 1.0**

**Date: 15/09/2016**

**Prepared by: Saumya Gupta**

**Project Name : Music Recommendation System **

**Project Description :** A music player that in addition to playing music, recommends user with music
similar to what he/she is listening from the offline as well as online music database. Also it updates
the metadata of user's offline music library files.


## ID Definitions

#### Requirement ID

1. R_01: Manage songs (adding/removing songs to/from the application).
2. R_02: Control music (play/pause/stop/seek music, go to previous/next track, increase /decrease/mute music volume).
3. R_03: Manually update metadata.
4. R_04: Manually recommend music.
5. R_05: Edit fields in the song info.

#### Test Scenario ID

1. TS_01: File doesn't have a music file extension/ or has the extension that the player doesn't support (acceptable extensions - .mp3, .wav etc.)
2. TS_02: User starts a gaming application or any other application which plays a sound in the background while listening to a song on the music player.
3. TS_03: User gets a call or message while listening to a song on the music player.
4. TS_04: The music file playing doesn't have sufficient metadata for the metadata updater to work.
5. TS_05: User removes the song which is playing currently.
6. TS_06: No internet connection available for connecting to MusicBrainz database online MusicBrainz returns error.
7. TS_07: The particular music file doesn't have sufficient metadata for the metadata updater to work.
8. TS_08: User removes song while updation.
9. TS_09: User closes software w/o saving data.


#### Test Case ID's

1. TC_01: Open software.
2. TC_02: Click on Add Music music option.
3. TC_03: Add file with wrong extension.
4. TC_04: Click on Play music option.
5. TC_05: Start a gaming application or any other application which plays a sound in the background.
6. TC_06: Receive a call or message.
7. TC_07: Click on Update Metadata.
8. TC_08: Click on Edit music data option.
9. TC_09: Type data in the given fields.
10. TC_10: Don't click on Save.
11. TC_11: Click on Close.
12. TC_12: Click on Remove music option.
13. TC_13: Get recommendations.
14. TC_14: Info updated.
15. TC_15: Click on Get Recommendations option.


## Requirements Traceability Matrix


| ID | Status | Test Scenario ID | Test Case ID | Verification | Additional Comments |
| --- | --- | --- | --- | --- | --- |
| R_01 | In Progress | TS_01 | TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_03|Failed | |
|R_02|In Progress|TS_02|TC_01|Passed| |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_04|Passed | |
| |In Progress||TC_13|Passed | |
| |In Progress||TC_05|Passed | |
| |In Progress|TS_03|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_04|Passed | |
| |In Progress||TC_13|Passed | |
| |In Progress||TC_06|Passed | |
| |In Progress|TS_04|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_04|Passed | |
| |In Progress||TC_13|Failed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_05|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_04|Passed | |
| |In Progress||TC_12|Passed | |
| |In Progress||TC_13|Failed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_06|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_04|Passed | |
| |In Progress||TC_13|Failed | |
| |In Progress||TC_14|Failed | |
|R_03| In Progress|TS_06|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_07|Passed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_07|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_07|Passed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_08|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_07|Passed | |
| |In Progress||TC_14|Failed | |
| |In Progress||TC_12|Passed | |
|R_04 |In Progress|TS_06|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_15|Passed | |
| |In Progress||TC_13|Failed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_07|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_15|Passed | |
| |In Progress||TC_13|Failed | |
| |In Progress||TC_14|Failed | |
| |In Progress|TS_08|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_15|Passed | |
| |In Progress||TC_12|Passed | |
| |In Progress||TC_14|Failed | |
| |In Progress||TC_13|Failed | |
|R_05 |In Progress|TS_09|TC_01|Passed | |
| |In Progress||TC_02|Passed | |
| |In Progress||TC_08|Passed | |
| |In Progress||TC_09|Passed | |
| |In Progress||TC_10|Passed | |
| |In Progress||TC_11|Passed | |
| |In Progress||TC_14|Failed | | |
