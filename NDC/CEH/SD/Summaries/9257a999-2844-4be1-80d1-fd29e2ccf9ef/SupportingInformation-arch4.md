# Exotic Plantations Increase Risk of Flooding in Mountainous Landscapes

## Overview and purpose
- Describes two datasets used to support the manuscript on how land cover affects flood risk in the Upper Nilgiris (Western Ghats, Tamil Nadu, India).
- Datasets cover 2013–2016 field campaigns with ongoing data collection up to May 2020.
- Data were collected by a collaboration of four research agencies and are tied to ecohydrology research on rain–runoff, carbon sequestration, and nutrient/sediment discharge.
- Focus is on extreme rain events; the dry season data are not included.

## Data assets (two CSV files)
- DailyRainDischarge2014to2016.csv
  - Daily rainfall and discharge for eight small catchments with land-cover information in the Upper Nilgiris.
  - Rainfall recorded with tipping bucket rain gauges (1-minute resolution, tips per minute converted to mm).
  - Water level data recorded with capacitance-based loggers in stilling wells.
  - Data aggregated to daily time steps for analysis; used to study rain–runoff response.
- KSatLandCovers.csv
  - Saturated hydraulic conductivity (Ksat) under major land covers.
  - Measured in the field with a mini-disk infiltrometer at selected sites.
  - Land covers include Shola, Grassland, Pine, and Wattle.

## Fieldwork, instrumentation, and data collection
- Rainfall (Rain gauges)
  - Tipping bucket gauges installed in grasslands and ridges on a ~1x1 km grid; data captured at 1-minute intervals; retrieved roughly every two weeks.
  - Precise locations provided (coordinates listed in the document).
- Discharge (water level recorders)
  - Eleven streams monitored at 5-minute intervals; stage values converted to discharge using velocity–area methods (except one unit with a weir).
  - Catchments are small (order 1–3); boundaries estimated from SRTM data.
- Infiltration (Ksat)
  - Mini-disk infiltrometers used at patch-scale land covers; GPS accuracy ~20 m due to canopy; multiple site coordinates provided for Shola, Grassland, Pine, and Wattle.

## Data processing, structure, and reproducibility
- Data handling
  - Raw data imported into R and aggregated to daily time steps.
  - Comprehensive processing pipeline documented via a suite of scripts and functions (organized with master scripts and modular components).
  - Scripts cover data import, calibration, gap filling, aggregation to multiple timescales, and reporting outputs (CSV and plots).
- Data structure and metadata
  - Data described in detail (Table 5) with fields such as:
    - dt.tm: Timestamp (IST) of the sample
    - wlr: Water level recorder number
    - Discharge, DepthDischarge: discharge metrics; flowD: daily flow; mm: daily rainfall
    - PeakDischarge, PeakDepthDischarge: daily peak metrics
    - AMI: Antecedent Moisture Index (past 14 days)
    - area, CircularityIndex, slopeSteep, drainDensity: catchment characteristics
    - catchment: land-cover category (Wattle, Grassland, Shola)
  - Calibration and QA metadata are embedded in the data lineage (calibration for rain gauge and WLRs; QA notes linked to data fields).

## Quality assurance and data quality
- General QA
  - Regular checks for power interruptions, battery changes, and contact issues; problematic intervals replaced with NULL values.
  - Stilling wells paired with a permanent scale to correct placement errors in capacitance probes.
  - Salt-dilution gauging (slug and constant-rate) used in parallel with velocity-area methods for discharge validation.
  - Infiltrometer readings: at least three consecutive readings per sample; discard readings with air-leak issues.
  - Sampling sites chosen to avoid obstructions (stones, sticks) and ensure representative measurements.
- Rain/runoff data QA
  - Rainfall converted from tips-per-minute to mm during annual calibration.
  - WLR readings converted to mm using manufacturer software.
- Documentation
  - Calibration procedures and QA steps are documented (e.g., rainfall gauge calibration, WLR calibration, infiltrometer protocol).

## Limitations and considerations for data users
- Dry-season data are not included; dataset emphasizes extreme rainfall events.
- GPS accuracy for some land-cover sites is ~20 m due to canopy cover.
- Data describe specific catchments in a particular region; applicability to other regions should consider local context.
- Meta-information and processing scripts enable reproducibility, but users should review calibration notes and data processing steps when reusing the data.

## Context and references
- The data support analyses related to land-cover effects on rainfall–runoff processes, carbon sequestration, and nutrient/sediment discharge.
- Equipment manuals and foundational references (e.g., Rain Wise gauges, mini-disk infiltrometers, velocity–area discharge methods) are cited to underpin methodologies.