# Supporting document for diurnal soil nitrous oxide emission datasets

## Overview
- Supporting dataset compilation for the study “Diurnal variability in soil nitrous oxide emissions is a widespread phenomenon” intended for Global Change Biology.
- Focused on diurnal N2O flux measurements extracted from 46 published articles (1983–2019).

## Data types and structure
- Four data types:
  - N2O_xxx.csv: time of flux measurement, N2O flux (μg N2O-N m-2 h-1), normalised flux (N2Onorm) within a 24-hour cycle.
  - soil_temp_xxx.csv: time of measurement and soil temperature at 5–10 cm depth (°C) within a 24-hour cycle.
  - dataset_info.csv: literature title and non-diurnal parameters (e.g., pH, bulk density, soil texture, season, soil water-filled pore space, irrigation, grazing) for each dataset.
  - diurnal_pattern_categorisation_data.csv: processed data including timing of maxima/minima, cumulative flux metrics, and diurnal pattern classifications.
- Each dataset (N2O_xxx) pairs with a corresponding soil_temp_xxx when available (same day and study; matched by number).

## Data collection and sources
- Systematic literature search in Web of Science Core Collection and ScienceDirect; cut-off date: 28 August 2019.
- Inclusion criteria:
  - N2O flux measured on cropland, grassland, or forest soils.
  - At least five N2O flux measurements per 24-hour cycle.
  - First and last measurements within 00:00–03:59 and 20:59–23:59, respectively.
- Result: 286 diurnal N2O flux datasets (from 46 articles); 160 datasets include soil temperature (5–10 cm), 157 include soil pH, 115 bulk density, 175 soil texture, 135 soil moisture, 261 season data.

## Data extraction and processing
- N2O flux and soil temperature data were extracted from figures using Engauge Digitizer and saved as CSV per 24-hour cycle.
- Time formatting: hours/minutes converted to decimal hours (0.00–23.99).
- Normalisation: N2Onorm = (N2Ot − N2Omin) / (N2Omax − N2Omin); scale 0–1 to remove magnitude differences across studies.

## Diurnal pattern categorisation and thresholds
- Datasets categorized into three diurnal patterns:
  - Daytime peaking (with morning or afternoon subcategories)
  - Night-time peaking
  - Non-diurnal
- Thresholds for daytime/night-time classification adjusted for each dataset:
  - Adjusted threshold = (24 / hours between first and last measurement) × 50%
- Emissions within 04:00–16:00 h, 06:00–18:00 h, and 08:00–20:00 h are used to compute 12-hour period percentages via trapezoidal integration.
- For daytime peaking:
  - Highest and second-highest N2Onorm occur between 04:30–19:30 h.
  - Lowest N2Onorm occurs between 00:00–09:00 h or 18:00–00:00 h.
  - Emission in daytime windows exceeds adjusted threshold; further sub-classified as morning or afternoon peaking.
- For night-time peaking:
  - Lowest two values occur between 04:30–19:30 h.
  - Highest value occurs between 00:00–09:00 h or 18:00–00:00 h.
  - Daytime emission percentage is below the threshold.
- Non-diurnal if neither daytime nor night-time patterns are met.

## Nature and units of recorded values
- N2O flux values standardised per 24-hour cycle (μg N2O-N m-2 h-1); times converted to decimal hours.
- Normalised flux values (N2Onorm) range from 0 to 1.
- Soil temperature values at 5–10 cm depth (°C).

## Details of data structure and fields
- N2O_xxx.csv: columns include time (hour), N2O_flux (μg N2O-N m-2 h-1), norm_flux (0–1).
- soil_temp_xxx.csv: time (hour) and soil temperature (°C).
- dataset_info.csv: for each dataset, literature title and non-diurnal parameters (pH, bulk density, soil texture, season, SWP, irrigation, grazing).
- diurnal_pattern_categorisation_data.csv: processed metrics per dataset:
  - max_hour, sec_max_hour, min_hour, sec_min_hour
  - cum_all, cum_early, cum_early_percent, cum_mid, cum_mid_percent, cum_late, cum_late_percent
  - first_condition_D, second_condition_D, third_condition_D (diurnal daytime)
  - first_condition_N, second_condition_N, third_condition_N (diurnal nighttime)
  - daytime_peaking, nighttime_peaking

## Data availability and usage
- Data enable cross-study GIS analyses of diurnal N2O emission patterns.
- Rich contextual attributes (soil properties, land use, season) support stratified mapping and regional comparisons.
- Time-normalised, standardized units facilitate integration into map-based data products and spatial analyses.

## Limitations and considerations for GIS work
- Data derived from digitised figures may introduce digitisation errors.
- Diurnal categorisation depends on the measurement window and the adjusted thresholds; some datasets cover shorter time spans.
- The compilation reflects literature up to 2019; no post-2019 updates are included.

## References and scope
- Includes 46 cited journal articles with full references available in the accompanying Reference section.