# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- Meteorological and environmental data collected at a 12 m mast located beside the ammonia enhancement manifold in the Queensberry Estate, Sri Lanka (coordinates: 6.9693 N, 80.5911 E; altitude 1645 m).
- Purpose: support wind-controlled NH3 enhancement experiments and estimation of ammonia deposition to forest ecosystems; extension of the 2022 dataset from the same site.
- Time frame: 1 January 2023 to 31 December 2024, Sri Lanka Standard Time (SLST).
- Data product: 70,176 measurements across 37 parameters, provided as a CSV with detailed metadata per variable; used to inform and evaluate atmospheric deposition dynamics and related monitoring frameworks.

## Data collection
- Site setup: measurements taken at four heights for several variables; data include above-canopy and below-canopy conditions to capture vertical profiles.
- Measured variables include:
  - Air variables: air temperature (AirT1–AirT4), relative humidity (RH1–RH4), leaf wetness (LWS1–LWS4)
  - Meteorological: wind speed and direction (WXT_WS1/WS2, WXT_WD1/WD2), barometric pressure (WXT_BP1/BP2)
  - Radiation: photosynthetically active radiation (PAR1–PAR2), total solar radiation (Total_Solar1–Total_Solar2)
  - Rainfall metrics: Rain, Throughfall
  - Soil: soil volumetric water content (Soil_VWC1–VWC3), soil electrical conductivity (Soil_EC1–EC3), soil temperature (Soil_T1–T3)
  - Wind sensors near and above the canopy (WS_Cup1–WS_Cup3)
- Sampling cadence: data recorded every 20 seconds and averaged to 15-minute intervals.
- Data format and units: provided in SI-compatible units with descriptive field entries (e.g., height, instrument, description).

## Quality control and metadata
- Quality control: visual checks; removal of obvious instrument faults, datalogger issues, and power outages; occasional gaps due to sensor replacements.
- Notes on data quirks: step changes in leaf wetness measurements due to sensor baseline differences after replacements.
- Metadata transparency: dataset includes extensive field descriptions (instrument, height, description) to aid interpretation and reuse.

## Data structure and content
- Records: 70,176 measurements across 37 parameters.
- File format: CSV with columns including Timestamp, Height (m), Instrument, Description, and parameter-specific fields (e.g., Rain, Throughfall, LWS1–LWS4, AirT1–AirT4, RH1–RH4, Soil_VWC1–VWC3, etc.).
- Key parameter groups:
  - Rain and throughfall
  - Leaf wetness sensors (LWS1–LWS4)
  - Air temperature and relative humidity at multiple heights (AirT1–AirT4, RH1–RH4)
  - Soil moisture, conductivity, and temperature at multiple depths (Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3)
  - Wind and barometric pressure (WS_Cup1–WS_Cup3, WXT_WS1/WS2, WXT_WD1/WD2, WXT_BP1/BP2)
  - Radiation measures (PAR1–PAR2, Total_Solar1–Total_Solar2)
- Coverage: comprehensive multi-height dataset designed to support vertical profiling and deposition analyses.

## Experimental context
- Site purpose: ammonia enhancement experiments with wind-controlled conditions to study NH3 emissions and deposition in forest ecosystems.
- Relationship to prior work: extension of the 2022 dataset from the same site.
- Related publications and data access:
  - Deshpande et al. (2024a) Deciphering estimation of ammonia deposition via wind-controlled enhancement
  - Deshpande et al. (2024b) Meteorological data and ammonia concentration/deposition rates from Queensberry site (2022 dataset)
  - Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1)
  - Data availability: NERC EDS Environmental Information Data Centre (DOI references provided in the related publications)

## Accessibility and provenance
- Data are accompanied by methodological context describing experimental design, analysis, and findings in the cited works.
- Data provenance: collected with standardized instruments (e.g., Vaisala, Campbell Scientific, METER Environment), logged with consistent time stamps, and validated through quality checks.
- Intended use: suitable for calibration and validation of atmospheric deposition models, assessment of NH3 enhancement impacts, and informing monitoring frameworks and policy decisions related to environmental health.

## Relevance for monitoring frameworks
- Demonstrates rigorous data governance: high-frequency, multi-parameter measurements with clear QC and metadata practices.
- Supports environmental health monitoring goals: provides near-real-time-like data for understanding deposition processes, canopy interactions, and vertical profiles relevant to policy evaluation.
- Highlights practical challenges for monitoring: data gaps, sensor replacements causing baseline shifts, and the need for robust metadata to ensure traceability and reuse.
- Illustrates the importance of data standardization and open data practices for informing future monitoring approaches and governance.