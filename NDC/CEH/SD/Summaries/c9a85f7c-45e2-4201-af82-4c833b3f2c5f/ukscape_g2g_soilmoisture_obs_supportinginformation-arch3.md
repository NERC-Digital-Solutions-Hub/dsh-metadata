# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE programme (NERC-funded) provides Grid-to-Grid (G2G) soil moisture estimates for GB and NI on a 1 km x 1 km grid, driven by observed meteorological data (1980–2011).
- primary aim: support understanding of climate-change impacts on water quantity and inform monitoring/policy decisions.
- includes a complementary dataset driven by UKCP18 Regional (12 km) climate projections (1980–2080) for comparative analysis.
- related datasets cover river flows across GB and NI; together with soil moisture data, support integrated hydrological monitoring.

## What the dataset contains
- Monthly mean soil moisture (m water per m soil; dimensionless θ) on a 1 km x 1 km grid across GB and NI.
- Output is daily-mean soil moisture averaged to monthly values, representing depth-integrated soil moisture for the whole soil column (0 ≤ θ ≤ 1).
- Spatial domain: GB and NI, with specific grid extents and a separate lake-identification file.
- Lake handling: lakes and reservoirs not explicitly modeled; lakes are treated as river cells. Two lake-grid files identify majority lake cells (>85% water cover).

## Model and inputs
- Model: Grid-to-Grid (G2G), a national-scale hydrological model run at 1 km grid with 15-minute time steps; outputs natural river flows and soil moisture.
- Calibration: uses spatial datasets rather than catchment-specific calibration; uses nationally applicable parameter values.
- Inputs required:
  - Precipitation: daily 1 km grids (CEH-GEAR).
  - Potential evaporation (PET): monthly 40 km grids for short grass (MORECS).
  - Temperature: daily 1 km grids (Met Office HadUK-Grid).
- Time handling: precipitation and PET distributed across model time-steps; temperature downscaled within the day using a sine curve.

## Data products and format
- Primary GB dataset: G2G_GB_mmsoil_obs_1980_2011.nc (monthly mean soil moisture for GB, Dec 1980–Nov 2011).
- Primary NI dataset: G2G_NI_mmsoil_obs_1980_2011.nc (monthly mean soil moisture for NI, Dec 1980–Nov 2011).
- Data format: NetCDF4, with time encoded as days since 1900-01-01; monthly values assigned to the first day of each month.
- Spatial coverage:
  - GB: 700 km x 1000 km domain on GB National Grid (0,0 to 700000,1000000 m).
  - NI: 187 km x 170 km domain on GB National Grid (-7000,440000 to 180000,610000 m).
- Lake grids: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc and UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc, with a 1/2/−9999 coding scheme for land, lake, sea.

## Relationship to other datasets
- These soil moisture estimates can be analyzed alongside:
  - UKCP18-driven G2G soil moisture dataset (1980–2080) for comparative climate-projection analysis.
  - River-flow datasets for GB and NI to examine the hydrological response under observed vs. projected conditions.
- The dataset complements existing MaRIUS-G2G-MORECS monthly soil moisture data, with updates limited to a shorter period and some land-sea mask adjustments and missing data infill differences.

## Usage notes and limitations
- Lakes and reservoir effects on downstream flows are not modeled; lake cells are treated as river cells, potentially affecting downstream estimates.
- Model performs best in catchments with natural flow regimes and reliable observed data; performance may be lower in highly anthropogenically altered systems.
- Spatial resolution is high (1 km) but not calibrated to individual catchments; suitable for regional- to national-scale monitoring and trend analysis.
- Data governance considerations: openly shared NetCDF4 files; metadata available; data provenance and credited sources specified; acknowledgement of NERC support.

## Data governance and provenance
- Funded by the Natural Environment Research Council under the UK-SCAPE National Capability programme.
- Acknowledgements: program and principal investigators cited; dataset citations and DOIs provided for reproducibility and proper attribution.

## Relevance for monitoring frameworks
- Provides high-resolution, observation-driven soil moisture data useful for environmental health monitoring, policy scrutiny, and decision-making.
- Supports data quality, metadata transparency, and data-sharing practices aligned with governance needs.
- Enables consistent tracking of soil-moisture changes over time and across regions, with potential integration into dashboards and reports for environmental monitoring programs.