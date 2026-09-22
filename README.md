# Spotify Songs' Genre Segmentation Using Clustering

## 📌 Project Overview

This project focuses on **unsupervised machine learning-based genre segmentation of Spotify songs** using clustering techniques.

The objective is to analyze the audio characteristics of Spotify songs, identify groups of musically similar tracks, and understand how songs are naturally organized into clusters based on their audio features and playlist information.

The project applies data preprocessing, exploratory data analysis, correlation analysis, clustering, cluster evaluation, visualization, and similarity-based recommendation.

---

## 🎯 Objectives

The main objectives of this project are:

* Perform data preprocessing and cleaning on Spotify song data.
* Analyze the distribution of song and playlist characteristics.
* Study relationships between numerical audio features.
* Identify meaningful groups of songs using clustering.
* Compare different clustering approaches.
* Determine an appropriate number of clusters.
* Analyze clusters according to playlist genres and playlist names.
* Visualize the resulting song clusters.
* Build a similarity-based song recommendation component.
* Prepare the clustering results for a future recommendation system.

---

## 📂 Project Structure

```text
Spotify-Genre-Segmentation/
│
├── spotify_clustering.py
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

The project uses a Spotify songs dataset containing song-level information such as:

* Track name
* Artist name
* Playlist name
* Playlist genre/subgenre
* Danceability
* Energy
* Loudness
* Speechiness
* Acousticness
* Instrumentalness
* Liveness
* Valence
* Tempo
* Duration
* Other available numerical audio characteristics

The dataset should be provided as:

```text
spotify_songs.csv
```

Place the dataset in the same working directory before executing the Python script.

---

## 🔄 Project Workflow

```text
Spotify Songs Dataset
        ↓
Data Loading
        ↓
Data Cleaning
        ↓
Missing Value Handling
        ↓
Duplicate Removal
        ↓
Feature Selection
        ↓
Feature Scaling
        ↓
Exploratory Data Analysis
        ↓
Correlation Analysis
        ↓
Determining Number of Clusters
        ↓
K-Means Clustering
        ↓
Hierarchical Clustering
        ↓
Cluster Evaluation
        ↓
PCA Visualization
        ↓
Genre & Playlist Cluster Analysis
        ↓
Similarity-Based Recommendation
```

---

## 🧹 Data Preprocessing

The preprocessing stage prepares the Spotify dataset for clustering.

The following operations are performed:

1. Load the Spotify dataset.
2. Remove duplicate records.
3. Convert numerical features into appropriate numeric formats.
4. Handle missing numerical values using median imputation.
5. Select relevant audio features.
6. Standardize numerical features using `StandardScaler`.

Feature scaling is important because Spotify audio features can have different numerical ranges. Standardization prevents features with larger numerical values from dominating the clustering process.

---

## 📈 Exploratory Data Analysis

The project performs exploratory analysis to understand the dataset before clustering.

The analysis includes:

* Dataset statistics
* Missing-value analysis
* Numerical feature distributions
* Box plots
* Genre distribution
* Subgenre distribution
* Playlist distribution
* Correlation matrix

These visualizations help identify data patterns, feature relationships, and possible outliers.

---

## 🔗 Correlation Analysis

A correlation matrix is generated to examine relationships between Spotify audio features.

The analysis helps identify relationships among features such as:

* Danceability
* Energy
* Loudness
* Acousticness
* Valence
* Tempo
* Instrumentalness
* Speechiness
* Liveness

The correlation heatmap provides a visual representation of the relationships between these features.

---

## 🤖 Clustering Methodology

This project uses **unsupervised learning** because the objective is to discover natural groups of songs rather than train a classifier using predefined target labels.

### K-Means Clustering

K-Means clustering is used to partition songs into groups based on their standardized audio characteristics.

The algorithm:

1. Selects the number of clusters.
2. Initializes cluster centroids.
3. Assigns each song to the nearest centroid.
4. Updates the centroid positions.
5. Repeats the process until convergence.

### Hierarchical Clustering

Agglomerative Hierarchical Clustering is also implemented to identify groups of similar songs.

The method starts with individual observations and progressively merges similar observations into larger groups.

---

## 🔢 Selecting the Number of Clusters

The project evaluates multiple possible values of `K`.

Silhouette analysis is used to examine how well observations fit within their assigned clusters.

The analysis helps identify a suitable cluster configuration before generating the final clustering result.

---

## 📏 Clustering Evaluation

The clustering results are evaluated using multiple unsupervised learning metrics.

### Silhouette Score

Measures how similar a song is to its own cluster compared with other clusters.

### Davies-Bouldin Index

Measures the average similarity between each cluster and its most similar cluster. Lower values indicate better separation.

### Calinski-Harabasz Score

Measures the ratio between between-cluster dispersion and within-cluster dispersion.

Using multiple evaluation metrics provides a broader view of cluster structure.

---

## 📊 Cluster Visualization

Principal Component Analysis (PCA) is used to reduce the dimensionality of the audio feature space for visualization.

The resulting clusters are displayed in a two-dimensional representation, making it easier to observe the separation and distribution of song groups.

---

## 🎵 Genre and Playlist Analysis

After clustering, the project analyzes the relationship between clusters and available playlist information.

The analysis includes:

* Cluster vs. playlist genre
* Cluster vs. playlist name
* Songs belonging to each cluster
* Cluster-level feature statistics

This helps understand which types of music are commonly grouped together based on their audio characteristics.

---

## 🎧 Similarity-Based Recommendation

The clustering output can be used as a foundation for a recommendation system.

For a selected song, the system identifies songs with similar feature representations and returns nearby tracks based on audio-feature similarity.

The recommendation process can be represented as:

```text
Selected Song
     ↓
Extract Audio Features
     ↓
Standardize Features
     ↓
Find Similar Songs
     ↓
Calculate Feature Similarity
     ↓
Return Recommended Songs
```

This provides a foundation for developing a more complete music recommendation system.

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* OpenPyXL
* Jupyter

### Machine Learning Techniques

* K-Means Clustering
* Agglomerative Hierarchical Clustering
* Principal Component Analysis (PCA)
* Feature Scaling
* Similarity-Based Recommendation

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/Raghavendra582/Spotify-Genre-Segmentation.git
```

Move into the project directory:

```bash
cd Spotify-Genre-Segmentation
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

Make sure `spotify_songs.csv` is available in the project directory.

Run:

```bash
python spotify_clustering.py
```

The script performs preprocessing, exploratory analysis, clustering, evaluation, visualization, and recommendation-related analysis.

---

## 📁 Output

The project generates analysis results including:

* Statistical summaries
* Missing-value analysis
* Distribution plots
* Box plots
* Correlation heatmap
* Genre and playlist analysis
* Cluster evaluation results
* PCA cluster visualization
* Cluster profiles
* Playlist-cluster analysis
* Final clustered song dataset
* Similar-song recommendations

---

## 🔮 Future Enhancements

The project can be extended in several ways:

* Develop an interactive recommendation interface.
* Integrate Spotify API data.
* Add real-time song recommendations.
* Experiment with DBSCAN and other clustering algorithms.
* Improve similarity-based recommendation techniques.
* Develop a web application using Flask or Streamlit.
* Add user-specific recommendation functionality.
* Deploy the recommendation system as a cloud application.

---

## 👨‍💻 Author

**K. Raghavendra**

### Project Title

**Spotify Songs' Genre Segmentation Using Clustering**

---

## 📜 License

This project is intended for educational and research purposes.
