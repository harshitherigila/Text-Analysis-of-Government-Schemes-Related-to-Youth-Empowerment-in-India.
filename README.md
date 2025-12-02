

# **Text-Analysis-of-Government-Schemes-Related-to-Youth-Empowerment-in-India**

A regex-based project which uses parallel processing to find youth-related government schemes.

1. **Text Analysis of Government Schemes Related to Youth Empowerment in India.**
2. This project performs rule-based text analysis on government documents and scheme descriptions related to youth empowerment. It identifies how frequently themes like Education, Skill Development, Employment, and Entrepreneurship appear across government schemes.
3. The system uses regex, keyword-based scoring, and parallel processing to analyze large scheme documents efficiently.


# **Problem Statement**

The Government of India publishes many schemes focusing on youth empowerment, but the themes are not directly labeled.


# **Goal**

Build a system that reads government scheme text and finds:

* Whether it relates to Education, Skill Development, Employment, Entrepreneurship, or Sports
* How many times youth-related terms appear
* The distribution of scheme themes


# **Objectives**

1. Perform text analysis on government scheme descriptions
2. Automatically detect scheme themes using keyword matching
3. Process data using parallel computing to improve speed
4. Save results into CSV and SQLite database files
5. Visualize findings using bar and pie charts
6. Provide insights on scheme distribution across themes


# **Technologies Used**

* Python
* Pandas
* Regex Text Processing
* Parallel Processing (ProcessPoolExecutor)
* SQLite Database
* Matplotlib
* Google Colab


# **My Approach**

1. Collected government schemes data from the dataset.
2. Preprocessed the data using regex to convert it into cleaned text.
3. Created a Theme Dictionary to search for keywords inside the cleaned data.
4. For searching, I used rule-based regex:

   * For single keywords (e.g., *skill*) → used `\b keyword \b`
   * For multi-keyword terms (*Skill Development*) → split into (*skill*, *development*) and assigned +2 weight for each match.
5. Used parallel processing to improve performance.
6. Stored outputs in CSV and SQLite database.
7. Generated visualizations.


# **How to Run the Project**

### **Step 1 — Upload Files to Google Colab**

Upload:

* `Government_schemes.csv`
* `themes.db`

### **Step 2 — Run the Notebook**

Open the file:

```
src/Youth_Scheme_Project.ipynb
```

Run all cells to:

* mount drive
* load datasets
* detect themes
* generate visualizations
* save output

### **Step 3 — View the Output**

Check the `/output/` folder for:

* CSV results
* Database results
* Charts


# **Sample Visualizations**

* **Bar Chart (Themes Count):** Shows which themes are most common.
* **Pie Chart (Percentage Split):** Shows the distribution of schemes across themes.


# **Output Files**

* `detected_themes_results.csv`
* `detected_themes_results.db`
* `bar_chart.png`
* `pie_chart.png`


