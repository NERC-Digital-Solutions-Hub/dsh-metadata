# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

## Overview
- Provides grid-to-grid (G2G) model estimates of daily mean river flow for gauged catchments across Great Britain for 1960–2015.
- Enables comparison between simulated natural flows and observed gauged flows at 260 NRFA stations.
- Produced under the MaRIUS project (2014–2017) and stored in the NERC Environmental Information Data Centre.

## Dataset contents
- Variable: River flow (m3 s-1), daily mean from 09:00 to 09:00 the following day.
- Geographic scope: 260 NRFA gauging stations across Britain.
- Primary data file: G2G_MORECS_flow_1960_2015.csv
  - Structure: first column = date; subsequent columns = daily mean flows for each catchment.
  - Time coverage: 1960–2015 (calendar follows 365/366 days).
- Supporting station mapping: MaRIUS_NRFAStationInfo.csv
  - Details for each NRFA station, including station ID, river name, location, G2G easting/northing, catchment area, and data issues.
- Driving data used by G2G:
  - Precipitation: 1 km x 1 km CEH-GEAR daily rainfall.
  - Evaporation: Monthly potential evaporation (PE) from MORECS on a 40 km grid.
- Documentation: Brief summary and usage notes accompany the data, with references to related methodological studies.

## Model inputs and configuration
- Hydrological model: Grid-to-Grid (G2G), 1 km x 1 km grid, 15-minute time-step, parameterised by global spatial datasets (soil, land-cover, topography).
- Meteorological drivers: observed-based rainfall and PE (as above).
- Snow module: Not used in this dataset; precipitation treated as rain.
- Spin-up: Not included in these files.
- Calibration: Generally avoids catchment-by-catchment calibration; uses nationally applicable spatial parameter values.

## Data format and access
- Format: CSV with a single header row.
- Time representation: calendar date; flows are daily mean values (09:00 to 09:00).
- File naming: G2G_MORECS_flow_1960_2015.csv (historical).
- Data centre: NERC Environmental Information Data Centre (EIDC).
- Access and provenance: Dataset is an outcome of the MaRIUS project; acknowledgements and references provided for reproducibility and attribution.

## Spatial mapping and catchment considerations
- Each NRFA gauging station is paired with the most appropriate G2G 1 km grid cell, chosen for geographic proximity and catchment area similarity.
- Validation checks confirm the G2G river flow corresponds to the correct river tributary.
- Catchment area differences: In some cases, the G2G-derived catchment area draining to the selected 1 km cell differs from the NRFA catchment area; overall, G2G catchment areas are within 8% of NRFA catchment areas.
- Suitability: G2G performs best for catchments with natural flow regimes and accurate observed flow records; performance declines in regions with substantial artificial abstractions or discharges and where sub-surface hydrology is complex.

## How to use and interpret
- Use case: Compare simulated natural flows (1960–2015) with observed gauged flows from NRFA to assess model performance and drought identification capabilities.
- Key considerations:
  - The most appropriate G2G grid cell should be used for each NRFA station, with additional checks to ensure correct tributary representation.
  - Interpret results with caution in small catchments where grid discretisation can introduce larger relative errors.
  - Recognize that the model excludes explicit human alterations (abstractions, discharges) which can influence observed flows.

## Provenance, acknowledgements, and references
- Project provenance: MaRIUS (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity), UK NERC-funded (NE/L010208/1).
- Acknowledgements: Thanks to individuals who assisted in data curation and dissemination.
- References: Foundational methodological papers on the G2G model, CEH-GEAR rainfall estimates, MORECS evaporation data, and related drought analyses (multiple cited works from Bell, Kay, Jones, Hough, Tanguy, Monteith, etc.).

## Data stewardship considerations
- Metadata: Includes variable definitions, unit conventions, time references, and station mappings to facilitate discovery, reuse, and quality assessment.
- Data lifecycle: Historical dataset (1960–2015) intended for use in model validation and impact analyses; no automated updates indicated.
- Usage notes: Clear caveats about non-interoperability with certain anthropogenic datasets and potential catchment-area discrepancies; ensure proper attribution to MaRIUS and related data sources in any derived analyses.