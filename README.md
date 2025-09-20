# **🎶 Spotify Songs Clustering with K-Means & DBSCAN**
## **📌 Project Overview**
This project separation Spotify tracks with unsupervision algorytms : DBSCAN and K-Means.
![data](images/PCA_projection_of_Spotify_data.png)
## **📂 Dataset**
Source: Kaggle
Link: https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset/data
Size: 114000 data
Features: numerical audio attributes (danceability, energy, acousticness, …), plus metadata (genre, popularity, explicit, duration_ms)
## **⚙️ Methods**
Preprocessing:
-  delete poems with missing data
-  change object columns to categories
-  delete unnecessary columns
-  make heatmaps
Dimensionality reduction:
CA (2D) and UMAP (2D) for visualization
Clustering:
- K-Means algotytm separation data for 6 similar size clusters. This speparation in my opision is nice, but unfortunatly K-Means alghorytm don't make outliers who in this case study are nessesary.
  
