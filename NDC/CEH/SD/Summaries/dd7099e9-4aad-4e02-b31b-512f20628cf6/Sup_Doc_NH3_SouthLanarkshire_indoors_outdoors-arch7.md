# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two sites in a rural area of South Lanarkshire: one indoors (hall of dwelling) and one outdoors (garden) adjacent to grassland on a dairy farm.
- Collected using CEH ALPHA® passive samplers to measure ammonia (NH3) concentrations in air.
- Analysis performed by CEH Edinburgh; data embedded in a final CSV dataset (NH3_SouthLanarkshire_indoors_outdoors.csv) with monthly measurements.

## Study Area and Sites
- Inside site: located in the hall of a dwelling; coordinates 55.64072, 3.59705; air inlet height 1.5 m.
- Outside site: located in the garden of the dwelling; same coordinates; air inlet height 1.5 m.
- Operated by dwelling owner; analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.

## Measurement Methodology
- Passive CEH ALPHA® samplers with citric acid coated filter and PTFE membrane; diffuser orientation downward during exposure.
- Replicate samplers used for each site to improve reliability.
- Samplers exposed monthly at the beginning of each month, mounted on a shelter at ~1.5 m height.
- Analysis: samplers digested in deionised water; NH3 quantified by SEAL AA3 colorimetric method.
- NH3 concentration in air calculated from ammonium concentration using a known uptake rate of 0.003241315 m3 hr-1 and exposure duration.
- Data quality flags applied for concerns; final data values expressed as µg NH3 m-3.

## Data Product and Structure
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors.csv.
- Each row represents one month of data for a single site.
- Key fields (examples):
  - Site name and unique site identifier
  - network_id (RSW)
  - parameter_id (alpha_NH3_g)
  - measurement start date/time and measurement end date/time (exposure period)
  - concentration (units: µg NH3 m-3)
  - less-than flag (detection limit indicator)
  - verification id (1=Verified, 2= Preliminary verified, 3= Not verified)
  - unit_id (24 = µg NH3 m-3)
  - data capture (%) and validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status flags) and related explanatory codes
  - Month-Year of measurement (mmm-yy)
- Dataset also details site-specific information (two sites: inside and outside) and page-level notes about data content and flag meanings.

## Data Quality and Flags
- Quality checks:
  - CV of replicates: must be <15% for reliable replication; if >15%, replicates may be discarded or retained with notes.
  - Some measurements exceed calibration range but are still considered valid.
  - Missing data indicated by -9999 (and/or missing date/time metadata).
- EMEP flags provide context for each data point, including:
  - Data capture status (e.g., 0, 1)
  - Validity (e.g., -1, 1)
  - Reasoning codes (e.g., contamination, detection limits, sampling period issues, proximity influences)
- Examples of common flags described include CV issues (103), below detection (781/780), representative sampling period adjustments (652/653), contamination or local influence (559/599/651), and other site/measurement conditions.

## Spatial and Temporal Details
- Temporal coverage begins 01/01/2017; ongoing (End date: Ongoing).
- Spatial coordinates for both sites: Latitude 55.64072, Longitude 3.59705.
- Inlet height for both sites: 1.5 m above ground.
- Two discrete sites: indoor (hall) and outdoor (garden) at the same dwelling location.

## GIS Use and Considerations
- Data designed for map-based presentation and spatial analysis of indoor vs. outdoor NH3 concentrations.
- Useful for joining with spatial features representing the dwelling, garden, and surrounding land use (grassland / dairy farm) to assess spatial patterns and potential local influences.
- Time-series dimension (monthly) enables visualization of temporal trends across the two site types.
- Data quality flags and EMEP codes should be consulted when filtering for GIS analyses or when creating confidence-annotated maps.