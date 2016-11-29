<div align=center>
  <h1>Test Document</h1>
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


## WhiteBox Testing
## Unit Tests  
|TEST_CASE|FUNCTION|RESULT|
|---|----|----|
| test_build | ManageLocalStorage.build| *PASSED* |
| test_query | ManageLocalStorage.query| *PASSED* |
| test_dump | ManageLocalStorage.def dump| *PASSED* |
| test_write | AccessLocalStorage.write| *PASSED* |
| test_read | AccessLocalStorage.read| *PASSED* |
| test_update | AccessLocalStorage.update| *PASSED* |
| test_delete | AccessLocalStorage.delete| *PASSED* |
| test_readMetaData | ManageMetadataModule.ReadMetaData| *PASSED* |
| test_writeMetaData | ManageMetadataModule.WriteMetaData| *PASSED* |
| test_getMetadataDict_fileValidity | tagsReadMetadata.getMetadataDict | *PASSED* |
| test_getMetadataDict_fileNotEmpty | tagsReadMetadata.getMetadataDict | *PASSED* |
</br>

### Description of Test Cases

| TEST_CASE | TEST_DATA | PRECONDITIONS | EXPECTED_RESULT |
|---|---|---|----|
| test_build | object of ManageLocalStorage | set connectionName | return True |
| test_query | song path | database and table with filled row available| shouldn't return 'Query Failed' |
| test_dump | database object | database available | return True |
| test_write | song metadata | database and table available | return True|
| test_read | song path | database and table with entries with predefined value | return True |
| test_update | song path | database and table with entries with predefined value | return True |
| test_delete | song ID | database and table with entries | return True|
| test_readMetaData | song path | object of ManageMetadataModule, SongPath | return True |
| test_writeMetaData | song path | preconditions of test_readMetaData | return True |
| test_getMetadataDict_fileValidity | dictionary of metadata | get metadata of sample song | return True |
| test_getMetadataDict_fileNotEmpty | length of dictionay of metadata |same as test_getMetadataDict_fileValidity | return True |
</br>
### Coverage Report on modular level
| Module Covered | Statements | Miss | Cover |
|---|---|---|---|---|
| **LocalStorageModule** | 56  |  1  |  98% |
| **ManageMetadataModule** | 34 | 3 | 91% |

* Some Modules are not covered in testing due to structural complexity. Will be tested in future.

### Tools Used for Unit Testing
* *Nose2* Module
* *Unittest* Module

## BlackBox Testing
| ACTION | PRECONDITIONS | DESIRED_OUTPUT | OUTPUT | RESULT |
|---|---|---|---|---|
|Import Folder containing MP3 files having proper ID3 tagging| No existing database | Create database, create list of files in database, Load MP3 files into playlist | Database created, Tracks loaded | PASSED |
|Import Folder containing MP3 files having proper ID3 tagging| database exist with different entries | Update database, insert list of files into database, Load MP3 files into playlist | Database updated, Tracks loaded | PASSED |
| Import folder containing Mixed format files| NONE | Load MP3 files into playlist | ERROR - window closes, Program stops | FAILED|
|Import Folder containing MP3 files only but with improper ID3 tagging| NONE |Load MP3 files into playlist|ERROR - window closes, Program stops| FAILED |
| Delete the track after loading it into playlist and then restart the application | Import Folder containing MP3 files having proper ID3 tagging | Changes should reflect in playlist | ERROR - window closes, Program stops | FAILED |
| Play song | Load songs into playlist | Song starts playing with sound output, Seek bar shows total duration of song and  passed duration with moving graphics. | As desired | PASSED |
| Change volume | Play song | Volume should go up on moving the graphical volume level up and vice verse with level display in digits | As desired | PASSED |

* Some tests are remaining and will be done soon.

## Inference  
* Application is designed to meet the basic requirements.
* It lacks robustness.
* Less portable and scalable due to poor exception handling.
