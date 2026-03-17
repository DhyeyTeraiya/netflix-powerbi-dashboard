# 🎬 Netflix Movies & TV Shows Dashboard — Power BI

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Domain-Entertainment%20Analytics-E50914?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Dataset-8000%2B%20Titles-20BEFF?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>
</p>

---

## 📌 Project Overview

This project presents a **fully interactive Power BI Dashboard** that analyzes Netflix's entire content library. With **8,000+ titles** spanning movies and TV shows across multiple genres, countries, and decades, this dashboard delivers deep entertainment industry insights through stunning visualizations.

> 🎯 **Goal**: Explore Netflix's content strategy — what they produce, where, when, and for whom — through data-driven storytelling.

---

## 🖼️ Dashboard Preview

![Netflix Dashboard Preview](Netflix%20Movies%20and%20TV%20Shows%20Dashboard%20-%20by%20Shaikh%20Minhaj.png)

---

## 📊 Dashboard Features & Pages

### 🏠 Overview Page
- Total titles, Movies vs TV Shows split (donut chart)
- Rating distribution across content types
- Year-over-year content addition trend

### 🌍 Geographic Analysis
- World map: Country-wise content production
- Top 10 content-producing countries
- Regional content distribution

### 🎭 Content Analysis
- Genre breakdown and top genres
- Content rating distribution (TV-MA, PG-13, R, etc.)
- Duration analysis (Movies by minutes, Shows by seasons)

### 📅 Timeline Analysis
- Content addition trends by year and month
- Historical release year distribution
- Newest vs classic content balance

### 🔍 Content Explorer
- Searchable/filterable title lookup
- Director and cast analysis
- Description word cloud

---

## 🔍 Key Insights

| Category | Insight |
|----------|---------|
| 📺 Content Split | ~70% Movies, ~30% TV Shows |
| 🌍 Top Producer | United States leads with 36% of all content |
| 📅 Peak Addition Year | 2019 saw the highest number of titles added |
| 🎭 Most Popular Genre | International Movies & Dramas dominate |
| ⭐ Common Rating | TV-MA is the most frequent content rating |
| 📆 Oldest Title | Content dates back to the 1920s |

---

## 📁 Project Structure

```
Netflix-Movies-and-TV-Shows-Dashboard/
├── 📊 Netflix Moveis and TV Shows Dashboard.pbix    # Power BI file
├── 📄 netflix_titles.csv                            # Source dataset (8,807 records)
├── 🖼️ Netflix Movies and TV Shows Dashboard.png    # Dashboard screenshot
├── 🖼️ Netflix.png                                  # Logo/branding asset
└── 📄 README.md                                    # Project documentation
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and publishing |
| **Power Query (M Language)** | Data transformation and cleaning |
| **DAX (Data Analysis Expressions)** | Custom measures and calculated columns |
| **Python/R Visual** | Advanced statistical visualizations |

---

## ⚙️ DAX Measures Used

```dax
Total Titles = COUNTROWS(netflix_titles)

Movies = CALCULATE([Total Titles], netflix_titles[type] = "Movie")

TV Shows = CALCULATE([Total Titles], netflix_titles[type] = "TV Show")

Content Added This Year = 
CALCULATE([Total Titles], 
    YEAR(netflix_titles[date_added]) = YEAR(TODAY()))

Avg Movie Duration (min) = 
CALCULATE(AVERAGE(netflix_titles[duration_mins]), 
    netflix_titles[type] = "Movie")
```

---

## 📋 Dataset Information

- **Source**: [Kaggle — Netflix Movies and TV Shows](https://www.kaggle.com/shivamb/netflix-shows)
- **Records**: 8,807 titles
- **Columns**: 12 (show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description)
- **Coverage**: Content available on Netflix as of 2021

---

## 🚀 How to Use

1. **Install** [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. **Clone** this repository
3. **Open** `Netflix Moveis and TV Shows Dashboard.pbix`
4. Interact with the slicers (Type, Country, Genre, Year)
5. Hover over visuals for detailed tooltips
6. Use **Drill Through** for title-level details

---

## 💼 Business Applications

- 🎬 **Content Strategy**: Understand what types of content resonate
- 🌍 **Market Expansion**: Identify underserved geographic markets
- 💰 **Investment Planning**: Data-driven content acquisition decisions
- 👥 **Audience Targeting**: Match content ratings to target demographics

---

## 👤 Author

**Dhyey Teraiya** — Batch 8, Data Analytics Student

- 🐙 GitHub: [@DhyeyTeraiya](https://github.com/DhyeyTeraiya)
- 💼 LinkedIn: [Dhyey Teraiya](https://linkedin.com/in/dhyey-teraiya)

---

## 📄 License

This project is licensed under the **MIT License**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

⭐ **Star this repo if you enjoyed it!** ⭐

> *"The best stories are told not just with words, but with data."*
