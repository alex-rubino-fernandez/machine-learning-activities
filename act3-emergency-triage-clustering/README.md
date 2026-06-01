# Activity 3: Preliminary Patient Classification in Emergency Department using Unsupervised Techniques

## Objective

Apply unsupervised learning techniques (k-means clustering and PCA) on a real-world emergency department dataset to identify clinical patient profiles. The goal is to support the JENNER & PHIPPS S.A. hospital group in improving triage efficiency, detecting classification errors, and optimizing resource management.

## Dataset Description

The dataset (`Actividades_gcd_aa2_act3_proy_4P_dataset.csv`) contains anonymized records of 1267 patients attended in emergency departments, with 24 variables including:
- Demographics (age, sex)
- Vital signs (systolic/diastolic blood pressure, heart rate, respiratory rate, body temperature, oxygen saturation)
- Clinical assessment (pain scale NRS, mental status, injury presence)
- Triage information (KTAS level by nurse and expert, mistriage indicator)
- Outcome variables (disposition, length of stay)

The data comes from two different hospitals (Local and Regional), which introduces structural patterns relevant to the analysis.

## Exercises

The activity is developed in a Jupyter notebook and consists of the following exercises:

1. **Data loading and cleaning** - Identify and correct errors or anomalies in numerical variables. Impute, remove, or justify decisions on missing values and incorrect encodings. Includes RandomForest imputation for oxygen saturation (validated with MAE=1.65%) and detection of systematic coding errors in length of stay.
2. **Variable selection and scaling** - Select a relevant set of numerical variables for clustering (9 clinical features) and apply hybrid scaling strategy (StandardScaler for continuous/ordinal variables, no scaling for binary).
3. **K-means clustering** - Apply unsupervised k-means clustering and visualize the resulting groups. Optimal k justified using four complementary metrics (elbow method, silhouette score, Calinski-Harabasz index, Davies-Bouldin index).
4. **Dimensionality reduction** - Apply Principal Component Analysis (PCA) to visualize the clusters in 2D, reporting explained variance.
5. **Cluster interpretation** - Interpret the clusters by analyzing centroids in the original (non-scaled) space. Identify clinical patient profiles per cluster and propose real-world applications (triage support, error detection, resource optimization).

## Files

- `gcd_aa2_act3_grupo_alexrubino.ipynb` - Main Jupyter notebook (in Spanish)
- `Actividades_gcd_aa2_act3_proy_4P_dataset.csv` - Source dataset
- `dataset_limpio.csv` - Cleaned dataset generated after Exercise 1

## Language

The notebook is written in Spanish, as required by the course activity.

## Usage

This code is for educational purposes as part of the Machine Learning 2 course.
Feel free to explore and learn from it.
