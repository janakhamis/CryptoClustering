# Cryptocurrency Clustering with K-Means and PCA

## Overview

The goal of this project is to study and organize cryptocurrencies based on market data using clustering techniques, namely the K-Means algorithm. We refine and compare clustering findings to gain greater insights on bitcoin activities by employing scaled data and dimensionality reduction via Principal Component Analysis (PCA).

## Goals

1. Determine the optimal number of clusters (k) using the elbow method.
2. Cluster cryptocurrencies using the K-Means algorithm.
3. Apply PCA to reduce dimensionality and optimize clustering.
4. Compare clustering results from the original dataset and PCA-reduced data.

## Dataset

The analysis uses a cryptocurrency dataset that includes metrics such as:

- Price change percentage over 24 hours.
- Price change percentage over 7 days.
- Other relevant market indicators.

## Methodology

**Step 1**: Find the Best Value for k (Original Scaled Data)
1. Elbow Method: Compute inertia values for k in the range of 1 to 11.
2. Visualization: Plot the inertia values to identify the elbow point.
3. Optimal k: Determine the best value for k based on the plot.

**Step 2**: Cluster Cryptocurrencies (Original Scaled Data)
1. Initialize K-Means: Use the optimal k value.
2. Fit and Predict: Train the model on the scaled data and predict cluster labels.
3. Visualize: Create a scatter plot of two features, coloring points by cluster labels and adding cryptocurrency names for hover interactions.

**Step 3**: Optimize Clusters with PCA
1. Dimensionality Reduction: Reduce features to 3 principal components.
2. Explained Variance: Evaluate how much variance each component explains and compute the total explained variance.
3. Create PCA DataFrame: Include principal components and set cryptocurrency IDs as the index.

**Step 4**: Find the Best Value for k (PCA Data)
1. Elbow Method: Repeat the elbow method using PCA-reduced data.
2. Compare k Values: Identify and compare the best k value with the one from the original scaled data.

**Step 5**: Cluster Cryptocurrencies (PCA Data)
1. Initialize K-Means: Use the optimal k value from PCA data.
2. Fit and Predict: Train the model on PCA data and predict cluster labels.
3. Visualize: Create a scatter plot of principal components (PC1 vs. PC2), coloring points by cluster labels and adding cryptocurrency names for hover interactions.

**Step 6**: Visualize and Compare Results
1. Compare Elbow Curves: Create a composite plot to compare inertia plots from original scaled data and PCA data.
2. Compare Clustering Results: Create a composite plot to visualize clustering results from original scaled data and PCA-reduced data.

## Tools and Libraries
- Python Libraries: Pandas, Scikit-learn, hvPlot, Matplotlib.
- Clustering Algorithm: K-Means.
- Dimensionality Reduction: Principal Component Analysis (PCA).

## Questions Addressed
1. What is the optimal number of clusters (k) for the original scaled data and PCA data?
2. How does the explained variance of the PCA components impact clustering?
3. What is the effect of dimensionality reduction on clustering results?

## How to Run it 
1. Clone the repository:
    1. Open your terminal (Git Bash, Command Prompt, or any Git client).
    2. Use the cd command to navigate to the directory where you want to clone the repository.
    3. Run the following command to clone the repository: git clone link_provided
2. Ensure Pandas, Scikit-learn, hvPlot, and Matplotlib is installed on your machine.
   - Install Pandas using pip if it's not already installed (pip install pandas).
   - Install Scikit-learn using pip if it's not already installed (pip install scikit-learn).
   - Install hvPlot using pip if it's not already installed (pip install hvPlot).
   - Install Matplotlib using pip if it's not already installed (pip install matplotlib).
3. Open the cloned file in the Visual Studio Code:
   1. Go to file > Open Folder and navigate to the folder where you cloned the repository.
   2. Select the folder to open in VS code.
4. Run the Jupyter Notebook:
     1. Open the notebook file (Crypto_Clustering.ipynb) in VS code or Jupyter.
     2. Run the cells to perform the Analysis.

## Results and Insights

The project shows a detailed comparison of clustering performance before and after dimensionality reduction. It illustrates the trade-offs between feature richness and computing efficiency, providing a clearer picture of bitcoin market segmentation.