# Data Science Excel Dashboard – Bike Sales Analysis

## Project Overview

This project demonstrates how **Microsoft Excel can be used for data analysis and dashboard creation**. The analysis focuses on a bike sales dataset containing customer demographic information and purchasing behaviour using dataset from Alex the Analyst's Youtube Tutorial.

This project was created as part of learning Excel data analysis and is to be treated as a learning project only.

Tutorial reference:
https://youtu.be/opJgMj1IUrc?si=SMuCS0NZt4FcjQS-

The repository is intended for educational and portfolio purposes.

The project follows a structured **data analysis workflow**, including:

- Data cleaning
- Feature engineering
- Exploratory data analysis
- Pivot table analysis
- Interactive dashboard creation

The final output is an **interactive Excel dashboard** that allows users to analyze patterns in bike purchasing behaviour.

---

## Dataset Description

The dataset contains **customer demographic information and purchasing behavior related to bike sales**. Each row represents a customer record with demographic and socioeconomic variables.There are 1001 rows and 13 columns.

### Variables in the Dataset

| Variable | Description |
|--------|-------------|
| ID | Unique identifier for each customer |
| Marital Status | Customer marital status (Single / Married) |
| Gender | Gender of the customer |
| Income | Annual income of the customer |
| Children | Number of children |
| Education | Highest education level |
| Occupation | Customer occupation |
| Home Owner | Whether the customer owns a home |
| Cars | Number of cars owned |
| Commute Distance | Distance traveled to work |
| Region | Geographic region |
| Age | Age of the customer |
| Bike Purchase | Whether the customer purchased a bike (Yes/No) |

The **Bike Purchase** variable acts as the **target variable** used to analyze purchasing behavior.

---

## Project Workflow

The project follows a structured data analysis pipeline.The original dataset is kept as it is and a copy is created which is used as the working sheet. 

### 1. Data Cleaning

Data cleaning ensures the dataset is **accurate, consistent, and suitable for analysis**.

#### Replacing Short forms

Some categorical variables contained abbreviated values.

Example:

```
M → Married  
S → Single
```
```
M → Male
F → Female
```

Using **Find and Replace** using Ctrl+ H , these abbreviations were converted into readable labels.

---

#### Removing Duplicate Records

Duplicate rows were removed using Excel's inbuilt **Remove Duplicates** tool in the Data ribbon tab to ensure each observation represents a unique customer.

Steps:

```
Data → Remove Duplicates
```

---

#### Formatting Numeric Fields

Income values were formatted using **currency formatting** to improve readability and maintain consistency, using Home ribbon tab.

Example:

```
$45,000
$62,000
$110,000
```

---

### 2. Feature Engineering

A new categorical variable called **Age bracket** was created from the Age column using nested IFs.

This transformation helps simplify analysis and allows segmentation.

#### Age Groups

| Age Range | Category |
|----------|----------|
| < 31 | Adolescent |
| 31 – 54 | Middle Age |
| > 54 | Old |

#### Excel Formula Used

```
=IF(L2>54,"Old", IF(L2>=31,"Middle aged", IF(L2<31,"Adolescent", "Invalid")))
```
---

### 3. Exploratory Data Analysis

Exploratory analysis was conducted using **Excel Pivot Tables**.

Pivot tables enable quick summarization and comparison of data across multiple variables.

The analyses performed:

- Bike purchases by **Gender**
- Bike purchases by **Income**
- Bike purchases by **Age Group**
- Bike purchases by **Commute Distance**
- Bike purchases by **Car ownership**
- Bike purchases by **Having children**

These analyses help identify patterns and relationships in customer purchasing behavior.

---

### 4. Data Visualization

Charts were created using **Excel Pivot Charts** to visually represent patterns discovered during analysis.

Types of visualizations used:

- Line charts
- Bar charts
- Pivot charts

---

### 5. Interactive Dashboard

The final step of the project was building an **interactive Excel dashboard**.Another sheet was made for this purpose.

The dashboard integrates pivot charts and allows users to explore the data dynamically.

#### Dashboard Features

Interactive filters (slicers) were added for:

- Marital Status
- Education
- Region
- Occupation

These filters allow users to analyze bike purchase behavior across different demographic segments.

---

## Key Insights

The dashboard enables identification of several insights, such as:

- Demographic groups most likely to purchase bikes
- Relationship between income and bike purchases
- Influence of commuting distance on purchasing behavior
- Differences in purchasing patterns across age groups

Such insights can support **business decision-making** in areas such as:

- targeted marketing
- customer segmentation
- product positioning

Recommendations:

- Males, aged 31-54, who own less than 1 car are more likely to purchase a bike.
- Commute distance has a huge impact on bike sales. Customers with less than 2 miles tend to buy bikes more.
- More marketting can be pushed towards the age band of Adolescent to Middle aged group as they are more likely to buy the bikes.
- People owning no cars or 1 car have higher chance of buying bikes for shorter commute distance of less than 2 miles.

---



## Conclusion

This project demonstrates how Excel can be used as a **practical data analysis and visualization tool** for extracting meaningful insights from structured datasets.

By combining **data cleaning, feature engineering, pivot table analysis, and dashboards**, the project replicates a simplified version of a real-world **business intelligence workflow** and provides recommendations to the concerned team for further steps.
