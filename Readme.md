# Wine Quality Mining

- Data Warehousing and Data Mining Project

## Project Objective

The project focuses on:

- understanding the structure and behavior of the wine dataset
- performing common preprocessing steps
- predicting wine quality categories using classification algorithms
- discovering hidden wine groups using clustering techniques
- comparing model behavior and interpreting results

## Dataset

- Dataset used: `winequality-red.csv`
- Location: [data/raw/winequality-red.csv](E:/Rough/DWDM_Project/Wine-Quality-Mining/data/raw/winequality-red.csv)
- Total columns: 12
- Target column: `quality`
- Input features: physicochemical properties such as acidity, chlorides, sulphates, alcohol, pH, density, and sulfur dioxide measures

## Project Workflow

The project is divided into four major stages:

1. **Exploratory Data Analysis**
   - inspect dataset shape, data types, and summary statistics
   - analyze missing values, duplicates, and outliers
   - study quality distribution and feature relationships
   - generate EDA plots

2. **Preprocessing**
   - check missing values
   - remove duplicate rows
   - handle outliers
   - apply feature scaling
   - save processed datasets

3. **Classification**
   - treat `quality` as a multiclass target
   - split data into training and testing sets
   - train and compare classifiers
   - evaluate using accuracy, classification report, and confusion matrix
   - save the best trained model

4. **Clustering**
   - remove `quality` during clustering
   - standardize features
   - apply K-Means clustering
   - choose the best number of clusters using inertia and silhouette score
   - visualize clusters using PCA

## Notebooks

- [01_EDA.ipynb](E:/Rough/DWDM_Project/Wine-Quality-Mining/notebooks/01_EDA.ipynb)
  Performs exploratory data analysis and generates plots for distribution, outliers, feature relationships, and correlation.

- [02_Preprocessing.ipynb](E:/Rough/DWDM_Project/Wine-Quality-Mining/notebooks/02_Preprocessing.ipynb)
  Performs common preprocessing steps and saves cleaned and scaled datasets.

- [03_Classification.ipynb](E:/Rough/DWDM_Project/Wine-Quality-Mining/notebooks/03_Classification.ipynb)
  Performs multiclass classification, compares models, saves the best model, reloads it, and predicts a sample wine.

- [04_Clustering.ipynb](E:/Rough/DWDM_Project/Wine-Quality-Mining/notebooks/04_Clustering.ipynb)
  Performs K-Means clustering, cluster selection analysis, PCA visualization, and clustered data export.

## Models and Techniques Used

### Classification

- Logistic Regression
- K-Nearest Neighbors
- Random Forest

### Clustering

- K-Means Clustering
- PCA for 2D visualization

### Evaluation

- Accuracy
- Classification Report
- Confusion Matrix
- Inertia
- Silhouette Score

## Important Outputs

### Processed Data

- [winequality_cleaned.csv](E:/Rough/DWDM_Project/Wine-Quality-Mining/data/processed/winequality_cleaned.csv)
- [winequality_scaled.csv](E:/Rough/DWDM_Project/Wine-Quality-Mining/data/processed/winequality_scaled.csv)
- [winequality_clustered.csv](E:/Rough/DWDM_Project/Wine-Quality-Mining/data/processed/winequality_clustered.csv)

### Saved Model

- [best_classification_model.pkl](E:/Rough/DWDM_Project/Wine-Quality-Mining/models/best_classification_model.pkl)

### Plots

- EDA plots:
  - [quality_distribution.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/Eda/quality_distribution.png)
  - [feature_distributions.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/Eda/feature_distributions.png)
  - [feature_boxplots.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/Eda/feature_boxplots.png)
  - [feature_vs_quality_boxplots.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/Eda/feature_vs_quality_boxplots.png)
  - [correlation_heatmap.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/Eda/correlation_heatmap.png)

- Classification plots:
  - [confusion_matrix_best_model.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/classification/confusion_matrix_best_model.png)

- Clustering plots:
  - [cluster_selection_metrics.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/clustering/cluster_selection_metrics.png)
  - [kmeans_pca_clusters.png](E:/Rough/DWDM_Project/Wine-Quality-Mining/plots/clustering/kmeans_pca_clusters.png)

## Project Structure

```text
Wine-Quality-Mining/
├─ data/
│  ├─ raw/
│  └─ processed/
├─ models/
├─ notebooks/
│  ├─ 01_EDA.ipynb
│  ├─ 02_Preprocessing.ipynb
│  ├─ 03_Classification.ipynb
│  └─ 04_Clustering.ipynb
├─ plots/
│  ├─ Eda/
│  ├─ classification/
│  └─ clustering/
├─ requirements.txt
└─ Readme.md
```

## How to Run

1. Open the project in the same virtual environment used for this repository.
2. Run the notebooks in order:
   - `01_EDA.ipynb`
   - `02_Preprocessing.ipynb`
   - `03_Classification.ipynb`
   - `04_Clustering.ipynb`
3. Check the generated outputs in:
   - `data/processed`
   - `plots`
   - `models`