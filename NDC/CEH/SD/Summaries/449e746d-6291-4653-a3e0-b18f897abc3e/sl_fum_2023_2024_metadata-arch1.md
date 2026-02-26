# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (20232024)

## Overview
- Purpose: study the effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil in a tropical sub-montane forest.
- Location: Queensberry Estate, central Sri Lanka (coordinates 6.9693°, 80.5911°; altitude 1645 m).
- Timeframe: data from 1 January 2023 to 31 December 2024; extension of a 2022 dataset.
- Context: part of a broader effort to estimate ammonia deposition to forest ecosystems; results linked to Deshpande et al. (2024a, 2024b).

## Experimental design and NH3 release control
- Release system: NH3 is emitted only when wind conditions meet specific directional and speed thresholds, measured below the canopy.
  - Wind direction: 5–75° and 185–255°.
  - Wind speed threshold: 0.3–10 m s⁻¹.
- Physical setup: three horizontally aligned 20 m PVC tubes at heights of 0.5, 1.35, and 2.2 m.
  - NH3 delivery through six 4 mm holes around each tube (20 cm spacing).
  - Gas supplied from a cylinder via a manifold, mass flow controller (MFC), and solenoid valve; NH3 is diluted in the fan airflow prior to release.
  - Solenoid valve enabling release only under correct wind conditions.
- Monitoring and data capture:
  - Below-canopy wind data from a WXT536 weather station.
  - NH3 release rate recorded by the MFC every 20 seconds; 15-minute interval averages computed.
- Time reference: all data are logged in Sri Lanka Standard Time (SLST).

## Data content and structure
- Dataset size: 61,751 measurements across 4 parameters.
- Format: CSV with the following columns (described succinctly):
  - Timestamp fields (three components: date, time, description)
  - NH3_status: duration (minutes) NH3 was released; valve type (Type 6027 solenoid valve); manufacturer (Bürkert); description (time NH3 release)
  - NH3_flow: flow rate (slpm); instrument (G series MFC); manufacturer (MKS Instruments); description (NH3 flow into release manifold)
  - Wind_speed: wind speed (ms⁻¹); instrument (WXT536); manufacturer (Vaisala); description (below-canopy wind speed)
  - Wind_direction: wind direction (degrees); instrument (WXT536); manufacturer (Vaisala); description (below-canopy wind direction)

## Data quality control
- Visual checks performed; obvious instrument malfunctions, datalogger issues, and power cuts removed.
- Some data gaps caused by replacement of faulty gas control components.

## Temporal and contextual scope
- Timeframe covered: 1 January 2023 to 31 December 2024.
- Relationship to prior work: extension of the 2022 dataset from the same site; contributes to broader analyses of NH3 enhancement and deposition.

## Data usage and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Key references:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos. Environ. 2024a. DOI: 10.1016/j.atmosenv.2023.120325
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Queensberry, Sri Lanka, 2022. NERC EDS Environmental Information Data Centre. DOI: 10.5285/998c2b2b-7470-42b0-81e7-409b91752377

## Accessibility and metadata
- Data are provided as CSV with explicit units, instrument details, and descriptions for each variable.
- Complete methodological details are available in the cited Deshpande et al. papers, including experimental design, analysis, and findings.