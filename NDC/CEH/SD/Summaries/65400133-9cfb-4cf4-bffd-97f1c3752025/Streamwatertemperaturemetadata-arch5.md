# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

## Overview
- Integrates observed river water temperatures with a consistent set of modeled climate data to explore how climate controls seasonal WT across Britain.
- Aims to understand large-scale spatio-temporal variability and basin modifiers to inform water and land management under climate change.

## Dataset scope and coverage
- 35 water temperature monitoring sites on 21 rivers across 16 basins.
- Great Britain geographic extent.
- Temporal coverage: 1984–2007.
- Seasonal data: three-month averages (winter, spring, summer, autumn) for six climate variables.

## Data components and variables
- Water temperature data (WT): 3-month average WT (°C) derived from various CEH projects; temporal resolution varies by source.
- Climate data: six variables from CHESS forcing dataset for JULES (daily time series, 1971–2007, 1-km grid).
  - Includes: air temperature (AT), short wave radiation (SWR), wind speed (WS), specific humidity (SH), precipitation (P), long wave radiation (LWR).
- Time index: a code representing seasons and years (e.g., 1 = winter 1984, 1.25 = spring 1984, etc.).
- Spatial matching: CHESS 1-km cells matched to the study sites.

## Dataset columns (data structure)
- UID: Unique identifier
- Year: Year of data collection
- Season: Season of data collection (1 = winter; 2 = spring; 3 = summer; 4 = autumn)
- Num Days: Number of days used to calculate 3-month averages
- WT: 3-month average Water Temperature (°C)
- AT: 3-month average Air Temperature (°C)
- SWR: 3-month average Short Wave Radiation (W/m^2)
- WS: 3-month average Wind Speed (m/s)
- SH: 3-month average Specific Humidity (kg/kg)
- P: 3-month average Precipitation (kg/m^2/day; unit equivalent)
- LWR: 3-month average Long Wave Radiation (W/m^2)
- Time: Time index for modelling
- Dataset: Dataset name
- Basin: Basin name
- River: River name
- Site: Site name or code
- NGR: National Grid Reference
- Easting: British National Grid easting
- Northing: British National Grid northing

## Climate data and modelling context
- CHESS dataset serves as the forcing data for JULES (UK land surface model).
- CHESS: UK-wide 1-km downscaling from MORECS (precipitation based on gauge data); provides daily series per 1-km cell for 1971–2007.
- Spatial matching ensures each study site aligns with the CHESS cell data.

## Seasonal series derivation and processing
- Step 1: Sub-daily WT datasets were averaged to daily values where possible; spot measurements assumed representative of the measurement day for some datasets.
- Step 2: Daily WT data were matched by date to corresponding daily climate data.
- Step 3: Seasonal averages were computed from daily data using standard definitions:
  - Winter: December–February (spanning year boundaries; e.g., winter 1976 uses Dec 1975, Jan 1976, Feb 1976)
  - Spring: March–May
  - Summer: June–August
  - Autumn: September–November
- Season codes: 1 (winter), 2 (spring), 3 (summer), 4 (autumn).

## Data provenance and references
- Water temperature data sourced from CEH and related UK projects (e.g., Frome, Great Ouse, Tadnoll, Plynlimon, UKAWMN, LOCAR).
- Climate data derived from CHESS (JULES forcing) with supporting methodological references for model components and data sources.

## Practical considerations for Data Stewards
- Data governance and standards:
  - Ensure consistent metadata across WT and climate variables; document data origins, processing steps, and seasonal derivation rules.
  - Maintain traceability of source projects and transformations (daily -> seasonal averages).
- Data interoperability and formats:
  - Align column definitions and units (e.g., WT in °C, radiation in W/m^2, P units) to facilitate cross-dataset integration.
  - Preserve time indexing scheme (Season, Time) for reproducibility and modelling needs.
- Data quality and updates:
  - Be aware of varying temporal resolutions and gaps due to source heterogeneity; document data availability and limitations.
  - Establish workflows for updating with new data or reprocessing as climate datasets are refined.
- Data sharing and access:
  - Provide clear provenance, licensing, and usage guidance; note that some WT sources were not originally collected for warming/climate studies and may have bespoke collection methods.
- Governance challenges to pre-empt:
  - Bridging incomplete user needs with a technically rich, multi-source dataset.
  - Coordinating data from multiple systems and formats; ensuring interoperability.
  - Handling large datasets and potentially non-uniform historical data requiring bespoke processing.

## Usage notes
- Suitable for analyses linking seasonal WT with modeled climate drivers, assessing basin-specific responses, and informing climate adaptation strategies for river management.
- Users should account for the heterogeneity in WT data resolution and potential temporal gaps when conducting comparative analyses or trend assessments.