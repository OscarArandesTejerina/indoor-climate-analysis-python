# Indoor Climate & Energy Analysis (Python)

A time-series analysis of indoor environmental sensor data from a two-floor building, carried out in Python with pandas, NumPy, and matplotlib. The project examines how indoor temperature, humidity, and air quality behave over time, how they relate to outdoor conditions and HVAC setpoints, and how well each floor stays within its target comfort range.

## Overview

The data comes from environmental sensors on the ground and first floors of a building, recording temperature, humidity, air quality, and heating/cooling setpoints over time. Starting from raw, unordered records, the project cleans and structures the data, visualizes it across multiple time scales, and analyzes indoor climate and thermal comfort.

## Workflow

**1. Data understanding and preparation.** Loading data from a two-sheet Excel file, converting timestamps to a datetime index, sorting chronologically (the raw data was in reverse order), converting sensor readings from text to numeric types, and handling missing values.

**2. Time-series visualization.** Plotting indoor temperature at hourly, daily, weekly, and monthly scales, comparing indoor and outdoor temperature, tracking humidity trends, and visualizing heating and cooling setpoints together with indoor conditions.

**3. Relationships between variables.** Computing Pearson correlation coefficients between pairs of variables (outdoor vs. indoor temperature, humidity vs. air quality, setpoints vs. indoor conditions) to quantify their linear dependence.

**4. Setpoint and comfort analysis.** Engineering a season-dependent temperature-error feature (measured against the heating setpoint in the cold season and the cooling setpoint in the warm season) and counting significant deviations from target comfort conditions over time.

**5. Floor comparison.** Comparing the two floors by average temperature, temperature fluctuation, and comfort deviation.

## Key Findings

- Indoor temperature is moderately-to-strongly correlated with outdoor temperature (≈ 0.69–0.78 on both floors), showing outdoor conditions still influence indoor climate despite HVAC regulation.
- Most other relationships between air quality, humidity, and setpoints are weak, indicating limited direct linear dependence.
- Comfort deviations are concentrated in specific periods (notably early 2021), becoming rare afterward before reappearing in 2024–2025.
- The two floors have similar temperature fluctuation (SD ≈ 3.2 °C), with the first floor slightly warmer on average.

## Techniques

Data cleaning and type conversion · datetime indexing · time-series resampling · correlation analysis · feature engineering · aggregation and comparison · data visualization

## Repository Contents

```
indoor-climate-analysis/
├── README.md
├── data.xlsx                       # Sensor data (ground floor + first floor)
└── indoor_climate_analysis.ipynb   # Full analysis notebook with narrative and plots

```

## Tech

Python · pandas · NumPy · matplotlib
