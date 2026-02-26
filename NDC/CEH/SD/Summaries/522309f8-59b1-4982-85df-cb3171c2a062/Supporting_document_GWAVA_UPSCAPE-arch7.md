# GWAVA Modelling- UPSCAPE

## Overview
- GWAVA 5.0 is a large-scale, semi-distributed gridded water resources model by UK Centre for Ecology & Hydrology.
- Produces daily, grid-level hydrological and water-demand outputs for the Cauvery Basin at 0.125-degree resolution (444 modelling cells).
- Combines natural processes with anthropogenic stress, including domestic, industrial, agricultural, and irrigation demands, with irrigation driven by crop type and planting month.
- Data intended for GIS-based analysis and map-style presentation of water resources and demands under multiple climate and socio-economic scenarios.

## Model Setup and Purpose
- Uses a lumped probabilistic soil moisture storage (PDM), surface storage, and groundwater storage framework to estimate local runoff per grid cell.
- Incorporates a demand-driven routine to account for urban, rural, livestock, industrial, and irrigation needs.
- Domestic and livestock demands are temporally static but spatially dynamic; irrigation demand is both temporally and spatially dynamic.
- Cauvery Basin modeled with 444 cells at 0.125-degree resolution, including major and minor reservoirs and agricultural areas.

## Spatial and Temporal Scope
- Spatial: Cauvery Basin (grid-based, 0.125-degree cells; 444 cells).
- Temporal: daily time steps within baseline (1986–2005) and future periods (2041–2060, 2061–2080), across multiple climate and socio-economic scenarios.

## Climate Scenarios and Ensemble
- Future climate represented via ensemble climate datasets under multiple pathways:
  - Climate models: BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M, and others.
  - Scenarios: SSP1 (SDG-focused, low material growth), SSP2 (business as usual), SSP3 (policy shifts with rapid development/degradation).
  - RCP representations: RCP4.5 and RCP8.5 included in ensemble runs.
- Data organized to support scenario-based GIS analyses for 2041–2060 and 2061–2080 windows.

## Variables and Units (Table 2 Summary)
- TotQ: Total runoff, units m3/s, description: mean runoff per grid box per day (positive land-to-river flux).
- Aqlevel: Aquifer level, units m below ground, mean per grid box per day.
- Urban_dems: Urban domestic demand, m3/s (mean per grid box per day).
- Rural_dems: Rural domestic demand, m3/s (livestock-related demand).
- Livestock_dems: Livestock demand, m3/s (cattle and small ruminants).
- Industrial_dems: Industrial demand, m3/s.
- Irrigation_dems: Irrigation demand, m3/s (includes irrigation efficiency; calculated from irrigated crops).
- Unfulfilled demands: Daily, grid-mean values for unfulfilled urban, rural, livestock, industrial, irrigation demands.
- All outputs represent daily means over each grid cell.

## Data Structure and File Organization
- Data delivered as seven CSV files.
- Common header fields in all files: xll (lower-left x coordinate), yll (lower-left y coordinate), year, timestep (Julian day 1–366).
- File contents:
  - Baseline_1986_2005.csv: baseline daily variables (1986–2005).
  - Ensemble_climate_2041_2060.csv: ensemble climate for 2041–2060 under RCP4.5 and RCP8.5.
  - Ensemble_climate_2061_2080.csv: ensemble climate for 2061–2080 under RCP4.5 and RCP8.5.
  - SSPs_2041_2060.csv: SSP1–SSP3 for 2041–2060 (daily).
  - SSPs_2061_2080.csv: SSP1–SSP3 for 2061–2080 (daily).
  - Ensemble_climate_SSPs_2041_2060.csv: combinations of RCPs and SSP1/SSP3 for 2041–2060 (daily).
  - Ensemble_climate_SSPs_2061_2080.csv: combinations of RCPs and SSPs for 2061–2080 (daily).
- Data labeling within files uses:
  - BL: Baseline (1985–2005 range)
  - ENA: Ensemble climate data
  - RCP: Representative concentration pathway (4.5 or 8.5)
  - SSP: Socio-Economic Pathway (SSP1, SSP2, SSP3)
- Outputs are daily means over grid boxes, suitable for GIS time-series analysis and mapping.

## Quality Control and Validation
- Calibrated at 14 gauging stations using SIMPLEX auto-calibration (parameters for routing, soil moisture capacity, and rooting depth).
- Validated at the same 14 stations plus 200 groundwater wells over different periods.
- Performance reported as Kling-Gupta Efficiency (KGE) values per site.
- Some sites show strong performance (e.g., KGE up to ~0.82) while others show lower or negative validation KGE (e.g., -1.27 at Tbekuppe for 2001–2003), indicating variable accuracy across locations and periods.

## Practical GIS Considerations
- Data are grid-based with explicit grid coordinates (xll/yll) enabling georeferencing for rasterization or conversion to GIS-friendly formats.
- Daily time steps across multiple scenarios allow for rich spatial-temporal analysis and visualization of water availability, needs, and deficits.
- Baseline and future scenario datasets enable comparative GIS mapping of changes under climate and socio-economic futures.
- Consumers may need to convert CSV time-series to raster or NetCDF formats and align to a GIS grid framework for map-based products.

## Acknowledgements
- Recognizes CMIP and the climate modeling groups contributing model outputs; U.S. Department of Energy’s Program for Climate Model Diagnosis and Intercomparison for coordinating software infrastructure and portal development.