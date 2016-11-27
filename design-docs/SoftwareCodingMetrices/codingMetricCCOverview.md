
## Cyclomatic Complexity:

Parameter list:

| CC score	| Rank | Risk |
| --- | --- | --- |
| 1 - 5 | A | low - simple block |
| 6 - 10 | B | low - well structured and stable block |
| 11 - 20 | C |	moderate - slightly complex block |
| 21 - 30 | D | more than moderate - more complex block |
| 31 - 40 | E | high - complex block, alarming |
| 41+ |	F | very high - error-prone, unstable block |

| Block type | Letter |
| --- | --- |
| Function | F |
| Method | M |
| Class | C |

### File: Recommend\recommend\editMetadata_form.py
    C 11:0 Ui_EditMetaDataDialog - A (1)
    M 12:4 Ui_EditMetaDataDialog.setupUi - A (1)
    M 138:4 Ui_EditMetaDataDialog.retranslateUi - A (1)
### File: Recommend\recommend\main.py
    M 142:4 MainWindow.crawlFolder - B (10)
    M 250:4 MainWindow.playPauseHandler - B (8)
    M 269:4 MainWindow.stopHandler - A (4)
    M 224:4 MainWindow.loadSettings - A (3)
    M 309:4 MainWindow.durationChangedHandler - A (3)
    M 387:4 MainWindow.populateEditMetadataDialog - A (3)
    C 13:0 MainWindow - A (2)
    M 125:4 MainWindow.browseHandler - A (2)
    M 198:4 MainWindow.buildMediaPlaylistPathList - A (2)
    M 241:4 MainWindow.buildPlayList - A (2)
    M 303:4 MainWindow.mediaPlayerPositionChangedHandler - A (2)
    M 338:4 MainWindow.currentMediaChangedHandler - A (2)
    M 355:4 MainWindow.seekPosition - A (2)
    M 380:4 MainWindow.editMetadataHandler - A (2)
    F 481:0 main - A (1)
    M 14:4 MainWindow.__init__ - A (1)
    M 30:4 MainWindow.extraSetup - A (1)
    M 121:4 MainWindow.closeEvent - A (1)
    M 133:4 MainWindow.openAboutUrl - A (1)
    M 136:4 MainWindow.openGitHubUrl - A (1)
    M 139:4 MainWindow.openIssuesUrl - A (1)
    M 208:4 MainWindow.playlistViewDoubleClickHandler - A (1)
    M 214:4 MainWindow.saveSettings - A (1)
    M 279:4 MainWindow.prevHandler - A (1)
    M 282:4 MainWindow.nextHandler - A (1)
    M 287:4 MainWindow.volumeIncrHandler - A (1)
    M 292:4 MainWindow.VolumeDecrHandler - A (1)
    M 297:4 MainWindow.muteHandler - A (1)
    M 367:4 MainWindow.volumeChangedHandler - A (1)
    M 370:4 MainWindow.increaseVolume - A (1)
    M 375:4 MainWindow.decreaseVolume - A (1)
    M 430:4 MainWindow.buildMessageBox - A (1)
    C 438:0 MetadataDialog - A (1)
    M 439:4 MetadataDialog.__init__ - A (1)
    M 453:4 MetadataDialog.wireButtons - A (1)
    M 459:4 MetadataDialog.saveButtonHandler - A (1)
    M 476:4 MetadataDialog.cancelButtonHandler - A (1)
### File: Recommend\recommend\mainWindow.py
    C 11:0 Ui_MainWindow - A (1)
    M 12:4 Ui_MainWindow.setupUi - A (1)
    M 331:4 Ui_MainWindow.retranslateUi - A (1)
### File: Recommend\recommend\classifier\Recommendation.py
    M 32:4 Recommendation.FetchRelevantSong - A (2)
    C 26:0 Recommendation - A (1)
    M 28:4 Recommendation.__init__ - A (1)
    M 55:4 Recommendation.Predict - A (1)
### File: Recommend\recommend\classifier\ManageCacheModule.py
    M 62:4 ManageCache.ReadCache - A (4)
    M 88:4 ManageCache.WriteCache - A (4)
    M 33:4 ManageCache.buildCache - A (3)
    M 139:4 ManageCache.deleteCache - A (3)
    C 17:0 ManageCache - A (2)
    M 125:4 ManageCache.dumpCache - A (2)
    M 19:4 ManageCache.__init__ - A (1)
    M 27:4 ManageCache.getConnectionName - A (1)
    M 30:4 ManageCache.setConnectionName - A (1)
    M 122:4 ManageCache.InvalidateCache - A (1)
