# 📱 Google Play Store Data Analytics

An exploratory data analysis (EDA) and data cleaning project on the Google Play Store dataset using Python, Pandas, Matplotlib, and Seaborn.

---

## 📌 Project Overview
The goal of this project is to analyze mobile application performance, ratings, installs, pricing models, and user engagement metrics using real-world data from the Google Play Store.

---

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Plotly
* **Environment:** VS Code & Jupyter Notebooks

---

## 📋 Progress Log

### Milestone 1: Setup & Initial Inspection (Completed)
* Configured local Python development environment in VS Code.
* Loaded `googleplaystore.csv` (10,841 records, 13 features).
* Identified data type mismatches where numerical fields (`Installs`, `Price`, `Reviews`, `Size`) were stored as `object` (string) types.

### Milestone 2: Data Cleaning & Preprocessing (Completed)
* **Corrupted Record Removal:** Dropped shifted row `10472` containing misaligned values.
* **Installs Column:** Stripped formatting characters (`,` and `+`) and converted values to `int64`.
* **Price Column:** Removed currency symbols (`$`) and cast values to `float64`.
* **Reviews Column:** Converted review counts to `int64`.
* **Size Standardization:** Standardized sizes to Megabytes (`float64`), converting Kilobytes (`k`) to MB and replacing `'Varies with device'` with `np.nan`.
* **Deduplication:** Dropped `1,181` duplicate app records, leaving `9,659` distinct applications.
* **Missing Value Imputation:** Imputed missing values in `Rating` using the mean (`4.2`), and dropped 11 rows with missing categorical/version values (`Type`, `Current Ver`, `Android Ver`).

### Milestone 3: Exploratory Data Analysis & Visualizations (In Progress)
* **Volume vs. Demand:** Identified that while `FAMILY` leads in total app count, `GAME` and `COMMUNICATION` dominate in total installs.
* **Rating Distribution:** Plotted KDE histogram showing user ratings are left-skewed, clustering between 4.0 and 4.5.
* **Monetization Analysis:** Analyzed Free (~92%) vs. Paid (~8%) apps; box plots reveal paid apps maintain slightly higher average ratings (~4.25 vs ~4.17) with significantly fewer 1-star outliers.
* **Size vs. Satisfaction:** Generated scatter plot and calculated Pearson correlation coefficient (~0.056), demonstrating that file size has virtually no linear correlation with user ratings.

---

## ⏭️ Upcoming Next Steps
* [ ] Complete user engagement analysis (Reviews vs. Installs).
* [ ] Identify top revenue-generating paid apps.
* [ ] Build interactive visualizations with Plotly (Phase 4).