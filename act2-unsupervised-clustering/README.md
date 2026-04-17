# Activity 2: Unsupervised Clustering

## Objective

Understand the characteristics of unsupervised clustering techniques based on distances (k-means) and densities (DBSCAN), and apply them to a synthetic dataset with complex geometric structures.

## Dataset Description

The synthetic dataset has the following characteristics (similar to Figure 1 in the statement):
- Two concentric circles with random thickness
- Three additional circles also with random thickness
- Some of these circles intersect each other
- Six compact blocks (small circles acting as dense blobs) distributed among the previous circles

## Exercises

The activity is developed in a Jupyter notebook and consists of the following exercises:

1. **Dataset generation and visualization** - Generate a synthetic dataset with the described characteristics (without using labels) and visualize it.
2. **k-means clustering** - Train a k-means model on the dataset, justifying the optimal number of clusters (e.g., using elbow method or silhouette score).
3. **DBSCAN clustering** - Train a DBSCAN model on the dataset, justifying the hyperparameters (eps and min_samples) based on the data characteristics.
4. **Discussion** - Briefly discuss the results and determine which approach (k-means or DBSCAN) is more appropriate for this dataset, supporting the judgment with images obtained from the tests.

## Files

- `gcd_aa2_act2_alex_rubino.ipynb` - Main Jupyter notebook (in Spanish)

## Language

The notebook is written in Spanish, as required by the course activity.

## Usage

This code is for educational purposes as part of the Machine Learning 2 course.
Feel free to explore and learn from it.