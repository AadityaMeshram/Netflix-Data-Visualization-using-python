# Netflix-Data-Visualization-using-python
A comprehensive exploratory data analysis (EDA) and visualization project on a Netflix dataset using Python. This project uncovers content trends, genre patterns, rating distributions, and production insights from over 6,000 Netflix titles.
# 🎬 Netflix Data Visualization Project

A comprehensive exploratory data analysis (EDA) and visualization project on a Netflix dataset using Python. This project uncovers content trends, genre patterns, rating distributions, and production insights from over 6,000 Netflix titles.

---

## 📁 Project Structure

```
netflix-data-visualization/
│
├── Data_visualization_project_in_netflix.ipynb   # Main Jupyter Notebook
├── Netflix.csv                                    # Raw dataset
├── cleaned_netflix_data.csv                       # Cleaned output dataset
└── README.md
```

---

## 📊 Dataset Overview

| Property | Value |
|---|---|
| Total Records | 6,069 |
| Total Columns | 13 |
| Date Range | 2013 – 2022 |
| Source | Netflix Titles Dataset |

**Columns:** `Sl.No`, `Title`, `Description`, `Genres`, `Cast`, `Director`, `Production Country`, `Added to Netflix On`, `Year`, `Series`, `Duration(in Minutes)`, `Season`, `Rating`

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** – Data loading, cleaning, manipulation
- **NumPy** – Numerical operations
- **Matplotlib** – Base plotting
- **Seaborn** – Statistical visualizations
- **Jupyter Notebook** – Interactive development environment

---

## 🔧 Data Cleaning Steps

- Filled missing `Rating` values with column mean
- Filled missing text columns (`Director`, `Cast`, `Production Country`, `Genres`) with `"Unknown"`
- Removed duplicate rows (0 duplicates found)
- Converted `Added to Netflix On` to datetime format
- Extracted `Added_Year` from the date column
- Cleaned `Duration(in Minutes)` — removed season-based strings and converted to numeric
- Replaced `"Unknown"` in `Production Country` with `NaN` for accurate country analysis
- Calculated `Content_Age` = `Added_Year` − `Year`

---

## 📈 Visualizations & Key Insights

### 1. Rating Distribution
- Most Netflix content is rated between **6 and 7**.
- The distribution shows a clear peak around **6.5**, indicating moderate overall quality.

### 2. Average Rating by Release Year
- Older content (pre-2000) tends to have **higher average ratings** due to selective curation.
- Post-2000 content shows **high volatility** as volume increased.

### 3. Average Rating by Netflix Added Year
- **2014** had the highest average rating (~7.4) — early Netflix focused on quality.
- **2017–2018** saw the lowest ratings (~6.5) — period of content saturation.
- **2020** dipped again due to COVID-era mass production.
- **2021–2022** shows slight stabilization — Netflix entering an optimization phase.

### 4. Top 10 Genres on Netflix
- **International Movies** dominate by a large margin — reflecting Netflix's global expansion strategy.
- **Dramas** are the most popular content theme across both movies and TV.
- **Comedies** and **International TV Shows** also rank highly.
- **Romantic Movies** appear at the bottom, often blended with other genres.

### 5. Top Producing Countries
- **United States** leads content production by far.
- **Japan**, **United Kingdom**, and **South Korea** follow.
- India, Spain, Canada, France, Australia, and Mexico round out the top 10.

### 6. Top 10 Directors
- A large portion of director data is missing — common in auto-scraped OTT datasets.
- Named directors include Rajiv Chilaka, Suhas Kadav, Marcus Raboy, and others.

### 7. Duration Distribution
- Most content falls between **60–120 minutes**, aligning with standard movie length.
- The distribution is right-skewed, with a few titles exceeding 250 minutes.

### 8. Content Trend by Year and Rating (Heatmap)
- Content volume has **surged post-2010**.
- Mature-rated content has increased in recent years, reflecting a shift in audience demand.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/netflix-data-visualization.git
   cd netflix-data-visualization
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook Data_visualization_project_in_netflix.ipynb
   ```

4. **Update the dataset path** in the notebook to point to your local `Netflix.csv` file.

---

## 📌 Conclusions

1. Netflix content production has grown rapidly over the years.
2. Few countries (US, Japan, UK, South Korea) dominate global content creation.
3. Netflix primarily targets mature audiences with high-rated content.
4. Most content follows standard movie duration patterns (60–120 min).
5. Movies dominate the catalog, but TV series show increasing popularity.
6. Early Netflix focused on quality; rapid expansion caused a temporary quality dip.
7. Data visualization effectively uncovered hidden business and content trends.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