### File: Recommend\recommend\classifier\cluster\raw_metadata.py
    F 4:0 getRawMetadata - A (3)
### File: Recommend\recommend\classifier\cluster\algorithms\KMeans.py
    M 73:4 kMeansClustering.get_common_phrases - B (6)
    M 100:4 kMeansClustering.get_clusters - A (3)
    F 121:0 main - A (2)
    C 24:0 kMeansClustering - A (2)
    M 41:4 kMeansClustering.find_clusters - A (2)
    M 93:4 kMeansClustering.print_common_phrases - A (2)
    M 115:4 kMeansClustering.print_clusters - A (2)
    M 29:4 kMeansClustering.__init__ - A (1)
### File: Recommend\recommend\classifier\cluster\preprocessing\tokenize_and_stem.py
    F 8:0 tokenize_and_stem - B (10)
### File: Recommend\recommend\LocalStorage\AccessLocalStorageModule.py
    M 25:4 AccessLocalStorage.read - A (4)
    M 70:4 AccessLocalStorage.write - A (4)
    M 128:4 AccessLocalStorage.update - A (4)
    C 11:0 AccessLocalStorage - A (3)
    M 112:4 AccessLocalStorage.delete - A (3)
    M 12:4 AccessLocalStorage.__init__ - A (1)
### File: Recommend\recommend\LocalStorage\ManageLocalStorageModule.py
    M 24:4 ManageLocalStorage.build - A (3)
    C 8:0 ManageLocalStorage - A (2)
    M 64:4 ManageLocalStorage.dump - A (2)
    M 80:4 ManageLocalStorage.query - A (2)
    M 9:4 ManageLocalStorage.__init__ - A (1)
### File: Recommend\recommend\Metadata\loloLyrics.py
    F 9:0 getLyrics - A (3)
### File: Recommend\recommend\Metadata\LyricsAndMetaData.py
    M 165:4 EditMetadata.removeTag - B (8)
    M 207:4 EditMetadata.addTag - B (8)
    M 242:4 EditMetadata.fetchTag - B (8)
    C 86:0 EditMetadata - A (4)
    M 68:4 EditLyrics.writeLyrics - A (3)
    M 35:4 EditLyrics.ifLyrics - A (2)
    M 264:4 EditMetadata.writeTag - A (2)
    C 28:0 EditLyrics - A (1)
    M 29:4 EditLyrics.__init__ - A (1)
    M 48:4 EditLyrics.removeLyrics - A (1)
    M 56:4 EditLyrics.addLyrics - A (1)
    M 63:4 EditLyrics.fetchLyrics - A (1)
    M 87:4 EditMetadata.__init__ - A (1)
    M 291:4 EditMetadata.populateMetadict - A (1)
### File: Recommend\recommend\Metadata\ManageMetaDataModule.py
    C 6:0 ManageMetaData - A (1)
    M 7:4 ManageMetaData.__init__ - A (1)
    M 24:4 ManageMetaData.ReadMetaData - A (1)
    M 50:4 ManageMetaData.WriteMetaData - A (1)
### File: Recommend\recommend\Metadata\tagsReadMetadata.py
    F 46:0 getMetadataDict - B (10)
    F 96:0 metaDataDictToUnicode - A (2)
### File: Recommend\recommend\musicplayer\ControlMusic.py
    C 1:0 ControlMusic - A (1)
    M 3:4 ControlMusic.__init__ - A (1)
    M 7:4 ControlMusic.add - A (1)
    M 11:4 ControlMusic.remove - A (1)
    M 16:4 ControlMusic.query - A (1)
    M 20:4 ControlMusic.ManuallyGet### File: Recommendation - A (1)
    M 23:4 ControlMusic.ResetAll - A (1)
### File: Recommend\recommend\musicplayer\ManageSongs.py
    C 1:0 MangaeSongs - A (1)
    M 3:4 MangaeSongs.__init__ - A (1)
    M 7:4 MangaeSongs.TriggerPlaySequence - A (1)
    M 10:4 MangaeSongs.Play - A (1)
    M 13:4 MangaeSongs.PlaySong - A (1)
    M 16:4 MangaeSongs.Pause - A (1)
    M 19:4 MangaeSongs.Next - A (1)
    M 22:4 MangaeSongs.Prev - A (1)
    M 25:4 MangaeSongs.Seek - A (1)
    M 28:4 MangaeSongs.Stop - A (1)
    M 31:4 MangaeSongs.VolControl - A (1)
