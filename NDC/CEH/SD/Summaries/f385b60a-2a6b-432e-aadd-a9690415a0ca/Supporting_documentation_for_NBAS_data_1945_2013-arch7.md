# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013.

## Scope and purpose
- Long-term monitoring dataset for Windermere's North Basin, England, covering surface temperature, surface oxygen saturation, water clarity, water chemistry, and phytoplankton chlorophyll a.
- Timeframe extends from February 1945 to the end of 2013 for various variables; some variables began earlier than others.
- Aims to enable analysis of long-term ecological and climatic changes in a temperate lake system.

## Data and variables
- Variables and units included:
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - PH: pH
  - NH4N: ammonium (µg N per L)
  - NO3N: nitrate (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon as SiO2 (µg per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)
- Measurements are taken from a boat at a marked buoy location at the deepest part of the lake.
- Some chemistry samples are reported with “<” indicating values below detection limits.

## Sampling regime and collection methods
- Frequency: weekly or fortnightly sampling (as reported for different variables).
- Depth integration for water chemistry:
  - 0–5 m (1945–1962)
  - 0–10 m (1962–1964)
  - 0–7 m (1964 onwards)
- Site: single, fixed buoy location in the deepest part of Windermere’s North Basin.
- Origin and stewardship: data initially collected by the Freshwater Biological Association; subsequently collected by the Centre for Ecology & Hydrology (CEH) and its predecessor since 1989.

## Data quality and QC
- The dataset consists of raw data and has not been fully quality controlled or calibrated.
- Visual checks have been conducted.
- Some entries are duplicates from 2005 onwards that underwent quality checks.

## Data structure and file format
- Data are provided as a comma-separated values (CSV) file.
- Core fields:
  - sdate: date of measurement
  - variable: shorthand name (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: measured value for the corresponding variable
  - sign_if_LT_LOD: indicator if value is below detection limit (a “<” sign)
- Each column has a Description describing its content (e.g., date of measurement, variable description, value description, detection-limit indicator).

## Spatial and temporal coverage
- Spatial: Windermere, North Basin, Lake; measurements from a single fixed buoy at the deepest part of the lake.
- Temporal: February 1945 through 2013 (end of 2013 for the available data).

## Usage considerations for GIS specialists
- Suitable for time-series analysis and visualization of long-term lake dynamics at a single station.
- Can be integrated with GIS land/water layers or lake-wide layers for contextual mapping, but spatial coverage is limited to one monitoring location.
- Given raw nature and limited QC, users may want to apply quality filtering/normalization before map-based analyses or cross-dataset comparisons.
- Depth-integration changes over time (0–5 m, 0–10 m, 0–7 m) should be accounted for when comparing across periods or combining variables.

## Notable references and use cases
- Recent publications utilizing the dataset include:
  - Do early warning indicators consistently predict non-linear change in long-term ecological data? (Journal of Applied Ecology, 2016)
  - Insights into perch population and ecology from a 70-year Windermere time series (2015)
  - Various studies on climate, phenology, and ecosystem dynamics in freshwater systems leveraging long-term Windermere data (listed in the document)