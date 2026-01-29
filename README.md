# 🎬 Netflix Movie Analysis (EDA + Data Cleaning + Preprocessing)

This project performs **Exploratory Data Analysis (EDA)** and **data preprocessing** on a Netflix-style movie dataset to extract insights about movie releases, genres, popularity, and voting patterns.

---

## 📌 Project Objectives

The goal of this analysis is to:
- Understand trends in movie releases over the years
- Identify the most frequent genres
- Analyze popularity and voting distributions
- Clean and preprocess the dataset for further analysis / modeling

---

## 📂 Dataset Information

**Dataset file:** `mymoviedb.csv`

### Available Columns (raw dataset)
- `Release_Date`
- `Title`
- `Overview`
- `Popularity`
- `Vote_Count`
- `Vote_Average`
- `Original_Language`
- `Genre`
- `Poster_Url`

---

## 🧹 Data Cleaning Performed

Since the dataset contained **no missing values** and **no duplicate records**, cleaning mainly focused on removing irrelevant columns:

✅ Dropped columns:
- `Overview`
- `Original_Language`
- `Poster_Url`

---

## ⚙️ Feature Engineering & Preprocessing

Key preprocessing steps:
- Converted `Release_Date` to datetime format
- Extracted `Release_Year` for year-wise analysis
- Cleaned and transformed `Genre` column:
  - Split comma-separated genres
  - Used `explode()` to ensure **one genre per row**
- Categorized `Vote_Average` into quartile-based bins (optional):
  - `not_popular`, `below_avg`, `average`, `popular`

---

## 📊 Exploratory Data Analysis (EDA)

The notebook answers questions such as:
- Which genre appears most frequently in the dataset?
- Which movie has the highest popularity and what is its genre?
- Which movie has the lowest popularity and what is its genre?
- Which year has the highest number of movie releases?
- What is the distribution of popularity scores?
- How are popularity, vote count, and release year correlated?

---

## 🔑 Key Insights

- **Drama** is the most frequent genre in the dataset.
- Movie releases show a strong increasing trend over time, peaking in **2021**.
- Popularity distribution is **right-skewed**, meaning most movies have low-to-moderate popularity while a few are extremely popular (outliers).
- **Spider-Man: No Way Home** has the highest popularity and belongs to multiple genres (Action, Adventure, Science Fiction).
- Correlation analysis shows **weak relationships** among features, indicating popularity depends on multiple factors.

---

## 🛠️ Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

