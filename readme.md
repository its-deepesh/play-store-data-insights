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
* Identified data type mismatches where numerical fields (`Installs`, `Price`, `Reviews`) were stored as `object` (string) types.

### Milestone 2: Data Cleaning & Preprocessing
* **Corrupted Record Removal:** Detected and dropped shifted row `10472` containing invalid categories and shifted string metrics (`"Free"` in `Installs`).
* **Installs Column:** Stripped non-numeric formatting characters (`,` and `+`) using string replacement, then converted values to 64-bit integers (`int64`).
* **Price Column:** Filtered out the currency symbol (`$`) from paid app entries and cast the column to floating-point numbers (`float64`).

---

## ⏭️ Upcoming Next Steps
* [ ] Convert the `Reviews` column into integer format.
* [ ] Standardize the `Size` column (convert `M` and `k` to consistent numeric megabytes).
* [ ] Handle missing values in `Rating` and categorical columns.
* [ ] Exploratory visual analysis with Seaborn & Matplotlib.
* [ ] Interactive dashboards with Plotly.