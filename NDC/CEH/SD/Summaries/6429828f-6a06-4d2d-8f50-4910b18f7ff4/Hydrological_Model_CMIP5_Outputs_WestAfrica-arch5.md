# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows on a 0.1° × 0.1° grid across West Africa.
- Covers historical period (1950–2005) and future projections (2006–2099) driven by bias-corrected CMIP5 climate data.
- Two future water-use scenarios: (i) water use varying with projected population change, (ii) water use staying at present-day levels (WO).
- Part of AMMA-2050 regional hydrological modelling; intended to support climate-impacts planning and climate-adaptation decisions.

## Data content and structure
- Domain and resolution
  - West Africa: lat 3°–26° N, lon -18°–25° E
  - Grid resolution: 0.1° × 0.1° (~10 km × 10 km)
- Variables and time
  - Monthly Mean Flows (MMFLOW): monthly mean river flows (m3 s-1)
  - Annual Maximum Flows (AMFLOW): annual maximum of daily river flows (m3 s-1)
  - Periods: historical 1950–2005; future 2006–2099
- Ensemble and scenarios
  - 29 historical CMIP5 realizations
  - 76 future realizations across RCP2.6, RCP4.5, RCP8.5
  - For each realization, two water-use scenarios: BC (bias-corrected CMIP5 input with population-related water use) and WO (same as present-day)
- Data format and access
  - NetCDF-4 format with dimensions: Latitude, Longitude, Time
  - Metadata-rich headers; suitable for GIS and programming tools (Python, Fortran, ArcGIS, NCView, etc.)
  - Files are too large to share online as a single ensemble; data provided as gridded products at 0.1° resolution

## Modelling approach and projections
- Hydrological model: Hydrological Modelling Framework-West Africa (HMF-WA), a grid-based, physically-based model accounting for anthropogenic water use, wetlands, and endorheic regions
- Forcing data: bias-corrected CMIP5 daily climate variables (precipitation, near-surface air temperature, daily max/min temperatures); precipitation and temperature bias-corrected to 0.5° × 0.5° grid over Africa
- Assumptions and limitations
  - HMF-WA parameters are not calibrated to individual catchments; uses physical/soil properties to set model conditions
  - Future water use is driven either by population growth or held constant (WO)
  - Rivers, lakes, reservoirs, and wetlands are assumed not to change significantly between present day and 2100
- Validation and performance
  - Validation against observed data (1981–2010) shows NSE ≈ 0.62 and NSE-log ≈ 0.82 across West Africa; smaller catchments and flashy rivers may be less well represented
  - All results are ensemble-based; no single realization is preferred; results reflect uncertainty across CMIP5 models and scenarios

## Data access, licensing and citation
- Data access
  - Access and terms: https://doi.org/10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4
  - Full citation required: Rameshwaran et al. (2021) NERC EIDC dataset; access/terms: https://doi.org/10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4
- Usage notes
  - Data are provided to support planning for floods and droughts; results should be interpreted as projections under specified CMIP5 realizations and water-use scenarios
  - Do not compare CMIP5 ensemble members to observed river flows; comparisons should be within the same CMIP5 model across periods/SCENARIOS
  - Data available for country/raster cell identification, but coarse resolution (~10 km) limits catchment-scale (sub-5000 km2) analyses
- Documentation and provenance
  - AMMA-2050 project context; bias-corrected climate inputs (Famien et al., 2018)
  - Model and methodology described in accompanying publications and project notes

## Data quality, validation, and limitations
- Strengths
  - High-resolution gridded river-flow estimates across a large, ungauged West African domain
  - Ensemble approach captures a range of possible futures and water-use trajectories
- Limitations
  - Non-calibrated parameters may reduce accuracy for specific basins; performance is better for high flows than low flows
  - Assumed static river networks, lakes, reservoirs, and wetlands; potential future changes not captured
  - Bias-correction narrows uncertainty range; using full ensemble remains important to reflect residual uncertainty
- Data quality indicators
  - Documented performance metrics (NSE, NSE-log) from validation period
  - Acknowledgement of uncertainties due to model structure, forcing data, and scenario assumptions

## Usage guidance and applications
- Intended use
  - Support planning for future floods and droughts in West Africa and country-level analyses
  - Explore impacts of climate change under multiple RCPs and water-use trajectories
- Analytical approaches
  - Use AMFLOW for flood-frequency analyses (Gringorten plotting positions, L-moments) while noting stationarity assumptions
  - Compare across CMIP5 models for a given country/region to assess uncertainty
- Practical considerations
  - Spatial resolution limits interpretation for small basins
  - NetCDF format requires appropriate tools; data can be converted to ASCII if needed, acknowledging large file sizes
  - Always cite the dataset and publication when using the data in outputs

## Data governance, sustainability, and stewardship
- Data governance
  - Centralized, citable data package with clear provenance and usage terms
  - Metadata-rich NetCDF files enabling discoverability and reuse
  - Explicit licensing/terms via data provider links; requires proper citation
- Data storage and maintenance
  - Large ensemble; recommended storage with regional or national sub-sets as needed
  - Maintain versioning and provide method updates if new bias-corrected inputs or improved HMF-WA configurations become available
- Documentation and metadata
  - File naming conventions clearly indicate model, bias-correction, scenario (HIST, RCP, WO), and date range
  - Documentation available to describe domain, variables, units, time conventions, and calendar (including 360-day year options)

## Data sources and acknowledgements
- CMIP5 bias-corrected climate inputs (precipitation, near-surface air temperature, daily max/min temperature)
- Observed river discharge data from GRDC for validation
- AMMA-2050 project context and NERC FCFA support; data preparation support from Hydro-JULES program
- Key references: Famien et al. 2018; Rameshwaran et al. (submitted); Bell et al. 2007; Crooks et al. 2014; supporting methodological papers on bias correction and hydrological modelling in Africa