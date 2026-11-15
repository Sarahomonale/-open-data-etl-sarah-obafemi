# Lisbon Weather ETL - Sarah OBAFEMI

## Source
Open-Meteo API, no key required.
Lisbon: latitude 38.72, longitude -9.14

## How to run
1. pip install -r requirements.txt
2. python -m src.main

## What it does
1. Extract: Fetches 7 days of daily weather for Lisbon
2. Transform: Renames columns, creates temp_range_c, filters rain < 5mm, sorts by hottest
3. Load: Saves to data/processed/output.csv

## Output
Columns: date, temp_max_c, temp_min_c, rain_mm, temp_range_c
Example: Hottest day was 2026-11-17 with 21.3°C, rain 1.7mm, range 3.0°C.
Rainiest day 2026-11-18 with 8.4mm was filtered out.
Final file has 5 rows.
