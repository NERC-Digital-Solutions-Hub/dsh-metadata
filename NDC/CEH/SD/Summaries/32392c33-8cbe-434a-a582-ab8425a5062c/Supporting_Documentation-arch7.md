# Water quality data - work packages 3 and 5

## Overview
- A data package for water quality generated from field sampling, intended for GIS-based visualization and analysis.
- Main data file is Water_quality_data.csv, with supporting metadata in Sampling_sites.csv and Determinand_list.csv, plus Particulate_matter_method.rtf for methodology context.
- Data supports map-based inspection of spatial patterns, temporal trends, and relationships between sites, sampling trips, and measured determinands.

## Data files and contents
- Water_quality_data.csv
  - Core data table with samples and measured determinands.
  - Includes site and trip identifiers, date and time of sampling, and determinand values with qualifiers.
  - Notable columns: SiteRef, SiteName, Trip, Date, Time, determinand values, pH-related fields (pHUncorrected and pH), and qualifiers indicating data status.
- Sampling_sites.csv
  - Metadata about sampling locations.
  - Key fields: SiteName, SiteRef, Type (Fresh or Saline), Sampling (Spot or Continuous), Easting, Northing (National Grid).
- Determinand_list.csv
  - Details for each determinand column in Water_quality_data.csv (what each column measures, units, etc.).
- Particulate_matter_method.rtf
  - Methodology information for the analysis of certain particulates.

## Data model and key fields
- Site linkage and geography
  - SiteRef links Water_quality_data.csv to Sampling_sites.csv.
  - Easting and Northing provide spatial coordinates in the UK National Grid for GIS mapping.
  - Type indicates water body class (Fresh or Saline) and sampled locations with tidal influence.
- Sampling and time
  - Trip indicates the field campaign context: single hand sample, stage-triggered autosampler, or extended sampling over 1–2 days.
  - Date and Time specify when each sample was collected.
  - Trip encoding includes a 3-digit code for intermediate trips when additional samples were collected.
- Determinands and data quality
  - Water_quality_data.csv contains multiple determinand columns; specifics are defined in Determinand_list.csv.
  - Qualifier field accompanies determinand values (e.g., blank or other codes) to flag data status.
  - pH data shows historical instrument issues; pHUncorrected contains original values, and some pH values in pH are a mix of correct and corrected values.
  - Corrected pH values were approximately adjusted using alkalinity data.
  - Blank fields indicate missing data; zeros are recorded values.
- Specialized methods
  - Particulate_matter_method.rtf provides methodology details for analyzing certain particulates, informing interpretation of related determinands.

## Spatial and GIS considerations
- Each sample can be georeferenced via Easting/Northing in Sampling_sites.csv, enabling spatial visualization (points, density maps, time-enabled layers).
- Estuarine vs. freshwater sites (e.g., estuarine sites BCN, TYC, DOL) can be distinguished and analyzed for tidal influences.
- The dataset supports joining time-series analysis at each site across trips, enabling spatial-temporal visualizations.

## Data quality, caveats, and handling guidance
- Data quality issues to note
  - pH data: mixture of correct and corrected values; use pHUncorrected for original values and interpret the pH column with awareness of corrections.
  - Qualifiers accompany determinand values; review qualifiers to assess data reliability.
  - Missing data: blank fields indicate non-measured variables for a sample.
  - Zeros are legitimate measured values; do not treat as missing.
- Data preparation considerations for GIS
  - Join Water_quality_data.csv with Sampling_sites.csv on SiteRef to obtain coordinates and site attributes.
  - Use Determinand_list.csv to understand the meaning and units of determinand columns before visualization.
  - Refer to Particulate_matter_method.rtf when mapping or interpreting particulate-related measurements.

## Practical GIS workflows
- Map creation
  - Plot sample locations using Easting/Northing from Sampling_sites.csv.
  - Color-code or symbolize by major determinands or composite indices, with time-enabled animation by Trip/Date.
- Data integration and cleaning
  - Join main data with site metadata for coordinates and water type.
  - Validate pH values by cross-referencing pHUncorrected and pH, applying appropriate corrections where necessary.
  - Account for missing data by flagging or masking blank fields during visualization.
- Analysis opportunities
  - Compare freshwater vs. estuarine sites across trips and dates.
  - Assess spatial patterns in key determinands and their temporal evolution.
  - Integrate particulate matter methodology insights when mapping relevant particulate measurements.

## Provenance and additional resources
- Determinand_list.csv provides column-level definitions for determinand measurements.
- Particulate_matter_method.rtf contains the analytical methodology for certain particulates, aiding interpretation of related data.
- Sampling_sites.csv and Water_quality_data.csv are the primary geospatial and attribute data sources, with date/time, site, and measurement details enabling GIS-driven analysis.