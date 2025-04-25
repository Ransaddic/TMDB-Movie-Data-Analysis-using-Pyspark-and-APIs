
# TMDB Movie Data Analysis using PySpark and APIs

## 📽️ Overview  
This project presents a comprehensive analysis of movie data from The Movie Database (TMDB). Leveraging PySpark and the TMDB API, we explore financial performance, audience reception, genre trends, and production elements that influence a movie's success.

---

## 🎬 Introduction  
The global film industry generates billions in revenue annually. Understanding what drives a movie's success is vital for studios, investors, marketers, and creators. This project analyzes curated TMDB data to uncover patterns and insights that can inform strategic decisions in filmmaking and distribution.

---

## 🎯 Project Objectives  
- **API Data Extraction**: Gather movie metadata using the TMDB API.  
- **Data Cleaning & Transformation**: Preprocess and structure data for analysis using PySpark.  
- **Exploratory Data Analysis (EDA)**: Identify trends across financial and audience metrics.  
- **Advanced Filtering & Ranking**: Rank movies based on profitability, ratings, and popularity.  
- **Franchise & Director Analysis**: Compare franchises and directors across key success metrics.  
- **Visualization & Insights**: Present results using insightful visualizations.

---

## 📊 Dataset  
The dataset includes a variety of movie-related information:  
- **Metadata**: Title, release date, runtime  
- **Financials**: Budget and revenue  
- **Audience Metrics**: Popularity, vote count, average ratings  
- **Production Info**: Companies, countries, languages  
- **Creative Aspects**: Genres, cast, directors

### 🔗 Data Source  
Data was collected via the [TMDB API](https://developers.themoviedb.org/3/getting-started/introduction) using selected movie IDs:  
`[0, 299534, 19995, 140607, 299536, 597, 135397, 420818, 24428, 168259, 99861, 284054, 12445, 181808, 330457, 351286, 109445, 321612, 260513]`

---

## ⚙️ Installation  
### Set up a Python environment and install dependencies:
```bash
pip install -r requirements.txt
```

### PySpark Setup Instructions  
To use PySpark locally:  
1. Install Java (JDK 8 or later).  
2. Install Spark from https://spark.apache.org/downloads.html.  
3. Set environment variables in your shell config (`.bashrc`, `.zshrc`, or `.profile`):  
```bash
export SPARK_HOME=/path/to/spark
export PATH=$SPARK_HOME/bin:$PATH
export PYSPARK_PYTHON=python3
```  
4. Start using Spark in your scripts or notebooks.

---

## 🗂️ Project Structure  
```
tmdb-data-analysis/
│
├── data/                          
│   ├── clean_movies_df.parquet         # Processed, cleaned dataset
│   ├── extracted_movies_df.parquet     # Raw data from TMDB API
│
├── notebooks/
│   ├── data_extraction.ipynb           # API integration and data fetching
│   ├── data_cleaning.ipynb             # Data preprocessing and transformation
│   ├── data_analysis.ipynb             # Analysis and visualization
│
├── requirements.txt                   # Python dependencies
├── README.md                          # Project documentation
```

---

## 📌 Key Findings  

### 🔝 Best & Worst Performing Movies  
- 💸 **Highest Budget**: *Avengers: Age of Ultron*  
- 💰 **Highest Revenue**: *Avatar*  
- 🏆 **Most Profitable & Highest ROI**: *Avatar*  
- 📉 **Lowest Profit & ROI**: *Avengers: Age of Ultron*  
- 🔥 **Most Popular Movie**: *Avengers*  
- ⭐ **Highest Rated Movie**: *Avengers: Endgame*

---

### 🧩 Franchise vs. Standalone Performance  
- 🎯 **Standalone Movies**  
  - Higher **average revenue**  
  - Higher **median ROI**  
  - Higher **average popularity**  

- 🧬 **Franchise Movies**  
  - Higher **average budget**

---

### 🧠 Most Successful Franchises & Directors  
- 🏙 **Top Franchise by Number of Movies**: *The Avengers Collection*  
- 💼 **Highest Budget (Total & Average)**: *The Avengers Collection*  
- 🤑 **Highest Revenue (Total)**: *The Avengers Collection*  
- 💵 **Highest Revenue (Average)**: *The Avatar Collection*  
- 🎓 **Highest Average Ratings**: *The Harry Potter Collection*  

- 🎬 **Top Directors by Number of Movies**:  
  *James Cameron, Joss Whedon, Anthony Russo, Joe Russo, Chris Buck, Jennifer Lee*  

- 💲 **Most Successful Director by Revenue**: *James Cameron*  
- 🌟 **Most Successful Directors by Rating**: *Joe Russo, Anthony Russo*
