### Capstone project: Spotify dataset classification. Machine Learning, Spring 2024

### Yan Konichshev; yk2602

---

Structure of the project and the files I am going to be referring to throughout the report:

```bash
.
├── capstone_data_cleaning.ipynb (1)
├── capstone_dimension_reduction.ipynb (2)
├── classifications
│  ├── capstone_classification_intersection_ds.ipynb (3)
│  ├── capstone_classification_lda_ds.ipynb (4)
│  ├── capstone_classification_pca_ds.ipynb (5)
│  └── reducedDataSets
│     ├── intersection_reduced.csv (6)
│     ├── lda_reduced.csv (7)
│     └── pca_reduced.csv (8)
├── dataSet
│  └── musicData.csv (9)
├── LICENSE
├── poetry.lock
├── processed_dataset.csv (10)
├── project_spec_sheet.pdf
├── pyproject.toml
└── README.md
```

| Number | File Name                                       | Description                                                           |
| ------ | ----------------------------------------------- | --------------------------------------------------------------------- |
| 1      | `capstone_data_cleaning.ipynb`                  | code for cleaning the dataset.                                        |
| 2      | `capstone_dimension_reduction.ipynb`            | code for dimensionality reduction.                                    |
| 3      | `capstone_classification_intersection_ds.ipynb` | code for classification using the intersection dataset.               |
| 4      | `capstone_classification_lda_ds.ipynb`          | code for classification using the LDA dataset.                        |
| 5      | `capstone_classification_pca_ds.ipynb`          | code for classification using the PCA dataset.                        |
| 6      | `intersection_reduced.csv`                      | reduced dataset using the intersection variables between PCA and LDA. |
| 7      | `lda_reduced.csv`                               | reduced dataset using the LDA method.                                 |
| 8      | `pca_reduced.csv`                               | reduced dataset using the PCA method.                                 |
| 9      | `musicData.csv`                                 | this is the original dataset.                                         |
| 10     | `processed_dataset.csv`                         | this is the dataset I got after cleaning the original one.            |

---

Beggining of the report.

#### A: how I build my model?

#### B: how I made my design choices?

#### C: how I handled challenges imposed by the dataset?

#### D: visualizations of ROC curves, clusterings

#### E: the most important factor underlying my classification success

<figure>
  <img src="pics/fig1.png" alt="Fig. 1.1 - Confusion marix for perceptron" height="300">
  <figcaption>Fig. 1.1 - Confusion marix for perceptron</figcaption>
</figure>

---

End of the report.
