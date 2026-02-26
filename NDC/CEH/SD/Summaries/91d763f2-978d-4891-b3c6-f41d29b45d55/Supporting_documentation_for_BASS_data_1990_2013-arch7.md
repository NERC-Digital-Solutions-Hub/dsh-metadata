# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

## Overview
- Long-term monitoring dataset from Bassenthwaite Lake, Cumbria, England (1990–2013).
- Tracks multiple water quality and ecological parameters:
  - Surface temperature (TEMP, °C)
  - Surface oxygen saturation (OXYG, % air-saturation)
  - Secchi depth (SECC, m)
  - Alkalinity (ALKA, µg CaCO3 per L)
  - pH
  - Ammonium (NH4N, µg N/L)
  - Nitrate (NO3N, µg N/L)
  - Soluble reactive phosphate (PO4P, µg P/L)
  - Total phosphorus (TOTP, µg P/L)
  - Dissolved reactive silicon (SIO2, µg/L)
  - Phytoplankton chlorophyll a (TOCA, µg/L)

## Sampling regime and collection methods
- Fortnightly sampling from August 1990 to end of 2013.
- Water samples based on 0–5 m integrated depth.
- Typical sampling from a boat at a buoy located at the deepest part of the lake; shore samples used when buoy access was not possible (Flag 2).
- Data gaps: March–June 2001 due to Foot-and-Mouth disease restricting access.
- Data are raw (not quality controlled or calibrated) except for some duplicate entries from 2005 onward; visual checks performed.

## Data structure and format
- Delivered as a comma separated values (CSV) file.
- Key columns:
  - sdate: Date of measurement
  - variable: Description of the measurement (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: Measured value
  - sign_if_LT_LOD: Indicates if value is below detection limit (a "<" sign)
  - flag: Sampling location indicator (1 = buoy, 2 = shore)

## Quality and limitations
- Raw data without formal quality control or calibration (except some duplicate entries from 2005 onward).
- Visual quality checks performed.
- Some values below detection limits are flagged accordingly.
- Data represent measurements from the buoy location (deepest part) with occasional shore samples when buoy access was not possible.

## Spatial and GIS considerations
- Location context: sampling tied to Bassenthwaite Lake; primary data points come from buoy at the deepest part, plus shore samples.
- Potential GIS use:
  - Create time-enabled point features for each sampling event, with coordinates for buoy location and shore sampling sites.
  - Attach attributes for each variable to enable multi-layer visualisations (temperature, oxygen, clarity, nutrients, silicon, chlorophyll a).
  - Handle Flag 2 shore samples distinctly to reflect change in sampling location.
  - Depth integration (0–5 m) considerations when mapping: may require a lake-depth or vertical profile layer to contextualize measurements.

## Data usage and examples
- Dataset referenced in multiple publications for modelling and climate-related studies, illustrating its utility for:
  - Phytoplankton community modelling and nutrient dynamics
  - Assessing nutrient sources and retention in lakes
  - Evaluating potential climate-change impacts on lake habitats and phenology
  - Integrated analyses of carbon and silicon cycles in freshwater systems

## Availability and notes
- Timeframe: August 1990 – end of 2013.
- Data format: CSV with explicit columns for date, variable, value, detection-limit flag, and sampling location flag.
- Users should account for raw status and sampling-location nuances when integrating into GIS-based data products.