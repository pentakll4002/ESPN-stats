## 📊 ESPN-Stats with Power BI

This project extracts, cleans, and visualizes ODI Cricket Statistics (Batting, Bowling, and Fielding) from ESPN Cricinfo Stats
. The dataset focuses on England vs. Australia matches in ODI format, with filters applied to home/away conditions and ordered by fielding dismissals.

The processed data is published and visualized using Power BI Service (Cloud).

### 🚀 Project Workflow
#### 1. Data Crawling

- Sources:

    - Batting Stats

    - Bowling Stats

    - Fielding Stats

- Extracted across all available ODI pages for complete coverage.

- Automated crawling ensures no manual copy-pasting of statistics.

#### 2. Data Cleaning & Transformation

Performed in Power Query (Power BI):

- Removed duplicates, null values, and unnecessary columns.

- Standardized column names for consistency across datasets.

- Converted data types (e.g., numeric fields for Runs, Strike Rate, etc.).

- Merged datasets for holistic analysis (Batting + Bowling + Fielding).

#### 3. Feature Engineering

New calculated columns and measures include:

- Strike Rate Categories

    - Categorized strike rates into ranges (e.g., 0–50, 51–80, 81–100, 101–140).

- Strike Rate Ranking

    - Created rank ordering for players based on strike rate values.

- Deviation Metrics

    - Deviation = Runs - AVERAGE(Runs)

    - Absolute Deviation = |Runs - AVERAGE(Runs)|

    - Squared Deviation = (Runs - AVERAGE(Runs))²

These allow for more advanced statistical insights into batting performance.

#### 4. Power BI Modeling

- Relationships built between Batting, Bowling, and Fielding tables.

- Calculated measures (DAX) for:

    - Strike Rate Analysis

    - Fielding Efficiency

    - Bowling Economy & Wickets Comparison

    - Player Performance Distribution
 
#### 5. Visualization

Interactive Power BI dashboards include:

- 📈 Batting Analysis → Strike Rate vs Runs, Player Categories, Ranking

- 🎯 Bowling Analysis → Wickets, Economy Rate, Match Impact

- 🧤 Fielding Analysis → Dismissals, Catching Efficiency

- ⚖️ Overall Comparison → England vs Australia, Home vs Away

#### 6. Publishing

- Report published to Power BI Cloud (Power BI Service).

- Enables real-time access, sharing, and collaboration.


### 📂 Repository Structure
    `
      📁 ESPN-Stats
     ┣ 📂 data/               # Raw crawled data (Batting, Bowling, Fielding)
     ┣ 📂 powerbi/            # Power BI .pbix files
     ┣ 📂 reports/            # Exported PDF/PNG of dashboards
     ┣ 📜 README.md           # Documentation
     ┗ 📜 requirements.txt    # Python crawling dependencies (if applicable)
    `

### 🛠️ Tech Stack

- Python → Web scraping (BeautifulSoup / Pandas)

- Power BI → Data cleaning, modeling, visualization

- DAX → Measures and statistical calculations

- Power BI Service → Cloud publishing & sharing


### 🌟 Key Insights

- Strike Rate categorization highlights batting efficiency across matches.

- Deviation analysis provides insights into player consistency.

- Fielding dismissals reveal match-changing contributions often overlooked.

- Combined view enables a 360° performance analysis of England vs Australia ODIs.

### 📌 Next Steps

- Extend analysis to other teams and formats (T20, Test).

- Automate data refresh from ESPN Stats into Power BI Cloud.

- Add predictive modeling layer (Machine Learning integration).

