<div align=center>
  <h1>Sophistication</h1>
  <h2>Project Recommend</h2>
  <b> Music Recommendation System </b><br />
</div><br /><br />

# Purpose Of The Document

Here, we are going to discuss what all parameters we have considered while building our product and how many parameters we have been able to cover actually. Our software involves cutting - edge unsupervised machine learning concepts such as k-means clustering and natural language processing (NLP).

We promised our customers that we will be building a simple music player (which has basic features like play, pause, stop, seek, Vol. up, Vol. down, add music, see lyrics, see and edit metadata of a particular track and so on..), which will allow you to add a set of songs from your offline music collection to a _playlist_, will fetch recommendations using the _Musicbrainz_ API (online) and from your local music collection (offline), and will accordingly populate two sections (both of which occupy the right side of UI). If a song, which is in online recommended section, has a download link attached to it, the user can download that track, there and then, else can download that manually from any other place. On the other hand, those in the offline recommended section can be added to the _playlist_.

According to whatever has been mentioned above, we have been successfully able to build our software, which meets all the requirements.

# Modules And Functions Used

- From the module, **sklearn.feature_extraction.text**, we have imported _TfidfVectorizer_ (Transforms text to feature vectors that can be used as input to estimator.).

- From **sklearn.cluster**, we have imported _KMeans_ (k-means clustering is a method of vector quantization, originally from signal processing, that is popular for cluster analysis in data mining.)

- From **nltk.tokenize**, we have imported _wordpunct_tokenize_.

-  From **nltk.stem.lancaster**, we are importing _LancasterStemmer_ (It is a fast algorithm which effectively reduces your huge set of words.)

# Taking Complexity into Account

Complexity Adjustment Values (F_i) are used on a scale of 0 (least important) to 5(most important):

1. Does the system require reliable backup and recovery?&nbsp;&nbsp;&nbsp; Value: **0**

2. Are data communication required?&nbsp;&nbsp;&nbsp;Value: **3**
3. Are there distributed processing functions?&nbsp;&nbsp;&nbsp;Value: **4**

4. Is performance critical?&nbsp;&nbsp;&nbsp;Value: **5**

5. System to be run in an existing, heavily utilized environment?&nbsp;&nbsp;&nbsp;Value: **3**

6. Does the system require on-line data entry?&nbsp;&nbsp;&nbsp;Value: **0**

7. On-line entry requires input over multiple screens or operations?&nbsp;&nbsp;&nbsp;Value: **0**

8. Are the master files updated on-line?&nbsp;&nbsp;&nbsp;Value: **0**

9. Are the inputs, outputs, files, or inquiries complex?&nbsp;&nbsp;&nbsp;Value: **3**

10. Is the internal processing complex?&nbsp;&nbsp;&nbsp;Value: **5**

11. Is the code designed to be reusable?&nbsp;&nbsp;&nbsp;Value: **5**

12. Are conversion and instillation included in the design?&nbsp;&nbsp;&nbsp;Value: **3**

13. Multiple installations in different organizations?&nbsp;&nbsp;&nbsp;Value: **0**

14. Is the application designed to facilitate change and ease-of-use?&nbsp;&nbsp;&nbsp;Value: **5**
