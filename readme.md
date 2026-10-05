# 📱 Google Play Store Data Analytics

An exploratory data analysis (EDA) and data cleaning project on the Google Play Store dataset using Python and Pandas.

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

### Milestone 1: Setup & Initial Inspection
* Configured local Python development environment in VS Code.
* Loaded `googleplaystore.csv` (10,841 records, 13 features).
* Identified data type mismatches where numerical fields (`Installs`, `Price`, `Reviews`, `Size`) were stored as `object` (string) types.

### Milestone 2: Data Cleaning & Preprocessing (Completed)
* **Corrupted Record Removal:** Dropped shifted row `10472` containing misaligned values.
* **Installs Column:** Stripped non-numeric formatting characters (`,` and `+`) and converted values to 64-bit integers (`int64`).
* **Price Column:** Filtered currency symbols (`$`) and cast values to floating-point numbers (`float64`).
* **Reviews Column:** Cast cleaned review counts to 64-bit integers (`int64`).
* **Size Standardization:** Wrote and applied a custom parsing function to standardize values into Megabytes (`float64`), converting Kilobytes (`k`) to MB and setting `'Varies with device'` to `np.nan`.
* **Deduplication:** Identified and dropped `1,181` duplicate app records based on unique app names, preserving `9,659` distinct applications.
* **Missing Value Imputation:** Imputed missing values in `Rating` using the dataset mean (`4.2`), and dropped 11 rows with missing categorical/version attributes (`Type`, `Current Ver`, `Android Ver`).

---

## ⏭️ Upcoming Next Steps
* [ ] **Phase 3:** Exploratory Data Analysis & Static Visualizations (Matplotlib & Seaborn)
  * Analyze top app categories by volume.
  * Investigate rating distributions and user review trends.
  * Compare free vs. paid app metrics.
* [ ] **Phase 4:** Interactive Dashboards with Plotly.