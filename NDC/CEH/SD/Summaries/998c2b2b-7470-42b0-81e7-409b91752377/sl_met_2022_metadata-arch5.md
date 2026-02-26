# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Dataset from a 12 m mast at the Queensberry Estate, Sri Lanka (coordinates 6.9693°, 80.5911°, altitude 1645 m).
- Time period: 17 March 2022 to 31 December 2022.
- Purpose: supports the ammonia enhancement experiment; wind conditions below the forest canopy influence the experiment.
- Data cadence: measurements every 20 seconds with 15-minute averages; data provided in Sri Lanka Standard Time (SLST).

## Data Collection Details
- Sensors measure across multiple heights and layers:
  - Above and below forest canopy for wind, temperature, humidity, radiation, and related variables.
  - Leaf wetness at multiple positions (LWS1–LWS4).
  - Air temperature (AirT1–AirT4) and relative humidity (RH1–RH4) at various heights.
  - Soil measurements at multiple depths: soil volumetric water content (Soil_VWC1–Soil_VWC3), soil electrical conductivity (Soil_EC1–Soil_EC3), soil temperature (Soil_T1–Soil_T3).
  - Wind, PAR (photosynthetically active radiation), and total solar radiation (Below- and Above-canopy).
  - Meteorological variables including wind speed/direction (WXT_WS/WXT_WD, below and above canopy), air temperature (WXT_AirT), relative humidity (WXT_RH), barometric pressure (WXT_BP).
- The setup includes instrument details (manufacturer and model) and descriptive notes for each parameter.
- Data file format: CSV with 37 parameters across 27,812 measurements.

## Quality Control
- Data visually checked; obvious instrument errors, datalogger issues, and power-cut artifacts removed.
- Gaps present due to time required to replace faulty sensors.
- Quality control notes tied to instrument performance and deployment conditions.

## Data Structure and Metadata
- Data file contains 27,812 measurements of 37 parameters.
- Columns include:
  - Timestamp (and related fields such as Height, Manufacturer, Instrument, Description).
  - Parameter-specific rows (e.g., LWS1, LWS2, LWS3, LWS4; AirT1–AirT4; RH1–RH4; Soil_VWC1–Soil_VWC3; Soil_EC1–Soil_EC3; Soil_T1–Soil_T3; WS_Cup1–WS_Cup2; PAR1–PAR2; Total_Solar1–Total_Solar2; WXT_WS1–WXT_BP2; WXT_AirT1–WXT_RH2; WXT_BP1–WXT_BP2, etc.).
- Descriptions for each field specify height (m), location relative to canopy (ground flora layer, below canopy, or above canopy), units, and instrument details.
- Time reference: 15-minute timestamps formatted as dd/mm/yyyy hh:mm.
- Time zone: Sri Lanka Standard Time (SLST).
- Data provenance is linked to a publication detailing the experimental design and methodology (Deshpande et al., 2024).

## Provenance, Access and Related Work
- Complete details of the experimental design, methodology, analysis, and findings are described in Deshpande et al. (2024).
- Funding for establishing the facility: UKRI GCRF South Asian Nitrogen Hub.
- Primary reference for dataset: Deshpande AG et al., Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024.

## Governance and Stewardship Considerations
- Documentation is comprehensive: multi-height, multi-sensor measurements with clear metadata (instrument, height, description, unit, and format).
- Time-stamped data supports reproducibility and跨-layer analyses (below-canopy vs above-canopy conditions).
- Quality control procedures are documented, including handling of instrument faults and data gaps.
- Data is positioned to support sharing and discovery alongside related datasets and portal catalogues, with explicit links to methodological publications for full context.
- Potential data-use considerations for stewards include:
  - Tracking and recording any future updates or reprocessing due to instrument changes.
  - Maintaining consistency in units and timestamp formats to ensure interoperability with other datasets.