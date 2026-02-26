# Elter_chlorophyll_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of chlorophyll a in the deepest point of the Elterwater inner basin.
- Timeframe: May 2018 to December 2019.
- Data capture includes depth-specific chlorophyll a concentrations.

## Data Collected
- Variables: Date (YYYY-MM-DD), Depth (m), Concentration (μg L^-1).

## Sampling Details
- Depths sampled: 0.5, 1, 2, 3, 4, 5, and 6 meters.
- Water sample size: 500 mL per sampling event.
- Sampling frequency: Weekly to monthly.
- Filtration: 500 mL water filtered immediately on collection through a 5.5 cm GF/C filter paper.
- Sample handling: Filter papers frozen; samples analyzed within one month of collection.

## Analytical Methods
- Chlorophyll a extraction: Heated methanol extraction.
- Measurement: Spectrophotometer.
  - 750 nm: background turbidity correction.
  - 665 nm: red absorbance maximum for chlorophyll a.
- Concentration calculation equation:
  - Chlorophyll a concentration = (13.9 * A_corr665 * 1/d) * v / V
  - A_corr665 = A_corr665 - A_corr750
  - d = cuvette pathlength (cm)
  - V = volume of sample filtered (mL)
  - v = volume of extract (mL)

## Data Structure
- Columns: Date (yyyy-mm-dd), Depth (m), Concentration (μg L^-1)

## Location and Timeframe
- Sampling site: Deepest point of Elterwater inner basin.
- Coordinates: 54.4287° N, -3.0350° W

## Data Handling and Storage
- Immediate filtration after sampling; filters frozen.
- Analysis conducted within one month post-collection.
- Data structured with explicit date, depth, and concentration fields for downstream analysis.

## Potential Uses and Considerations
- Time-series analysis of chlorophyll a by depth to infer phytoplankton biomass dynamics.
- Vertical profiling to study stratification and seasonal patterns.
- Potential correlations with environmental variables if integrated (e.g., temperature, light, nutrient data).
- Considerations for data quality include consistency of filtration, extraction protocol, and accurate turbidity correction (A_corr750).