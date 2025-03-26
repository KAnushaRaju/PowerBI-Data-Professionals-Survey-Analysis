# 📊 Power BI Project: Data Professional Survey Dashboard

Welcome! This repository contains an interactive Power BI dashboard built using a real-world survey dataset collected from data professionals. The project focuses on transforming, analyzing, and visualizing survey data using Power BI Desktop as a beginner-friendly portfolio project.

---

## 📁 Project Overview

The dataset was collected via an online survey shared on LinkedIn and Twitter and contains responses from over **630 data professionals** around the world.

This dashboard provides insights into:
- Job titles and average salaries
- Programming language preferences
- Gender-based salary comparison
- Work-life balance and salary satisfaction
- Difficulty in breaking into data careers
- Age and country demographics

---

## 📥 Dataset

- **Source:** Public survey data collected by Alex The Analyst
- **Format:** CSV file (imported into Power BI)
- **Data Columns Include:**
  - Job Title
  - Current Yearly Salary (ranges)
  - Industry
  - Programming Language
  - Work-life Balance, Management, Co-workers, Upward Mobility, etc.
  - Country, Gender, Age
  - Career Difficulty & Preferences

> ⚠️ All data is anonymous. No personal identifying information was collected.

---

## 🧹 Data Cleaning & Transformation (Power Query Editor)

All transformation steps were performed using Power Query within Power BI. Key transformations include:

### 🔻 Column Cleanup
- Removed unneeded fields (emails, time spent, internal IDs).

### 🧑‍💼 Job Title Simplification
- Grouped similar job roles to reduce clutter.
- Examples:
  - “Software Engineer (with AI)” → “Software Engineer”
  - “Other (please specify)” → "Other"

### 💰 Salary Column Cleanup
- Original values were in text ranges, e.g. `"106k - 125k"`.
- Used `split column` and `replace values` to extract lower and upper bounds.
- Created a new column `Average Salary`:
  - Formula: `(Lower Bound + Upper Bound) / 2`

### 💻 Programming Language
- Grouped custom free-text inputs into a clean category.
- Preserved main languages (Python, SQL, R, etc.), others grouped under "Other".

### 🌍 Country & Industry
- Grouped uncommon entries into “Other” to improve readability.
- Trimmed and cleaned inconsistent values.

---

## 📊 Visualizations

The final dashboard includes the following visuals:

| Visualization | Description |
|---------------|-------------|
| **Cards** | Total respondents, average age |
| **Bar Chart** | Average salary by job title |
| **Column Chart** | Favorite programming language |
| **Tree Map** | Country-wise respondent breakdown |
| **Gauge Charts** | Happiness with work-life balance and salary (scale of 0–10) |
| **Donut Chart** | Average salary by gender |
| **Stacked Bar** | Difficulty level in breaking into data roles |

![Dashboard Screenshot](images/dashboard.png)

