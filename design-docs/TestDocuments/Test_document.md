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

### Description of Test Cases

| TEST_CASE | TEST_DATA | PRECONDITIONS | EXPECTED_RESULT |
|---|---|---|----|
| test_build | object of ManageLocalStorage | set connectionName | return True |
| test_query | song path | database and table with filled row available| don't return 'Query Failed' |
| test_dump | database object | database available | return True |
| test_write | song metadata | database and table available | return True|
| test_read | song path | database and table with entries with predefined value | return True |
| test_update | song path | database and table with entries with predefined value | return True |
| test_delete | song ID | database and table with entries | return True|
| test_readMetaData | song path | object of ManageMetadataModule, SongPath | return True |
| test_writeMetaData | song path | preconditions of test_readMetaData | return True |
| test_getMetadataDict_fileValidity | dictionary of metadata | get metadata of sample song | return True |
| test_getMetadataDict_fileNotEmpty | length of dictionay of metadata |same as test_getMetadataDict_fileValidity | return True |

### Coverage Report
| Module Covered | Statements | Miss | Cover |
|---|---|---|---|---|
| **LocalStorageModule** | 56  |  1  |  98% |
| **ManageMetadataModule** | 34 | 3 | 91% |
