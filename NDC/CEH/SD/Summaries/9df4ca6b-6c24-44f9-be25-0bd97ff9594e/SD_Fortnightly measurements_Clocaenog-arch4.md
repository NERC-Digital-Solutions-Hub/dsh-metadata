# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Fortnightly measurements.rft'

## Purpose and scope
- Provides data-structure details for two datasets collected together as Fortnightly measurements at Clocaenog (2015–2016).
- Dataset 1: site-level data.
- Dataset 2: soil respiration data, with accompanying soil temperature, soil moisture, and photosynthetically active radiation (PAR) measures.

## Datasets at a glance
- Dataset 1: Fortnightly measurments_Clocaenog_2015-2016_site.csv
  - 20 columns, 32 rows.
  - Key columns:
    - Date (Day/Month/Year).
    - Rainfall (mm) – site level.
    - Throughfall (mm) for multiple plots with treatments: Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control.
    - Water table depth entries for plots (labels include Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control).
    - Notes on units: Water table depth column L is cm; subsequent water table depth columns (M, N, O, P, Q, R, S, T) are listed with unit mm in the description.
- Dataset 2: Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv
  - 38 columns, 32 rows.
  - Key measurements per date:
    - Soil respiration (mg CO2-C m^-2 hr^-1) for Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control.
    - Soil temperature (°C) for Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control.
    - Soil moisture (Vol%) for Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control.
    - Photosynthetic active radiation (PAR) in µmol m^-2 s^-1 for Plot1–Warming, Plot2–Warming, Plot3–Control, Plot4–Drought, Plot5–Drought, Plot6–Control, Plot7–Warming, Plot8–Drought, Plot9–Control.
  - Note: The dataset includes multiple measurement blocks (respiration, temperature, moisture, PAR) aligned by date and plot/treatment.

## Metadata and labeling
- Descriptions accompany each column, indicating the measured variable and the plot/treatment it represents.
- Date column is the temporal anchor for all measurements.
- The two datasets are designed to be analyzed together for integrated understanding of site-level conditions and soil/biophysical responses.

## Data management considerations for Data Leaders
- Data integrity and alignment
  - Ensure date formats are consistent across datasets; verify that dates correspond between site and soil measurements.
  - Confirm plot-to-treatment mappings (Plot1–Plot9) are consistent across all measurement types (rainfall, throughfall, water depth, respiration, temperature, moisture, PAR).
- Units and metadata
  - Validate units across water table depth columns (cm vs. mm) to prevent misinterpretation; ensure metadata clearly documents any unit inconsistencies.
  - Maintain clear metadata describing each column’s measurement, units, and the treatment associated with each plot.
- Discoverability and accessibility
  - Store both datasets with consistent naming, versioning, and a data dictionary to support reuse by policy-makers and analysts.
  - Link these datasets to the overarching Clocaenog Fortnightly measurements documentation to provide full context.
- Quality assurance
  - Check for missing values, outliers, and any header inconsistencies that could affect downstream analyses.
  - Maintain traceability to the original data collection protocols and supporting documentation.
- Reuse and collaboration
  - The structure supports cross-team analysis (e.g., policy colleagues or partners) by providing cohesive site-level and soil measurements over time.
  - Consider publishing a consolidated metadata file that maps each PlotX–Treatment to its corresponding data columns for ease of use by external stakeholders.

## Next steps for practitioners
- Review the related Clocaenog supporting documentation for Fortnightly measurements to ensure proper interpretation of the data series.
- Prepare a data dictionary and data quality report covering both datasets.
- Verify and reconcile any unit discrepancies before analysis, and document decisions in metadata.