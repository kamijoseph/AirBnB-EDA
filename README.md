# Airbnb Exploratory Data Analysis (EDA)

## Project Overview

This project performs an end-to-end **exploratory data analysis (EDA)** on Airbnb listing data to uncover pricing patterns, availability dynamics, host behavior, and location-based trends.
The objective is not prediction, but **understanding**: identifying structural relationships, anomalies, and actionable insights that can inform pricing strategy, market positioning, and future modeling work.

The analysis follows a disciplined data workflow: data inspection, cleaning, univariate and multivariate exploration, and insight synthesis.

---

## Objectives

* Understand the **distribution and drivers of listing prices**
* Analyze **availability patterns** across listings
* Examine **host characteristics** and their relationship to performance
* Identify **geographic and room-type effects**
* Surface **data quality issues** relevant for downstream modeling

---

## Dataset Description

The dataset consists of Airbnb listings with features typically including:

* Listing price
* Room type
* Location (neighborhood / coordinates)
* Availability metrics
* Host-related attributes
* Review and engagement indicators

The dataset is assumed to be observational, noisy, and non-stationary—reflecting real marketplace conditions rather than curated experimental data.

---

## Methodology

### 1. Data Inspection & Quality Assessment

* Schema inspection and data types validation
* Missing value analysis
* Duplicate and outlier detection
* Initial sanity checks on price and availability ranges

This stage establishes **trust boundaries** for the dataset.

---

### 2. Data Cleaning

* Handling missing and inconsistent values
* Price normalization (removal of symbols, coercion to numeric)
* Outlier treatment where extreme values distort distributional insight
* Feature type corrections

Cleaning decisions are conservative to preserve signal.

---

### 3. Univariate Analysis

* Price distributions and skewness
* Availability distributions
* Room type frequency analysis
* Host listing counts

This answers: *What does a “typical” Airbnb listing look like?*

---

### 4. Bivariate & Multivariate Analysis

* Price vs room type
* Price vs availability
* Host activity vs pricing
* Neighborhood/location effects

This answers: *What actually influences price and availability?*

---

### 5. Visualization

* Histograms and density plots for distributions
* Boxplots for comparative analysis
* Scatter plots for relationship discovery
* Aggregated plots for neighborhood-level insights

Visualizations are used as **diagnostic instruments**, not decoration.

---

## Key Insights (High-Level)

* Prices exhibit strong **right-skew**, with a small number of premium listings dominating the upper tail.
* **Room type** is a primary structural driver of price differences.
* Availability patterns suggest **strategic host behavior**, not randomness.
* Certain locations command consistent price premiums independent of other features.
* Raw data contains noise that must be addressed before any predictive modeling.

---

## Tools & Libraries

* **Python**
* **Pandas** – data manipulation
* **NumPy** – numerical operations
* **Matplotlib / Seaborn** – visualization
* **Jupyter Notebook** – interactive analysis

---

## Limitations

* Observational data → correlation ≠ causation
* Temporal effects (seasonality) not explicitly modeled
* Geographic analysis limited by granularity of location data

These constraints are acknowledged, not ignored.

---

## Future Work

* Feature engineering for price prediction models
* Time series analysis on availability and pricing
* Clustering listings by market behavior
* Integration into a dashboard (Tableau / Streamlit)

---