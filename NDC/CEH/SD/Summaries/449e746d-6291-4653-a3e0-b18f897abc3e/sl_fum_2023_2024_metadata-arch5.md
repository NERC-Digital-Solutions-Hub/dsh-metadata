# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Overview
- Study aim: investigate effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate, central Sri Lanka (6.9693°, 80.5911°, altitude 1645 m).
- Timeframe: data collected 1 January 2023 – 31 December 2024; extension of the 2022 dataset from the same site.
- Data format: CSV dataset with 61,751 measurements across four parameters.

## Data Collection and Experimental Setup
- Release system: NH3 released from three 20 m long tubes (110 mm OD) aligned parallel, at heights of 0.5, 1.35, and 2.2 m.
- NH3 release mechanism: NH3 fed from a cylinder through a mass flow controller (MFC) and solenoid valve into a central manifold and mixed with airflow from a central fan.
- Control logic: NH3 released only when wind direction matches monitoring quadrats (5–75° and 185–255°) and wind speeds exceed thresholds (0.3–10 m/s).
- Monitoring and measurement: below-canopy wind data from a WXT536 weather station; NH3 volume measured by the MFC and logged every 20 seconds, with 15-minute interval averages.
- Time standard: all measurements in Sri Lanka Standard Time (SLST).

## Data Quality and Processing
- Quality control: visual checks performed; obvious instrument malfunctions, datalogger issues, and power cuts corrected or removed.
- Gaps: some data gaps attributed to replacement of faulty gas control components.

## Data Structure and Metadata
- Dataset size: 61,751 measurements, 4 primary parameters.
- Data format and columns: CSV with 15-minute timestamps and the following parameters:
  - NH3_status: time NH3 is released; 15-minute intervals; units in minutes; instrument: Type 6027 solenoid valve; manufacturer: Bürkert.
  - NH3_flow: NH3 flow through the MFC into the release manifold; units: slpm; instrument: G series MFC; manufacturer: MKS Instruments.
  - Wind_speed: below-canopy wind speed; units: ms^-1; instrument: WXT536; manufacturer: Vaisala.
  - Wind_direction: below-canopy wind direction; units: degrees; instrument: WXT536; manufacturer: Vaisala.
- Time and metadata: each field includes timestamp metadata (unit, instrument, manufacturer, description); timestamps are 15-minute intervals.
- Coverage: data span 2023-01-01 to 2024-12-31 in SLST.

## Data Governance, Provenance, and Access
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Provenance: extension of the 2022 Queensberry site dataset; linked to related publications and data centre records.
- Reuse and discovery: metadata and structure prepared to support uploading to data portals/catalogues and to meet data governance and data user needs as per dataset stewardship standards. References provided for methodology and data sources:
  - Deshpande et al. 2024a (full experimental design, methodology, analysis, and findings).
  - Deshpande et al. 2024b (meteorological data and ammonia concentration/deposition rates, 2022 dataset).
  - NERC EDS Environmental Information Data Centre entry (2024b).