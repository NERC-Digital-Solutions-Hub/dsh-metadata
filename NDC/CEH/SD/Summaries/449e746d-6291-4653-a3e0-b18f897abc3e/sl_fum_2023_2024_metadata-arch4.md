# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Overview
- Study to understand the effects of high ambient ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate, central Sri Lanka; tropical sub-montane forest.
- Timeframe: 1 January 2023 – 31 December 2024 (Sri Lanka Standard Time).
- Data is part of an NH3 enhancement experiment with wind-controlled release.

## Data collection and methodology
- NH3 release is triggered only when below-canopy wind conditions meet specific direction and speed thresholds (5-75° and 185-255°; 0.3–10 m/s).
- Release system: three 20 m PVC tubes (110 mm OD) at heights 0.5, 1.35, and 2.2 m with six 4 mm holes per tube.
- NH3 delivery: stainless steel pipe, mass flow controller (MFC), solenoid valve; gas injected into the fan airflow and diluted before release.
- Monitoring and control: WXT536 weather station for wind data; MFC records NH3 volume released every 20 seconds; 15-minute averages calculated.
- Data timezone: SLST (Sri Lanka Standard Time).
- Dataset is an extension of the 2022 site dataset.

## Data structure and contents
- Total measurements: 61,751 across 4 parameters.
- Data format: CSV with columns including:
  - Timestamp (and related instrument/manufacturer details)
  - NH3_status (Minutes; duration NH3 is released)
  - NH3_flow (slpm; NH3 flow through the MFC into the release manifold)
  - Wind_speed (ms^-1; below-canopy wind speed)
  - Wind_direction (degrees; below-canopy wind direction)
- Additional metadata fields describe timestamp provenance, instrument, and description for each variable.

## Quality control and data quality notes
- Visual quality checks performed; removal of obvious instrument malfunctions, datalogger issues, and power-cut artifacts.
- Gaps present due to replacement of faulty gas control components.

## Temporal coverage and granularity
- Coverage: 2023-01-01 to 2024-12-31.
- Temporal resolution: data recorded every 20 seconds; 15-minute interval averages provided for certain fields.

## Data governance, accessibility, and metadata
- Detailed methodological description and equipment specifications documented.
- Data provided as a CSV with comprehensive column-level metadata and instrument details.
- Related publications and data products referenced (Deshpande et al. 2024a, 2024b) and deposited at NERC EDS Environmental Information Data Centre.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Key references:
  - Deshpande et al. (2024a) Estimation of ammonia deposition to forest ecosystems using wind-controlled NH3 enhancement experiments, Atmos. Environ.
  - Deshpande et al. (2024b) Meteorological data and ammonia concentration and deposition rates from Queensberry, Sri Lanka, NERC EDS Environmental Information Data Centre.