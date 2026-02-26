# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly] Bell VA, Rudd AC, Kay AL and Davies HN (2018). NERC Environmental Information Data Centre. https://catalogue.ceh.ac.uk/documents/e911196a-b37147b1-968c-661eb600d83b

## Purpose and scope
- Provides data and context for Grid-to-Grid (G2G) model estimates of monthly mean flow and soil moisture across Great Britain (GB) for 1960–2015.
- Supports assessment of drought and water scarcity risks by enabling comparison between modelled natural flows/soil moisture and observed gauged data.

## What the dataset contains
- Grid-to-Grid model outputs on a 1 km x 1 km grid:
  - Flow (m3 s-1) – monthly means of daily 09:00 values.
  - Soil moisture (mm water per m of soil) – monthly means of daily 09:00 values.
- Two supporting spatial datasets:
  - Digitally-derived catchment areas on a 1 km x 1 km grid.
  - Estimated locations of flow gauging stations on the 1 km x 1 km grid (and as a CSV).
- Historical driving meteorological data:
  - 1 km x 1 km daily rainfall (CEH-GEAR).
  - Monthly potential evaporation (PE) on a 40 km grid (MORECS).

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G), GB-wide, 1 km grid, 15-minute time-step, parameterised from physical datasets (soil types, land-cover, etc.).
- Key modelling characteristics:
  - Focus on natural (unabated) flows; does not incorporate abstractions or discharges.
  - Snow module not used; precipitation treated as rain.
  - Spatial data-driven parameters rather than catchment-specific calibration.
- Drive data specifics:
  - Rainfall: 1 km x 1 km CEH-GEAR estimates.
  - PE: 40 km MORECS estimates distributed to 1 km grid cells.
  - Inputs aligned with GB national grid; topography/soil data as per Bell et al. (2009).

## How to use the data
- Compare G2G natural-flow outputs with observed river flows from the National River Flow Archive (NRFA) to evaluate model performance.
- Performance notes:
  - Better for catchments with natural flow regimes and accurate observed flows.
  - Less reliable in areas with significant artificial water use or complex subsurface hydrology.
- Gauging station mapping:
  - A dedicated 1 km grid links NRFA stations to corresponding G2G grid cells to facilitate validation against observed data.
  - Includes checks to ensure correct tributary representation; small catchments may still show discrepancies due to grid discretisation.

## Data format and structure
- Primary dataset: MaRIUS-G2G-MORECS-monthly.nc (NetCDF4), with:
  - Variables: flow and soil (monthly means of daily 09:00 values).
  - Time: 1960–2015; calendar aligned to Gregorian years (first day of month for monthly values).
  - Domain: 700 km x 1000 km GB land area; sea grid cells set to missing (-9999).
- Supporting datasets:
  - MaRIUS_G2G_CatchmentAreaGrid.nc — catchment area (km2) per 1 km grid cell.
  - MaRIUS_G2G_NRFAStationIDGrid.nc — NRFA station IDs mapped to 1 km grid cells (land=ID, sea=-9999).
  - MaRIUS_NRFAStationIDs.csv — NRFA station details and mappings.
- Documentation cues:
  - File naming: G2G_MORECS_var_1960_2015.nc; var is 'flow' or 'soil'.
  - Time encoding: days since 1900-01-01; values nominally assigned to the first day of each month.

## Data quality, limitations, and considerations
- Natural-flow emphasis means outputs best reflect unimpeded hydrology; artificial withdrawals or discharges reduce reliability.
- Catchment-area discretisation to 1 km can cause small-catchment misalignments between G2G and NRFA catchments.
- Soil properties assume spatially varying depth; depth-integrated soil-moisture values represent the entire soil column.
- Snow effects and snowmelt processes are not represented in this dataset.
- Metadata and linking to observed stations are provided to support verification, but users should assess applicability to their monitoring questions.

## Data governance and provenance
- Funded by the UK Natural Environment Research Council (MaRIUS project) as part of drought and water scarcity research.
- Data publicly described and accompanied by scientific references validating model performance (Bell et al. 2009, 2016; Rudd et al. 2017; Davies & Bell 2009; Keller et al. 2015; Tanguy et al. 2016).

## References and further reading
- Bell VA, Kay AL, Jones RG et al. (2009). Use of soil data in a grid-based hydrological model to estimate spatial variation in changing flood risk across the UK.
- Bell VA, Kay AL, Davies HN, Jones RG (2016). Assessment of impacts of climate change on snow and peak river flows across Britain.
- Davies HN, Bell VA (2009). Methods for extracting low-resolution river networks from high-resolution data.
- Hough M, Jones RJA (1997). MORECS methodology overview.
- Keller VDJ, Tanguy M et al. (2015). CEH-GEAR rainfall estimates.
- Monteith JL (1965). Evaporation and environment.
- Rudd AC, Bell VA, Kay AL (2017). National-scale analysis of simulated hydrological droughts.
- Tanguy M, Dixon H et al. (2016). Gridded estimates of UK rainfall (CEH-GEAR).