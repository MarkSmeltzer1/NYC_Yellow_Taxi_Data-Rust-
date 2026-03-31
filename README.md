# NYC Taxi Data Analysis (Rust + DataFusion)

## Overview

This project analyzes large-scale NYC Yellow Taxi trip data to extract insights on ride patterns, revenue trends, and customer behavior.

The dataset contains millions of taxi trip records including timestamps, locations, fares, and payment types, enabling real-world data analysis at scale.

---

## Problem Statement

The goal of this project is to:

* Analyze trip volume and revenue trends over time
* Understand customer tipping behavior
* Identify patterns in ride frequency and payment methods

---

## Dataset

* NYC Yellow Taxi trip data
* Includes:

  * Pickup & dropoff timestamps
  * Trip distance
  * Fare amount
  * Tip amount
  * Payment type

---

## Approach

### Data Processing

* Loaded large-scale Parquet datasets using Apache DataFusion
* Filtered and cleaned inconsistent or out-of-range records
* Aggregated data by month and payment type

### Analysis Performed

* Trips and revenue by month
* Average fare and trip counts
* Tip behavior by payment type (tip rate and averages)

---

## Key Results

* Identified monthly revenue and demand trends across the dataset
* Analyzed tipping patterns across different payment methods
* Demonstrated ability to process and analyze large-scale datasets efficiently using Rust

---

## Technologies Used

* Rust
* Apache DataFusion
* Apache Arrow

---

## Key Learnings

* Working with large-scale, real-world datasets
* Data aggregation and performance optimization
* Translating raw data into actionable insights

---

## Future Improvements

* Add visualization dashboards
* Implement forecasting models (time-series)
* Integrate SQL-based querying interfaces
