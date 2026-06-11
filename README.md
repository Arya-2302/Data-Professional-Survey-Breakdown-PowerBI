# 📊 Data Professional Survey Analysis Dashboard

## Executive Summary

The **Data Professional Survey Analysis Dashboard** is an interactive Power BI solution developed to analyze survey responses from **628 data professionals** across multiple countries, industries, and job roles. The dashboard provides data-driven insights into salary trends, programming language preferences, career satisfaction, work-life balance, and the perceived difficulty of entering the data industry.

By transforming raw survey data into meaningful visualizations, this project demonstrates the application of data cleaning, transformation, modeling, and business intelligence techniques to support informed decision-making.

---

## 🎯 Business Objective

The primary objective of this project is to explore and answer key questions relevant to aspiring data professionals, recruiters, hiring managers, and organizations:

* Which data-related roles offer the highest compensation?
* What programming languages are most commonly preferred by data professionals?
* How satisfied are professionals with their salaries and work-life balance?
* How challenging is it to break into the data industry?
* Which regions contribute the most to the global data workforce?

---

## 📂 Dataset Overview

The dataset consists of survey responses collected from **628 data professionals** and includes information across the following dimensions:

### Demographics

* Age
* Gender
* Country
* Education Level
* Ethnicity

### Professional Information

* Current Job Role
* Industry
* Career Transition Status

### Compensation Data

* Salary Range

### Satisfaction Metrics (Scale: 0–10)

* Salary Satisfaction
* Work-Life Balance
* Coworker Satisfaction
* Management Satisfaction
* Opportunities for Growth
* Technical Skills Satisfaction

### Technology Preferences

* Favorite Programming Language

### Career-Related Insights

* Difficulty Breaking into the Data Industry
* Most Important Factor When Changing Jobs

---

## 🧹 Data Preparation and Transformation

Data preprocessing and transformation were performed using **Power Query** to ensure data quality and consistency before analysis.

### Key Data Cleaning Activities

#### Removal of Irrelevant Fields

* Eliminated unnecessary columns such as email addresses and non-essential identifiers.

#### Handling Missing Values

* Reviewed and managed null or incomplete entries across:

  * Country
  * Salary responses
  * Job roles

#### Salary Range Transformation

The original dataset contained salary information in categorical ranges. To enable quantitative analysis, salary ranges were converted into midpoint values.

| Salary Range | Midpoint Value |
| ------------ | -------------- |
| 0–40K        | 20             |
| 41K–65K      | 53             |
| 66K–85K      | 75.5           |
| 86K–105K     | 95.5           |
| 125K–150K    | 137.5          |

#### Data Type Standardization

* Age → Whole Number
* Salary → Decimal Number
* Satisfaction Scores → Whole Number

#### Data Standardization

Standardized:

* Country names
* Job titles
* Programming language categories

---

## 📈 Dashboard Components

### 1. Geographic Distribution of Respondents

**Visualization:** Treemap

Provides a country-wise breakdown of survey participants.

**Insight:**
The majority of responses originate from the United States, followed by India, indicating strong representation from established data and technology markets.

---

### 2. Average Salary by Job Role

**Visualization:** Bar Chart

Compares compensation levels across different data-related positions.

**Insight:**
Data Scientists report the highest average salaries, followed closely by Data Architects and Data Engineers. Entry-level positions and students exhibit comparatively lower compensation levels.

---

### 3. Preferred Programming Languages

**Visualization:** Stacked Bar Chart

Highlights the most commonly used programming languages among respondents.

**Insight:**
Python is the dominant language across data professions, reinforcing its importance in analytics, machine learning, and data engineering workflows.

---

### 4. Total Survey Respondents

**Visualization:** KPI Card

Displays the total number of survey participants.

**Value:**
Provides context regarding the scale and representativeness of the analysis.

---

### 5. Average Age of Respondents

**Visualization:** KPI Card

Displays the average age across all participants.

**Insight:**
The average respondent age of approximately 30 years suggests strong participation from early- to mid-career professionals.

---

### 6. Work-Life Balance Satisfaction

**Visualization:** Gauge Chart

Measures overall satisfaction with work-life balance.

**Insight:**
Respondents reported moderate satisfaction levels, indicating opportunities for organizations to further improve employee well-being.

---

### 7. Salary Satisfaction

**Visualization:** Gauge Chart

Measures satisfaction with compensation.

**Insight:**
Salary satisfaction scores are noticeably lower than work-life balance scores, suggesting compensation remains a concern for many professionals.

---

### 8. Salary Distribution by Gender

**Visualization:** Donut Chart

Provides a comparative view of salary representation across genders.

**Purpose:**
Supports analysis of compensation patterns and workforce diversity.

---

### 9. Difficulty Entering the Data Industry

**Visualization:** Bar Chart

Displays respondents' perceptions regarding entry into data-related careers.

**Insight:**
A significant portion of respondents perceive breaking into the data industry as moderately to highly challenging, reflecting increasing competition and skill requirements.

---

## 📊 Data Model & DAX Measures

The dashboard utilizes DAX measures to support KPI calculations and dynamic reporting.

### Total Respondents

```DAX
Total Respondents =
COUNTROWS(SurveyData)
```

### Average Age

```DAX
Average Age =
AVERAGE(SurveyData[Age])
```

### Average Salary

```DAX
Average Salary =
AVERAGE(SurveyData[Average Salary])
```

### Average Work-Life Balance

```DAX
Avg Work Life Balance =
AVERAGE(SurveyData[WorkLifeBalance])
```

---

## 🛠️ Technology Stack

* **Power BI** – Dashboard Development & Data Visualization
* **Power Query** – Data Cleaning & Transformation
* **DAX (Data Analysis Expressions)** – Calculated Measures & KPIs
* **Data Modeling** – Analytical Framework Development

---

## 📷 Dashboard Preview

<img width="2075" height="1200" alt="Survey_Project_page-0001" src="https://github.com/user-attachments/assets/81e4801c-dead-451e-85ea-9b50d6ab052f" />

