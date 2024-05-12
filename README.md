### Song Classification Machine Learning Model

---

#### Preamble:

Spotify released an API that reports the audio features of its songs, such as “tempo” or “energy”. Here, we will use these features of 50k randomly picked songs to predict the genre that the song belongs to.

---

#### Data:

The original dataset is contained in the file dataSet/musicData.csv. In this file, the first row represents the column headers. Each row after that represents data from one song.

The columns represent, in order (from left to right):

```
Column 1: unique Spotify ID of each song
Column 2: artist name
Column 3: song name
Column 4: popularity of the music (what percentage of users know about it, from 0 to 99%)
Column 5: acousticness (an audio feature) on a scale from 0 to 1
Column 6: danceability (an audio feature) on a scale from 0 to 1
Column 7: the duration of the music (in milliseconds)
Column 8: energy (an auditory feature) on a scale from 0 to 1
Column 9: instrumentality (an audio feature) on a scale from 0 to 1
Column 10: key of the song (in musical notation)
Column 11: liveness (an audio feature) on a scale from 0 to 1
Column 12: loudness (in dB relative to some threshold)
Column 13: mode of the song (musical)
Column 14: speechiness (an audio feature), on a scale from 0 to 1
Column 15: tempo (in beats)
Column 16: obtained date (when was this information obtained from Spotify)
Column 17: valence (an audio feature), on a scale from 0 to 1
Column 18: Genre of the song (there are 10 different genres, e.g. “Rock” or “Country”)
```

---

#### Some key challenges for this project:

- There is randomly missing data, e.g. some of the durations of some of the songs are missing, as well as some of the auditory feature values. There are not many missing values, but you have to handle them somehow, either by imputation or by removing the missing data in some reasonable way.
- The acoustic features are unlikely to be normally distributed.
- Some of the data is provided in string format, e.g. the key. This will need to be transformed into numerical data to be useful.
- Some of the data is provided in categorical format, e.g. mode. This will need to be dummy coded.
- The category labels of the genres will need to be transformed into numerical labels.
- As this is a multi-class classification (not just binary), you need to be careful – only if the predicted classification of a genre in the test set matches the actual genre of a song is the classification correct. In other words, there are many more ways to be wrong than to be right.
- Make sure not to normalize categorical values (like mode) for the purposes of doing dimensionality reduction.
- There might be information in the linguistic properties of artist and song, but you don’t have to include that you in your model.

Structure of the project

```bash
.
├── capstone_data_cleaning.ipynb (1)
├── capstone_dimension_reduction.ipynb (2)
├── classifications
│  ├── capstone_classification_lda_ds.ipynb (3)
│  └── reducedDataSets
│     ├── lda_training.csv (4)
│     ├── lda_x_testing.csv (5)
│     └── lda_y_testing.csv (6)
├── dataSet
│  └── musicData.csv (7)
├── LICENSE
├── poetry.lock
├── processed_dataset.csv (8)
├── project_spec_sheet.pdf
├── pyproject.toml
└── README.md
```

| Number | File Name                                              | Description                                                |
| ------ | ------------------------------------------------------ | ---------------------------------------------------------- |
| 1      | `capstone_data_cleaning.ipynb`                         | code for cleaning the dataset.                             |
| 2      | `capstone_dimension_reduction.ipynb`                   | code for dimensionality reduction.                         |
| 3      | `classifications/capstone_classification_lda_ds.ipynb` | code for classification using the LDA dataset.             |
| 4      | `classifications/reducedDataSets/lda_training.csv`     | reduced dataset containing LDA components.                 |
| 5      | `classifications/reducedDataSets/lda_x_testing.csv`    | reduced dataset using the LDA method.                      |
| 6      | `classifications/reducedDataSets/lda_y_testing.csv`    | reduced dataset using the PCA method.                      |
| 7      | `dataSet/musicData.csv`                                | this is the original dataset.                              |
| 8      | `processed_dataset.csv`                                | this is the dataset I got after cleaning the original one. |
