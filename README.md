# 🎧 Spotify Song Popularity Analysis**

### 📌 Background

Music streaming has transformed how people discover and consume music globally. Platforms like **Spotify** serve over 500 million users across 180+ markets. Understanding the factors that influence a song’s popularity is critical for artists, labels, and the music industry.

Spotify provides measurable **audio features** such as energy, danceability, and valence. These can serve as predictors of commercial success. This analysis explores the relationships between audio features and song popularity.

---

## ❓ Research Questions

1. **Is there a relationship between a song's energy level and its popularity on Spotify?**
2. **How do energy level and danceability together predict a song's popularity on Spotify?**

---

## 🧪 Data Overview

* **Population**: All songs available on Spotify
* **Sample**: Top 50 songs from 73 countries
* **Source**: Spotify API via Kaggle dataset by [ASANICZKA](https://www.kaggle.com/datasets/asaniczka/top-spotify-songs-in-73-countries-daily-updated)
* **Note**: Observational data used for descriptive and inferential analysis.

---

## 🔧 Data Preparation

* Loaded dataset: `universal_top_spotify_songs.csv`
* Removed irrelevant variables (e.g., country column)
* Verified data structure and removed NAs where appropriate

---

## 📈 Methodology

### 📊 Question 1: Energy & Popularity

* **Method**: Simple linear regression
* **Visualization**: Scatterplot with regression line
* **Model**: `popularity ~ energy`

### 🔍 Question 2: Energy, Danceability & Popularity

* **Method**: Multiple linear regression
* **Visualization**: Side-by-side plots and color-coded scatterplot
* **Model**: `popularity ~ energy + danceability`

---

## 📉 Key Results

### ✅ **Q1: Simple Linear Regression**

* **Effect**: For every 1-unit increase in energy, **popularity decreases by \~2.15 points**
* **95% CI**: \[-2.28, -2.02]
* **R²**: 0.0005 (\~0.05% of variance explained)
* **Conclusion**: Statistically significant, but **not practically meaningful**

### ✅ **Q2: Multiple Linear Regression**

* **Energy effect**: −0.92 (95% CI: \[-1.05, -0.78])
* **Danceability effect**: −5.38 (95% CI: \[-5.54, -5.23])
* **R²**: 0.00275 (\~0.28% of variance explained)
* **Conclusion**: Both predictors are statistically significant, but together explain **less than 1%** of popularity variance.

---

## 📉 Model Diagnostics

* **Linearity**: Residuals vs. fitted values suggest linear models are reasonable
* **Normality**: Q-Q plots reveal mild deviations from normality
* **Conclusion**: Models meet assumptions but offer limited predictive utility

---

## 🧠 Validity Assessment

* **External Validity**: Limited by sample (top 50 songs only); not generalizable to all Spotify tracks
* **Internal Validity**: Cannot infer causality; potential confounders like artist fame or label marketing not included
* **Construct Validity**: Spotify's popularity metric and audio features may not fully capture human perception or broader music success

---

## 🚀 Implications

* Audio features like energy and danceability have **minimal impact** on popularity
* Marketing, playlist placement, artist reputation, and release timing likely **play larger roles**
* Industry professionals should **not over-rely** on audio features when predicting success

---

## 🔭 Future Research

* Include variables like:

  * Artist follower count
  * Label information
  * Playlist placements
  * Genre, release date, and platform-specific metrics (e.g., TikTok virality)
* Expand across time to capture **evolving trends**
* Explore **interaction effects** and **non-linear models**
* Study **recommendation algorithms** and their role in popularity

---

## 📚 References

* Saniczka, A. *Top Spotify Songs in 73 Countries (Daily Updated)*. Kaggle, 2024. [Link](https://www.kaggle.com/datasets/asaniczka/top-spotify-songs-in-73-countries-daily-updated)
