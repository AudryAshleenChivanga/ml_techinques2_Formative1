# Clustering Unlabeled Sound Data

## Project Overview

This project applies clustering techniques to an unlabeled sound dataset to uncover meaningful groupings within the data. It involves extracting Mel spectrogram features, visualizing high-dimensional data, performing dimensionality reduction, and comparing clustering algorithms.

## Key Steps

1. **Feature Extraction**  
   Extracted Mel spectrogram features from raw sound files to represent audio characteristics in a 128-dimensional feature space.

2. **Visualization Without Dimensionality Reduction**  
   Used scatter and pair plots on a small subset of features to explore data structure, revealing challenges in visualizing high-dimensional data.

3. **Dimensionality Reduction**  
   Applied PCA and t-SNE to reduce feature dimensionality to 3 components for better visualization and clustering. Found t-SNE to provide better cluster separability.

4. **Clustering Methods**  
   Implemented K-Means and DBSCAN clustering algorithms on t-SNE reduced features. Optimized K-Means cluster count using the elbow method and evaluated clusters using Silhouette Score and Davies-Bouldin Index.

5. **Evaluation and Analysis**  
   Compared clustering performance and interpretability, concluding that K-Means performed better on this dataset due to the nature of the data and cluster shapes.

## Results

- **K-Means** achieved a Silhouette Score of 0.3632 and a Davies-Bouldin Index of 0.9808, indicating fairly compact and well-separated clusters.  
- **DBSCAN** had a lower Silhouette Score of 0.2876 and a higher Davies-Bouldin Index of 1.0922, showing less defined clusters.  
- Visualizations confirmed K-Means produced clearer cluster groupings compared to DBSCAN.

## Final Thoughts

Dimensionality reduction was crucial in revealing meaningful structures in this high-dimensional sound data, improving clustering outcomes. Choosing the right clustering algorithm depends on the data distribution: K-Means worked better here due to compact cluster shapes, while DBSCAN struggled due to uniform density.

This project highlights common real-world challenges in clustering, including handling high-dimensional noisy data and selecting appropriate methods.

## How to Run

1. Ensure you have the required libraries installed (`librosa`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `tqdm`).  
2. Place the unlabeled sound `.wav` files in the specified data folder.  
3. Run the notebook cells sequentially to reproduce feature extraction, visualization, dimensionality reduction, clustering, and evaluation.

## Acknowledgements

Thanks to the sound data provider and open-source libraries that made this project possible.

## Author 

Audry Ashleen Chivanga
