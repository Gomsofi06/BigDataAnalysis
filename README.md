

# <center>Big Data Analysis Project</center>

<center>
Master in Data Science and Advanced Analytics <br>
NOVA Information Management School
</center>

** **

<center>
David Cascão,   <br>
Jan-Louis Schneider,   <br>
Marta Boavida,   <br>
Jorge Cordeiro,   <br>
Sofia Gomes,   <br>
</center>

** **

## EEG Seizure Detection 

End-to-end big data pipeline to classify pediatric EEG recordings into three states:
**Normal**, **Pre-seizure**, and **Seizure**.  
Implemented in **PySpark on Databricks** to handle large-scale time-series data efficiently.

### Highlights
- Large-scale dataset: **~4.6M rows** of EEG-derived time-series features.
- Preprocessing in PySpark: exploration, cleaning, missing values handling, and time-series preparation.
- Model benchmarking in Spark ML:
  - Logistic Regression
  - Random Forest
  - Gradient-Boosted Trees
  - Multilayer Perceptron (MLP)
- Hyperparameter tuning with **random search** + **3-fold cross-validation**.
- Best model: **Random Forest**, achieving **~92% test accuracy** (with careful discussion of class imbalance).

### Repository structure
This repository is notebook-driven (Databricks/Jupyter style). Recommended execution order:

1. `01_preprocessing.ipynb` — data loading, exploration, cleaning and feature preparation  
2. `02_model_logistic_regression_final.ipynb` — baseline model + tuning  
3. `03_model_random_forest_final.ipynb` — tuning + best-performing model  
4. `04_model_gradient_boosted_trees_final.ipynb` — tuning and comparison  
5. `05_model_multilayer_perceptron_final.ipynb` — Spark MLP experiments  
6. `06_Transformers models.ipynb` — optional experiments (if applicable)  
7. `07_model_long_short_term_memory_final.ipynb` — optional experiments (if applicable)

Folders:
- `docs/` — report / documentation
- `graphics/` — plots and figures
- `extra/` — additional material / intermediate outputs

### Data
The dataset was provided in an academic context and may not be included in this repository.
If you want to run the notebooks:
- upload the dataset to Databricks (DBFS) or mount it,
- update the input paths in `01_preprocessing.ipynb`.

### Results 
Random Forest achieved the strongest performance on the held-out test set (~92% accuracy).
We analyzed model behavior under strong class imbalance, complementing accuracy with additional analysis and dashboards.


