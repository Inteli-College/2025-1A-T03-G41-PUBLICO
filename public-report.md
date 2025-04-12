# Public Report — Educational performance analysis for Instituto Ponte

## Project overview

This project was developed for **Instituto Ponte**, an NGO (Non-Governmental Organization) that operates across various regions of Brazil, offering educational opportunities to talented public school students in situations of social vulnerability. The organization seeks to optimize its **student selection process** and better understand the **educational gaps** and **socioeconomic barriers** that impact academic performance in Brazil.

---

## Sprint 1 — Inteli Project Opening Term and Project Planning

In the first sprint, the following artifacts were created:

- **Inteli Project Opening Term** outlining the project’s justification, objectives, methodology, and expected outcomes.
- A detailed **project plan**, including stakeholder agreements, communication frequency, expected deliverables, risks, assumptions, constraints, and governance structure.
- The project was structured to be executed individually by Wagner Estevam Barcelos da Silva over a period of **40 weeks**, divided into **20 sprints**.

### Key objectives:
- Identify key educational gaps across Brazilian regions.
- Incorporate socioeconomic and demographic filters (e.g., race, gender, income).
- Integrate public datasets such as ENEM and results from academic olympiads (e.g., OBMEP, OBA).
- Deliver a simple, scalable platform with clear visualizations and intuitive user experience.

---

## Sprint 2 — Research and data collection

During this sprint, extensive research was conducted on reliable public data sources. After evaluating several alternatives, it was decided to use the **ENEM microdata from INEP** as the main foundation for the platform.

### Why ENEM microdata?
- It provides **anonymized individual-level data** on exam scores and student demographics.
- Includes detailed information on **school types**, **socioeconomic background**, **race/gender**, and **geographic location**.
- Covers the period from **2009 to 2023**, enabling both historical analysis and trend identification.

### Next steps defined:
- Downloading and organizing the microdata files.
- Cleaning and standardizing data to ensure consistency.
- Creating filters and preparing the datasets for visualization and dashboarding.

---

## Sprint 3 — Initial dataset structuring

In this sprint, ENEM microdata files were:
- **Stored on Google Drive**
- **Accessed via Google Colab** using the `pandas` library
- **Processed and cleaned** for the years 2009 through 2023

### Key technical tasks:
- Selected only relevant columns (performance, demographics, school type, location).
- Removed null values in score fields to ensure reliability.
- Standardized key variables (e.g., mapping race codes, renaming columns).
- Converted coded values to numerical and categorical labels to facilitate future visualizations.
- Created a centralized and consistent base of datasets, ready for further analysis.

[Google Drive Folder with CSVs](https://drive.google.com/drive/folders/1KDu01qQci2CRJyXFd1AjCy5z0Wvtm3pj?usp=sharing)

---

## Sprint 4 — Exploratory analysis and dataset integration

In Sprint 4, exploratory analysis was conducted using data from **2021 to 2023**, with additional comparison to previous years for historical context.

### General observations:
- Average ENEM scores in **Math and Language** remained relatively stable (around 500 points), with small variations across the years.
- **Math scores showed greater variance**, indicating broader inequality in exact sciences education.

### Regional patterns:
- **Southeast and South** regions consistently showed better performance and higher participation.
- **North and Northeast** regions displayed lower average scores, revealing long-standing disparities.

### Data engineering highlights:
- Merged 2021, 2022, and 2023 datasets using `pd.concat()`
- Cleaned and standardized variables:
  - Gender: `"M"` → `"Male"`, `"F"` → `"Female"`
  - Race: `1` → `"White"`, `2` → `"Black"`, etc.
  - Income and parental education categories were also mapped
- Exported final dataset in UTF-8 CSV format


```df_final.to_csv('/content/drive/MyDrive/Final Project - Inteli/Datasets/enem_2021_to_2023.csv')```


## Sprint 5 — Final analysis

In this final sprint, the project reached its most important stage: transforming processed ENEM microdata into a functional, interactive visualization tool for Instituto Ponte.

### Visual analyses and findings

Using Google Sheets connected to BigQuery, a series of interactive and dynamic dashboards were created based on ENEM data from 2021 to 2023. These dashboards present aggregated educational performance data across multiple dimensions:

- **Family income:** Clear and consistent correlation between income brackets and student scores, with performance increasing alongside income.
- **School type:** Significant disparities in average scores between public and private school students.
- **Race/ethnicity:** Participant distribution was mapped across racial groups, revealing underrepresentation of Black and Indigenous students.
- **Gender:** Analysis highlighted gender-specific strengths — males scored higher in Mathematics, while females performed better in Writing.
- **State-by-state averages:** Regional comparison revealed inequality, with Southeast states showing better performance on average.
- **Age group:** Score variation was also observed across age ranges, with younger candidates typically performing better.


### Data infrastructure and query Design

To ensure performance and scalability:
- Data from ENEM 2021–2023 was **pre-aggregated using SQL queries in BigQuery**.
- Google Sheets pulled **only summarized results**, reducing processing time and staying within the platform's row limits.
- Charts were designed to **automatically update** when data is refreshed in BigQuery.

### Visualizations built

The following charts were developed and tested:

- **Average ENEM Scores by family Income**
- **Average ENEM Scores by school type**
- **Participant distribution by race**
- **Average scores by gender**
- **Math scores by state**
- **Scores by age group**

These visual tools were selected for their clarity and decision-making value, enabling Instituto Ponte to better understand where and how to direct its efforts.

📄 [Access the live dashboard in Google Sheets](https://docs.google.com/spreadsheets/d/1lC_Qd7Vl2u-c9MKh5pJuHD0hbFHxbsFgzuWxBf887iU/edit?usp=sharing)

### Value delivered

This sprint finalized the delivery of a powerful, interactive tool that:
- Consolidates ENEM data into an accessible and visual format
- Supports Instituto Ponte in identifying underserved populations
- Enables data-driven decisions for student support, regional outreach, and program planning


