# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013.

## Overview
- Long-term monitoring dataset from Derwent Water, Cumbria, England, covering 1990–2013. 
- Fortnightly sampling regime for: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Water chemistry samples integrated from 0–5 m; measurements taken from a boat at the deepest lake buoy; shore sampling when buoy access was not possible (Flag 2).
- Data available for download as a CSV with columns for Date, Variable, Value, and associated metadata.

## Sampling regime and collection methods
- Sampling location: Derwent Water, deepest part (buoy), with occasional shore sampling when buoy access was blocked.
- Frequency: fortnightly sampling from August 1990 to end of 2013.
- Depth integration: water samples integrated from 0–5 m; measurements cover a range of physical, chemical, and biological parameters.
- Data descriptors: included in the dataset are units for each variable and a flag indicating sample location.

## Quality control and data quality
- Raw data: not yet quality controlled or calibrated (except for double entries from 2005 onwards).
- Visual checks conducted for data quality.
- Known data gaps: March–June 2001 due to foot-and-mouth disease restricting lake access; partial data loss in 2009 due to weather.
- Documentation of missing and detection-limit information is provided via sign indicators and flags in the data matrix.

## Data structure and metadata
- File format: comma-separated values (CSV).
- Core columns:
  - Date: date of measurement.
  - Variable, Description: name and description of each measured parameter (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value, Description: numeric measurement for each variable.
  - Sign_if_LT_LOD, Description: indicates if the value is below the detection limit, using a < sign.
  - Flag, Description: 1 = sample taken at the buoy; 2 = sample taken from the shore (buoy visit not possible).
- Documentation notes: current dataset consists of raw values with accompanying indicators for detection limits and sampling location, suitable for layering quality control in a later step.

## Limitations, gaps, and considerations for reuse
- Quality control status: data require calibration and formal QC before high-precision analyses.
- Gaps: notable missing period (Mar–Jun 2001) and some 2009 data due to weather; users should account for these gaps in analyses.
- Interoperability: potential heterogeneity in collection circumstances across years (e.g., occasional shore samples) and the need for consistent integration of flags and LOD indicators.
- Provenance and context: dataset accompanied by literature references demonstrating usage in climate and lake-water studies; supports longitudinal analyses of lake physical and chemical properties.

## Usage and references
- Recent publications using this dataset include studies on climate impacts and lake productivity, illustrating the dataset’s value for historical trend analysis and environmental research.
  - Examples: studies on climate change effects on larger lakes in the English Lake District; catchment productivity and CO2 emissions; long-term case histories of species introductions and lake responses.