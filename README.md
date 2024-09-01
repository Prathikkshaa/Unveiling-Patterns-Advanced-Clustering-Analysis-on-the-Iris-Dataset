# Clustering Analysis on Iris Dataset

## Overview
This project explores clustering techniques on the Iris dataset to uncover patterns and groupings within the data. The Iris dataset, containing measurements of iris flowers, is used to perform KMeans clustering. The objective is to identify clusters of similar flowers and evaluate how well the clustering aligns with known species.

## Dataset
The Iris dataset consists of the following features:
- **Sepal Length**
- **Sepal Width**
- **Petal Length**
- **Petal Width**

The dataset is well-known for its balance among three Iris species: Setosa, Versicolor, and Virginica.

## Libraries Used
- **numpy**: For numerical operations and data handling.
- **pandas**: For data manipulation and loading.
- **plotly**: For interactive visualizations.
- **seaborn**: For statistical data visualizations.
- **sklearn**: For KMeans clustering and evaluation.

## Data Preparation
1. **Data Loading**: Imported the Iris dataset from a CSV file.
2. **Data Cleaning**: Removed the 'Id' column as it was not necessary for clustering.
3. **Feature and Label Separation**: Extracted features (`Sepal Length`, `Sepal Width`, `Petal Length`, `Petal Width`) and labels (species names) for analysis.

## Exploratory Data Analysis (EDA)
1. **Distribution Visualization**: Created a pie chart to visualize the distribution of Iris species. The data was well-balanced among the three species.
2. **Sepal Length Analysis**: 
   - **Box Plot**: Showed that Setosa had smaller Sepal Lengths compared to Virginica and Versicolor.
   - **Histogram**: Revealed distribution and overlapping regions among species.
3. **Sepal Width Analysis**: 
   - **Box Plot**: Indicated Setosa had a larger Sepal Width compared to the other species, while Versicolor had the smallest.
   - **Histogram**: Provided additional insights into Sepal Width distribution.
4. **Petal Length Analysis**: 
   - **Box Plot**: Demonstrated Setosa had much smaller Petal Lengths compared to Virginica and Versicolor.
   - **Histogram**: Highlighted overlapping regions among species.
5. **Petal Width Analysis**: 
   - **Box Plot**: Showed that Setosa had much smaller Petal Widths compared to Virginica and Versicolor, with some overlap between Virginica and Versicolor.
6. **Scatter Plots**: Visualized relationships between Sepal and Petal dimensions, color-coded by species, with varying sizes indicating additional features.

## Clustering Process
1. **Determining Optimal Clusters**: 
   - Used the elbow method to find the optimal number of clusters. Plotted the Sum of Squared Errors (SSE) against the number of clusters (1 to 8). The "elbow" in the plot suggested that 3 clusters were ideal.
2. **Applying KMeans**: 
   - Implemented KMeans clustering with `n_clusters=3`. The algorithm iteratively assigned data points to the nearest centroid and updated centroids until convergence.
3. **Evaluating Clusters**: 
   - Visualized the clustering results with scatter plots, color-coded by clusters. Included cluster centroids to show the center of each cluster.

## Insights and Observations
1. **Separation of Iris Species**: KMeans effectively clustered the Iris species based on their features, with Petal Length and Petal Width being particularly influential.
2. **Feature Importance**: Petal Length and Petal Width were crucial for distinguishing between species. Setosa was clearly separated due to its distinctively smaller Petal Length and Width.
3. **Cluster Visualization**: The visual representation of clusters and centroids showed how well the KMeans algorithm grouped the data and aligned with actual species labels.

## Files
- **`data/iris.csv`**: The Iris dataset in CSV format.
- **`preprocess.py`**: Script for loading and cleaning the dataset.
- **`eda.py`**: Script for performing exploratory data analysis and generating visualizations.
- **`clustering.py`**: Script for applying KMeans clustering and evaluating results.
- **`requirements.txt`**: Lists all dependencies required for the project.

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/iris-clustering-analysis.git
   cd iris-clustering-analysis
