# Water quality data - work packages 3 and 5

## Overview
- A data package for water quality monitoring, including Water_quality_data.csv and supporting metadata files.
- Metadata and methodology files provide context for interpreting measurements and sites.
- Intended to support consistent assessment of environmental health and policy performance over time.

## Data files and structure
- Water_quality_data.csv
  - Core fields: 
    - SiteRef: unique site code for each sampling location (BCN, TYC, DOL are estuarine; others are freshwater)
    - SiteName: unique site name
    - Trip: field trip identifier; indicates how samples were collected (single sampling, autosampler, or short multi-day sampling). A 3-digit code is used for intermediate dates.
    - Date: sampling date
    - Time: sampling time
  - Determinand values
    - All determinand values include a qualifier (usually blank; sometimes "<")
    - pH data: original pH values were incorrect during a period due to instrument failure. Original values are in pHUncorrected. Values flagged with an “x” in the qualifier are those considered incorrect and were approximately corrected using alkalinity; the pH column contains a mix of correct and corrected values.
  - Data completeness
    - Blank fields = missing data
    - Zeros = measured values
  - Additional column details are provided in Determinand_list.csv

- Sampling_sites.csv
  - SiteName: unique site name
  - SiteRef: unique site code
  - Type: Fresh or Saline (Fresh/Saline indicate tidal influence)
  - Sampling: Spot or Continuous sampling
  - Easting/Northing: National Grid coordinates

- Determinand_list.csv
  - Provides definitions and details for each determinand (i.e., what each column in Water_quality_data.csv represents)

- Particulate_matter_method.rtf
  - Methodology information for the analysis of certain particulates

## Data collection and sampling
- Trip and sampling method
  - Trip reflects the field campaign during which samples were collected.
  - Sampling could be single, spot, autosampler, or extended multi-day collection.
- Site characteristics
  - Estuarine sites (e.g., BCN, TYC, DOL) vs freshwater sites.
  - Tide state influences sample type (Fresh vs Saline) and sampling approach.

## Data quality and interpretation
- Qualifiers indicate data quality and special cases (e.g., "<" for below detection or similar).
- pH measurements include uncorrected values (pHUncorrected) for periods of instrument error; corrected values are reflected in the pH column where applicable.
- Missing data and measured zeros are explicitly indicated in the dataset.

## Usage and accessibility
- Data are structured to support standardized analysis and reporting of environmental health over time.
- Outputs are typically presented as reports, maps, and charts, and datasets are stored and uploaded to appropriate data portals for repository and accessibility.

## Practical notes for analysts
- Always consult Determinand_list.csv for column meanings and measurement details.
- Be mindful of periods with pH correction, and rely on pHUncorrected for original measurements where appropriate.
- Use Sampling_sites.csv to link samples to precise locations and seawater/freshwater context, including tidal influence and sampling type.