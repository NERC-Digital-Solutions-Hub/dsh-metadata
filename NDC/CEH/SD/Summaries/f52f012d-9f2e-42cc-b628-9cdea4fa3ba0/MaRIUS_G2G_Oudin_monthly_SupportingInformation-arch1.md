# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) funded by UK NERC (2014-2017) developed a risk-based drought and water scarcity framework.
- Provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1km x 1km grid across Great Britain for 1891-2015.
- Variables: flow (m3 s-1) and soil moisture (mm water per m soil); monthly means of daily values (09:00–09:00).
- Outputs are useful for comparing with observed gauged flows and for drought/water-availability analyses; includes spatial context via catchments and gauging station locations.

## Hydrological model and interpretation
- Grid-to-Grid (G2G) is a national-scale hydrological model with 1km grid resolution and 15-minute time-step.
- Parameterised using digital soil, land-cover, topography datasets; accounts for urban/suburban land-cover effects on runoff.
- Calibrated using spatial datasets rather than catchment-specific calibration; uses nationally applicable values for certain parameters (e.g., kinematic wave speeds).
- Outputs represent natural flows (i.e., before major artificial abstractions/discharges) and depth-integrated soil moisture across the full soil column.
- Optional snow module not used here; precipitation input assumes rain-only for the model, with limited impact on drought signals.

## Driving data and inputs
- Meteorological driving data are observation-based:
  - 1km x 1km daily rainfall grids (CEH-GEAR).
  - Monthly potential evaporation (PE) estimates derived from temperature on a 5km x 5km grid (temperature-based method).
- Gaps in early 20th century rainfall data were spatially infilled; PE is generated from temperature with long-term corrections to align with established references.
- PE and rainfall are disaggregated to the model's 15-minute time-step (each source scaled down accordingly).

## Data content and formats
- Outputs provide:
  - Flow: monthly means of daily natural flows (m3 s-1).
  - Soil moisture: monthly means of daily soil moisture (mm water/m soil), i.e., depth-integrated values.
- Geographic and temporal coverage:
  - Historical period: 1891–2015.
  - Domain: 700 km x 1000 km GB national grid; 1km x 1km grid cells (land only; sea cells missing).
- File format and naming:
  - NetCDF4 file: G2G_Oudin_var_1891_2015.nc.
  - Variables: 'flow' or 'soil'.
  - Time: days since 1891-01-01; monthly values assigned to the first day of each month.
  - Spatial indexing: grid cell centers, with missing values set to -9999 for sea or non-data cells.
- Auxiliary spatial data:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: digitally-derived catchment area (km2) draining to each 1km grid box.
  - MaRIUS_G2G_NRFAStationIDGrid.nc: locations of NRFA gauging stations mapped to 1km grid cells (1285 stations; land vs sea encoded, with -9999 for sea).
  - MaRIUS_NRFAStationIDs.csv: NRFA station IDs corresponding to grid cells.

## How to use MaRIUS-G2G-Oudin-monthly data
- Compare G2G natural-flow estimates with observed NRFA river flows to assess model performance.
- Best performance in catchments with natural flow regimes and accurate observed flows; less accurate where significant abstractions/discharges or complex sub-surface hydrology are present.
- Use the NRFA station alignment dataset to select the appropriate 1km grid cell for a given gauging station; note potential discrepancies in small catchments due to grid discretisation.
- Soil moisture values are depth-integrated over the soil column, useful for drought-related analyses but should be interpreted in the context of the underlying soil properties and grid-scale averaging.

## Spatial details and caveats
- Flow estimates are provided for every land grid box; sea grid boxes are set to missing.
- The grid cell used to represent a NRFA gauging station may not perfectly match the observed catchment area, especially for small basins.
- The model assumes only rainfall-driven input (no explicit snow module in this dataset), which may influence hydrological responses under certain conditions.
- Calibration is not performed per-catchment; parameters are applied nationally, which has implications for local accuracy.

## Acknowledgements and references
- Dataset outcomes from the MaRIUS project (NE/L010208/1) within the UK Drought and Water Scarcity programme.
- Notable references include Bell et al. (2009, 2016), Davies & Bell (2009), Hough & Jones (1997), Keller et al. (2015), Oudin et al. (2005), Perry & Hollis (2005), Rudd et al. (2017), Kay et al. (2018).

## Figure
- Figure 1 illustrates example outputs: grids for flow and soil moisture, NRFA gauging station locations, and catchment-area grid over Wales, highlighting Wales’ location within the domain.