# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

## Overview
- Dataset supporting Grid-to-Grid (G2G) model estimates of monthly mean flow and soil moisture for Great Britain over 1891–2015.
- Part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), a UK NERC-funded research program.
- Provides 1 km x 1 km gridded monthly means of natural river flow (m3 s-1) and soil moisture (mm water/m soil), driven by observed meteorological data.

## Model and outputs
- Hydrological model: Grid-to-Grid (G2G), operated on a 1 km x 1 km grid with a 15-minute time-step, parameterised from digital datasets and accounting for urban/suburban land-cover effects.
- Outputs: monthly means of daily natural flow and monthly mean soil moisture (flow in m3 s-1; soil moisture in mm water/m soil).
- Model characteristics: calibrated to GB conditions, performs well for catchments with natural flow regimes; less accurate where artificial abstractions/discharges are significant or sub-surface hydrology is complex.

## Meteorological driving data
- Daily rainfall: 1 km x 1 km CEH-GEAR dataset (Keller et al. 2015; Tanguy et al. 2016).
- Potential evapotranspiration (PE): monthly estimates derived from temperature data on a 5 km x 5 km grid (Oudin et al. 2005), with long-term correction factors to align with MORECS values (Rudd et al. 2007).
- Early 20th century rainfall gaps are spatially infilled (Rudd et al. 2017); PE is temperature-based for 1891–2015.

## Data format and files
- Primary data file: MaRIUS-G2G-Oudin-monthly 1 km x 1 km gridded data stored in NetCDF4 (CEH conventions).
- File naming: G2G_Oudin_var_1891_2015.nc (variables: flow or soil).
- Spatial domain: 700 km × 1000 km GB national grid; grid boxes represent the centre of each 1 km cell.
- Temporal reference: days since 1891-01-01; monthly values assigned to the first day of each month.
- Variables: flow, soil, time; missing values set to -9999 for sea grid cells.
- Additional datasets to support interpretation:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) draining to each 1 km grid box.
  - MaRIUS_G2G_NRFAStationIDGrid.nc: locations of NRFA gauging stations on the 1 km grid (1285 stations).
  - MaRIUS_NRFAStationIDs.csv: NRFA station IDs for which corresponding G2G grid boxes exist.

## How to use the data
- Compare G2G natural flow estimates to observed NRFA flows (e.g., NRFA data portal) to assess model performance.
- G2G performance: robust for catchments with natural flow regimes and accurate gauged records; limitations in areas with significant abstractions or discharges or complex subsurface hydrology.
- Validation considerations: ensure correct NRFA catchment representation for each G2G grid cell; small catchments may exhibit discretisation-related mismatches between observed catchments and grid-based representations.
- Example outputs and visualizations are illustrated in accompanying figures (e.g., example grids and NRFA station locations).

## Data provenance and limitations
- Driving data are observation-based; PE is derived from temperature data with regional correction factors.
- Snow module is not used; precipitation is distributed uniformly to model time-steps.
- Early-period data gaps are addressed through infilling; users should consider potential uncertainties in early 20th-century inputs.

## Metadata, governance, and access
- Data provided in standardized NetCDF4 format with clear variable naming (flow, soil, time) and calendar alignment.
- Supplementary grids (catchment areas and NRFA stations) facilitate interpretation and validation against observed data.
- Acknowledges funders and contributors; references provide methodological context for model components and driving datasets.

## Acknowledgements and references
- Funded by the UK Natural Environment Research Council as part of the MaRIUS project; thanks to individuals for advice and assistance.
- Key references cover G2G model development, data sources (CEH-GEAR, MORECS), and drought/hydrology analyses relevant to the dataset.