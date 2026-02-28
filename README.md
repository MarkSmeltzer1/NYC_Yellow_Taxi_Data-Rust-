# NYC Taxi Aggregations with DataFusion (Rust)

## What the project does
- Loads NYC TLC Yellow Taxi trip data for the year 2025 from Parquet files using Apache DataFusion.
- Computes two required aggregations using both the DataFusion **DataFrame API** and **SQL**.
- Cleans the dataset by filtering trips to pickup year = 2025 to remove out-of-year records present in the raw data.
- Prints readable aggregation tables to the terminal and reports successful completion.

## Aggregations

### Aggregation 1: Trips and revenue by month
Groups trips by pickup month (derived from `tpep_pickup_datetime`) and computes the total number of trips, total revenue (sum of `total_amount`), and average fare (average of `fare_amount`) for trips in 2025.

### Aggregation 2: Tip behavior by payment type
Groups trips by `payment_type` and computes the total number of trips, average tip amount (average of `tip_amount`), and tip rate (sum of `tip_amount` divided by sum of `total_amount`) for trips in 2025.

## Dataset source
NYC TLC Trip Record Data (Yellow Taxi):  
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## How to download the data
The dataset was downloaded manually from the NYC TLC website.

Steps:
1. Visit the NYC TLC Trip Record Data page.
2. Download the **Yellow Taxi trip data** for each available month of 2025 in **Parquet** format.
3. Place the downloaded Parquet files into a local `data/` directory in the project root.
4. The `data/` directory and `.parquet` files are gitignored and are not committed to the repository.

## How to run the project
From the project root directory:

```bash
cargo run