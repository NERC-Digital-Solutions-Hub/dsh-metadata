# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

## Overview
- Two sampling sites in a rural dwelling in South Lanarkshire: indoors (hall) and outdoors (garden). Garden backs onto grassland part of a large dairy farm.
- Sampling operator duties are performed by the dwelling owner; analysis is conducted by the Centre for Ecology and Hydrology Edinburgh.
- UKCEH ALPHA® passive samplers used to measure ammonia concentrations. Samplers are exposed in monthly cycles at the start of each month.
- The final dataset referenced is NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv, with site names and spatial identifiers provided in accompanying pages.

## Sampling method and deployment
- UKCEH ALPHA® sampler uses a citric acid coated filter to capture NH3; a white PTFE (Teflon) membrane protects the filter; membrane faces downward during exposure.
- Replicate samplers deployed at each site to improve reliability.
- Samplers mounted on a shelter on a pole at about 1.5 m above ground.
- Exposed samplers are protected in plastic containers when not in use.

## Analysis and data processing
- Analysis performed by extracting samplers into deionised water; NH3 concentration determined by SEAL AA3 via colorimetry.
- NH3 concentration in air calculated from ammonium concentration using a fixed uptake rate of 0.003241315 m3 h-1 and the exposure duration (in hours).
- Data quality flagged to highlight concerns (details on page 4 of the source).

## Quality assurance and data validity
- Raw data quality assessment rules:
  - Coefficient of variation (CV) of replicates < 15%: if CV > 15%, replicates reviewed; if the average is representative, data are valid and flagged as 103.
  - Values above calibration range but still valid: if dilution is not possible due to instrument failure or sample loss, results may still be valid.
  - Missing data or metadata: indicated by -9999; concentration cannot be calculated if essential date/time metadata are missing.
- The final dataset contains accepted data values with appropriate flags.

## Dataset structure and contents
- Dataset name: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv.
- Each row represents one month of data for a single site (indoor or outdoor).
- Core columns include:
  - Site name, start date, end date, ammonia concentration for the period (units: µg NH3 m-3), data flag.
  - Additional fields include site id, network id (RSW), parameter id (alpha_NH3_g), measurement start/end dates and times, flagging fields (less than detection limit, verification id, unit id, data capture percentage, validity, EMEP codes), Month-Year, and Comments.
- Units for concentration: micrograms of NH3 per cubic metre of air (µg NH3 m-3).
- Data capture and validity fields indicate data completeness and quality, with associated EMEP flags.

## Data flags and QA flags (EMEP)
- EMEP flag codes are provided to describe data status and quality (e.g., detection limits, representativeness of sampling period, contamination, etc.). Examples include a range of codes such as 999, 781, 780, 654, 653, 652, 651, 260, 103, 460, and others, each with specific meanings related to data capture, validity, and context.
- These flags help assess whether a given monthly measurement is valid, partially valid, or invalid due to various factors (e.g., contamination, low CV, detection limits).

## Site information and spatial metadata
- Inside site:
  - Start date: 01/01/17; End date: Ongoing.
  - Latitude: 55.64072; Longitude: 3.59705.
  - Height of air inlet above ground: 1.5 m.
  - Details: Located in the hall of the dwelling.
- Outside site:
  - Start date: 01/01/17; End date: Ongoing.
  - Latitude: 55.64072; Longitude: 3.59705.
  - Height of air inlet above ground: 1.5 m.
  - Details: Located in the garden of the dwelling.

## GIS considerations and use in map products
- Use two point features (indoors and outdoors) per dwelling, with shared coordinates but different location_type attributes (Indoor vs Outdoor), both at 1.5 m height.
- Attributes to map or filter:
  - Monthly NH3 concentrations (µg NH3 m-3) with the corresponding Month-Year.
  - Data quality flags (CV-based validity, calibration-range status, missing data indicators, and EMEP flag codes) to filter for high-quality data.
  - Verification and data capture fields to assess reliability.
- Potential visualizations:
  - Time-series plots of NH3 concentration for each site type (indoor vs outdoor).
  - Spatial layer showing two features for the dwelling with time-enabled attributes to display monthly concentrations.
  - Layered maps that annotate data quality (e.g., flags) alongside concentrations.
- Data provenance and context to aid interpretation in GIS:
  - Sampling method (ALPHA®, passive, monthly cycles).
  - Height and placement details (1.5 m, indoors hall vs garden outdoors).
  - Analysis method (SEAL AA3 colorimetry) and uptake-rate-based conversion to ambient NH3.

## Access to data
- Primary dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv.
- Spatial identifiers and site details are provided in accompanying pages (e.g., page 3 for dataset contents; page 5 for site names).
- The dataset supports map-based exploration of indoor vs outdoor ammonia environments at the rural dwelling, with explicit quality and metadata fields to support GIS analysis.