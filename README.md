# 📘 Predicting EA FC 26 Player Ratings from Real-World Football Statistics

This project explores whether EA FC 26 player attribute ratings can be predicted directly from 2024–2025 real-world football performance metrics. Using a combined dataset from Kaggle and a machine-learning pipeline implemented in Python, we build regression models to predict seven key EA FC attributes: **overall**, **pace**, **shooting**, **passing**, **dribbling**, **defending**, and **physic**.

The full methodology, preprocessing, model comparisons, and results are documented in the accompanying final report.


## 📊 Datasets Used

You must download the following two datasets from Kaggle:

**[1] Football Players Stats (2024–2025)**  
Sidorowicz, Hubert. “Football Players Stats (2024-2025).” Kaggle, 23 June 2025.  
https://www.kaggle.com/datasets/hubertsidorowicz/football-players-stats-2024-2025  

**[2] FC 26 (FIFA 26) Player Data**  
Rovnez. “FC 26 (FIFA 26) Player Data.” Kaggle, 22 Sept. 2025.  
https://www.kaggle.com/datasets/rovnez/fc-26-fifa-26-player-data  

These files **are not stored in the repository** due to Kaggle’s terms of service.


## 📁 Setting Up the Project in Google Colab

In order to run the notebook end-to-end, some setup is needed. Follow the setup procedure below.

### Step 1 — Download the two CSV files
You will obtain:

- `players_data-2024_2025.csv`
- `FC26.csv`

### Step 2 — Upload them to Google Drive  
Place them in:

```
MyDrive/Colab Notebooks/Project/
```

The directory structure should look like:

```
/content/drive/MyDrive/Colab Notebooks/Project/FC26.csv
/content/drive/MyDrive/Colab Notebooks/Project/players_data-2024_2025.csv
```

### Step 3 — Ensure the notebook paths match

```python
fc_2026_file_path = '/content/drive/MyDrive/Colab Notebooks/Project/FC26.csv'
player_stats_file_path = '/content/drive/MyDrive/Colab Notebooks/Project/players_data-2024_2025.csv'
```

If your file names match these defaults, no changes are needed.

If you would like to store your files elsewhere on your drive, make sure to update the notebook paths accordingly.


## 🧠 What the Notebook Does

The notebook performs the full machine learning pipeline:

1. Loads both datasets  
2. Cleans and normalizes data  
3. Performs fuzzy matching using nationality, club, birth year, and name similarity  
4. Merges datasets into a unified player table  
5. Runs exploratory data analysis  
6. Trains ML models:
   - Linear Regression  
   - Ridge / Lasso  
   - Decision Tree  
   - Random Forest  
   - XGBoost  
   - MLP Regressor  
7. Tunes hyperparameters with cross-validation  
8. Evaluates model performance on a held-out test set  
9. Selects best-performing model per target  
10. Generates predicted vs. actual comparison tables

This codebase is fully reproducible using Google Colab.


## 📎 How to Run the Notebook

1. Open the notebook in Google Colab  
2. Mount Google Drive (by running first cell block)
3. Ensure datasets are located in the correct directory  
4. Run cells from top to bottom  
5. View visualizations and model results


## 🧑‍💻 Contributors

- Ali Khimji  
- Ashraf Mahdi  
- Ali Alibhai  
- Naim Albadawi  
- Junaid Mohammed

