# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Overview
- National Park site in Northern Ireland (ASSI/SAC and Ramsar) monitored for potential NH3 impacts on the ammonia-sensitive Ballynahone Bog.
- Managed by Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Data collected along a transect through the bog due to concerns about NH3 emissions from local poultry installations.
- Monthly sampling with replicates to improve reliability; data intended for evaluating air-borne ammonia exposure and informing policy decisions.

## Measurement design and sampling
- UKCEH ALPHA passive samplers deployed around the transect at about 1.5 m above ground.
- Replicate samplers used per site to estimate ambient NH3 concentrations more robustly.
- Exposure cycles: monthly, at the beginning of each month.
- Data processing converts sampler readings to average ambient NH3 concentration using a known uptake rate (0.0038422 m3 h-1) and exposure duration.

## Laboratory analysis and concentration calculation
- Ammonia captured on citric acid-coated filters; analysis via SEAL AA3 colorimetric method after extraction in deionised water.
- Results reported as micrograms NH3 per cubic metre of air (µg NH3 m-3).
- Some raw samples were invalid due to incorrect exposure or weather-related losses; flagged accordingly.

## Data quality assurance and flags
- Data quality assessed with explicit rules:
  - Coefficient of variation (CV) across replicates < 15% → considered valid; otherwise evaluative steps taken.
  - Missing samplers flagged as invalid (-9999.00).
  - Sampler duration anomalies (long/short) flagged.
  - Local contamination or deviations noted; non-representative samples discarded.
- Final dataset (UWT_Ballynahone_Bog_Data_2022.csv) contains accepted data with appropriate flags.
- Data quality and provenance are documented, with data flagged for review and notes on storage/sharing constraints.
- Data capture percentage and validation status included per record; verification status codes (1=Verified, 2=Preliminary verified, 3=Not verified) available.

## Data structure and contents
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv.
- Each row represents one month of data for a single site.
- Columns include:
  - Site name, unique site identifier, network_id (BE)
  - Parameter type (alpha_NH3_g), measurement start/end dates and times
  - Ammonia concentration (µg NH3 m-3)
  - Flags for detection limit (less than), verification, unit, data capture, validity
  - EMEP data status codes and accompanying flags
  - Month of measurement
- The dataset documents site-specific data and has a separate page listing site information and identifiers.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8
- Start date: 01/09/2014; End date: Ongoing
- Location coordinates and altitude:
  - All sites at approximately 1.5 m above ground intake height
  - Latitudes and longitudes vary per site (e.g., bog_1: 54.82223827, -6.67860685; bog_8: 54.816161, -6.655967)
- Spatial identifiers and site details provided to support data integration and mapping

## Data governance, accessibility, and limitations
- Data are collected for environmental health monitoring and policy evaluation; metadata and dataset documentation accompany the data.
- Data may require sharing and proper governance; some raw data were excluded or flagged due to quality concerns.
- Potential barriers include data availability, metadata completeness, and ensuring up-to-date information across all sites.
- The dataset emphasizes transparency in QA processes, replicates usage, and explicit data flags to enable reproducibility and proper interpretation.

## Relevance for monitoring frameworks
- Demonstrates a practical, QA-driven approach to long-term environmental monitoring for policy relevance.
- Highlights importance of replicates, clear data processing steps, and explicit metadata to support data reuse.
- Shows integration of site-level measurements with standardized flags and data status codes, aiding cross-site comparisons and governance.
- Provides a model for documenting data quality issues, data capture, and provenance to inform future monitoring frameworks and decision-making.