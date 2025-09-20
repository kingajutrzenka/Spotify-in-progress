# **🎶 Spotify Songs Clustering with K-Means & DBSCAN**
## **📌 Project Overview**
This project separates Spotify tracks with unsupervised algorithms: DBSCAN and K-Means.  

<img src="images/PCA_projection_of_Spotify_data.png" width="600">

## **📂 Dataset**
- Source: Kaggle  
- Link: https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset/data  
- Size: 114,000 tracks  
- Features: numerical audio attributes (danceability, energy, acousticness, …), plus metadata (genre, popularity, explicit, duration_ms)  

## **⚙️ Methods**
**Preprocessing**:
- delete rows with missing data  
- change object columns to categories  
- delete unnecessary columns  
- make heatmaps  

**Dimensionality reduction**:  
PCA (2D) and UMAP (2D) for visualization  

**Clustering**:
- **K-Means algorithm** separated data into 6 similar-sized clusters. This separation in my opinion is nice, but unfortunately K-Means algorithm doesn't detect outliers, which in this case study are necessary.  
  <img src="images/KMeans.png" width="600">

- **DBSCAN algorithm** separated data into 19 different-sized clusters. This separation is worse than in K-Means algorithm, but this algorithm found 2,607 outliers, which in this case study is important.  
  <img src="images/DBSCAN.png" width="600">

### Comparison and conclusions:
#### DBSCAN vs K-Means

| Algorithm | Clusters | Outliers | Main insight |
|-----------|----------|----------|--------------|
| DBSCAN    | 19       | 2,607    | One huge mainstream cluster + smaller niches |
| K-Means   | 6        | –        | Balanced partitioning into large groups |

Probably the best option will be a mix: DBSCAN (for finding outliers) and K-Means (for data separation).  

## **🚀 Future Work**
- Try Gaussian Mixture Models (GMM) for probabilistic clustering.  
- Build a simple recommendation demo in Streamlit.  
