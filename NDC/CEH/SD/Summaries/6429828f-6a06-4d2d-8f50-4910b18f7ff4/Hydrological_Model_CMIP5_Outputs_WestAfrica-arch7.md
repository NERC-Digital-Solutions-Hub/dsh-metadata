# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows on a 0.1° × 0.1° grid across West Africa for historical (1950–2005) and projected future (2006–2099) periods.
- Uses bias-corrected CMIP5 climate inputs to drive the HMF-WA model, with two future water-use scenarios.

## Data products and structure
- Spatial resolution and extent:
  - Grid: 0.1° × 0.1° (~10 km × 10 km).
  - Domain: West Africa, latitudes 3°–26° N, longitudes -18°–25° E.
- Variables and units:
  - Monthly mean flows (MM) and annual maximum daily flows (AM) in m³ s⁻¹.
- Temporal and ensemble structure:
  - 29 historical CMIP5 realizations and 76 future realizations across three RCPs (RCP2.6, RCP4.5, RCP8.5).
  - Future simulations include scenarios with (BC) and without (WO) the impact of population-driven water use.
- Data format and file naming:
  - NetCDF4 format.
  - File naming conventions reflect MMFLOW and AMFLOW, BC/WO, model, RCP, and period (e.g., HMF-WA_MMFLOW_BC_ACCESS1.0_RCP8.5_200601-209912.nc).
  - Three possible year-day calendars per CMIP5 model (365/366, 365, or 360 days/year).

## Modelling approach
- Hydrological framework:
  - HMF-WA is a grid-based, physically-based, spatially distributed model designed for West Africa, incorporating anthropogenic water use, wetland inundation, and endorheic features.
- Forcing and bias correction:
  - Driven by bias-corrected CMIP5 daily climate variables (precipitation, near-surface air temperature, daily max/min temperatures) and derived PET, on a 0.5° × 0.5° Africa-wide basis (Famien et al., 2018).
- Calibration and performance:
  - No catchment-scale calibration to observed flows; uses spatial datasets of physical/soil properties to configure hydrology.
  - Assumptions include static future water use per capita (scaled by population) and little change in rivers, lakes, reservoirs, and wetlands to 2100.
  - Performance assessment (1981–2010) indicates good handling of high flows and moderate handling of low flows (NSE median ~0.62; NSElog median ~0.82).

## Data access and citation
- Access:
  - Data accessible via DOI: 10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4
  - Additional access and usage terms available at the same DOI page and related AMMA-2050 resources.
- Citation:
  - Rameshwaran, P., Bell, V.A., Davies, H.N., Kay, A.L. (2021). Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data. NERC EDS Environmental Information Data Centre (Dataset). https://doi.org/10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4

## Usage and limitations
- What the data are suitable for:
  - Planning for future floods and droughts in West Africa at a gridded, regional scale.
  - Analyzing impacts of climate change on river flows under multiple RCP scenarios and future water-use assumptions.
  - Deriving flood frequency characteristics using annual maximum flows (AM) and evaluating scenarios with Gringorten plotting positions and L-moments.
- Important caveats:
  - Full CMIP5 ensemble is too large for online storage; use the ensemble to assess uncertainty rather than selecting a single “best” member.
  - Gridded flows are not directly comparable to observed river flows; coarse resolution (~10 km) limits applicability for catchments smaller than ~5,000 km².
  - Historical simulations are climate-model-driven rather than driven by observed historical data.
  - Two future water-use scenarios provide an envelope of potential impacts; results depend on assumed population-driven water demand and static non-population water-use assumptions.
- Data use guidance:
  - Data can be read in various GIS/analysis tools that support NetCDF (ArcGIS, NCView, Xarray-based workflows, Python/Fortran).
  - For detailed river-by-river interpretation, identify cells corresponding to interest areas; aggregate to higher-level regions as needed.

## Applications and context
- Context:
  - Outcome of AMMA-2050 project (UK NERC/DFID FCFA) focused on West African monsoon changes and climate-compatible development.
- Practical applications:
  - Spatial planning for floods and drought resilience under different climate futures.
  - Country- or river-specific analyses to understand potential changes in flow regimes and extreme events.
  - Use of AM flows for flood-frequency analysis, with attention to stationarity assumptions and ensemble uncertainty.

## Data sources and acknowledgments
- Forcing data:
  - CMIP5 bias-corrected variables from 20 model realizations (RCP2.6, RCP4.5, RCP8.5); bias-corrected Africa-wide forcing grid from Famien et al. (2018).
- Observed data for validation:
  - GRDC observed daily river discharge data (20 gauging stations across West Africa).
- Project and funding:
  - AMMA-2050 and FCFA programs; data preparation supported by NERC Hydro-JULES.