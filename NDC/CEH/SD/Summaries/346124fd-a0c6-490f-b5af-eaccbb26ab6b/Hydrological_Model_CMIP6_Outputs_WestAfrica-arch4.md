# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean and annual maximum river flows (m3 s-1) on a 0.1° × 0.1° grid across West Africa for historical (1950–2014) and projected future (2015–2100) periods.
- Driven by bias-corrected CMIP6 daily climate model outputs (precipitation, daily max/min near-surface temperature, and near-surface air temperature), feeding the HMF-WA model.
- Part of AMMA-2050, a UK NERC/DFID FCFA initiative addressing monsoon changes and climate-compatible development in West Africa.
- Two future water-use scenarios: (i) water use varying with projected population growth and (ii) water use equal to present day; together they form an indicative envelope of potential impacts.

## Data and Modeling Approach
- Hydrological Model: Hydrological Modelling Framework – West Africa (HMF-WA), a physically-based grid-based model covering West Africa and the Sahel. Accounts for anthropogenic water use, wetland inundation, and regional hydrological features.
- Grid and domain: 0.1° × 0.1° resolution over lat 3°–26° N and lon -18°–25° E; designed to provide spatially consistent flows across the region, including ungauged locations.
- Inputs and driving data: Bias-corrected CMIP6 climate outputs (for 14 SSP126, 15 SSP245, 15 SSP585 ensemble members; 44 total realisations) used to drive the model; potential evapotranspiration estimated via established temperature-based methods.
- Scenarios and outputs: Historical (1950–2014) and Future (2015–2100) projections; monthly mean flows and annual maximum daily flows provided for each grid cell; two future water-use scenarios (with and without population-driven changes).
- Calibration: Parameters used without catchment-scale calibration to observed flows; designed for broad spatial consistency rather than perfect catchment fits.
- Climate ensembles: 17 historical realizations plus 44 future realizations across three SSP-RCPs; data emphasize the range of possible outcomes rather than a single forecast.

## Data Format and Access
- Output format: NetCDF4 files containing three dimensions (Latitude, Longitude, Time) with grid-based monthly means and annual maxima.
- File naming conventions: Examples include HMF-WA_MMFLOW_BC_<model>_HIST_195001-201412.nc and HMF-WA_AMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc; “BC” denotes bias-corrected climate input, “WO” denotes future scenarios without population-driven water-use changes.
- Temporal structure: Monthly means and annual maxima; annual maximum data reflect maximum daily river flows for each year, with year length depending on calendar (365/366/360 days as per CMIP6 model).
- Accessibility and tools: NetCDF format supports standard hydrological and geospatial tools (ArcGIS, NCView, Xconv) and programming environments (Fortran, Python); data can be subset by region or coordinate.
- Limitations on comparability: Do not compare CMIP6-driven simulations directly to observed historical flows; ensemble members cannot be ranked as more reliable than others.

## Performance and Limitations
- Validation: Model performance assessed against observed daily river discharge at 20 GRDC stations for 1981–2010 using CHIRPS precipitation and GLEAM potential evaporation; NSE median ~0.62 and NSE log ~0.82, with better performance for high flows than low flows.
- Limitations: Lack of catchment-level calibration may reduce accuracy for some smaller or upland catchments; predictions are more robust for broad West Africa but can be less reliable for finer-scale hydrology.
- Assumptions: Future water use constrained to either population-driven or present-day levels; river networks, lakes, reservoirs, and wetlands are assumed not to change significantly by 2100.
- Data scope caveats: The CMIP6-based results are provided as an ensemble to capture uncertainty; no single ensemble member is preferred; broader interpretation should consider the full range of projections.

## Applications and Use Cases
- Planning for floods and droughts: Spatial projections support country-level and regional planning across West Africa.
- Scenario analysis: Compare impacts across SSP126, SSP245, and SSP585 futures and across population-driven vs present-day water-use assumptions.
- Extremes analysis: Use annual maximum flows to construct flood-frequency curves and study changes in extreme river flows; feasible for Gringorten plotting positions and generalized logistic distributions with L-moments.
- Comparative studies: Users can contrast CMIP6-driven HMF-WA results with CMIP5 outputs to identify differences in future hydrological projections.
- Data utility notes: Useful for policy and adaptation planning, infrastructure design, and risk assessment in a climate-change context, with an emphasis on understanding uncertainty across an ensemble.

## Data Sources and Acknowledgements
- Observed river discharge: Global Runoff Data Centre (GRDC).
- Observational context and modelling framework: AMMA-2050 project; HMF-WA model development and CMIP6-driven simulations described in Rameshwaran et al. and related works.
- Support: UK NERC/DFID FCFA program; data and metadata detailed in associated publications and data records.

## Practical Considerations for Data Leaders
- Data governance: Large ensemble size (44 future realizations) offers a robust basis for uncertainty quantification but requires careful storage, metadata management, and clear guidance for end-users on interpretation.
- Metadata and discoverability: NetCDF headers provide metadata; ensure documentation includes file naming conventions, scenario definitions, calendar types, and grid mapping to aid discoverability.
- Data strategy alignment: This dataset aligns with regional climate impact assessment needs (flood/drought planning, water resource management) and demonstrates the value of ensemble, bias-corrected climate inputs for downstream hydrological impact modeling.
- Cross-domain collaboration: Potential for integration with regional water-use planning, infrastructure resilience, and policy-making networks; supports a broader data ecosystem for climate-resilient development in West Africa.