# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

## Overview and purpose
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum daily river flows on a 0.1° × 0.1° grid across West Africa for historical (1950–2005) and projected future (2006–2099) periods.
- Uses bias-corrected CMIP5 climate outputs (precipitation, near-surface air temperature, daily max/min temperatures) to drive the HMF-WA hydro-model.
- Aims to support understanding of climate-change impacts on river flows and to inform climate-compatible planning in the region.

## Data content and structure
- Model: Hydrological Modelling Framework - West Africa (HMF-WA); grid-based, spatially consistent flows across West Africa and the Sahel.
- Variables: monthly mean flows (MM) and annual maximum daily flows (AM) in m3 s-1.
- Resolution and domain: 0.1° × 0.1° grid covering latitudes 3°–26° N and longitudes -18°–25° E.
- Time periods: historical 1950–2005; future 2006–2099.
- Climate scenarios and ensembles: 76 CMIP5 realizations across three RCPs (RCP2.6: 20 members; RCP4.5: 27; RCP8.5: 29).
- Water-use scenarios: two future pathways
  - With population-driven water use (BC data)
  - Without population-driven changes (WO)
- Data format: NetCDF4 files; metadata-rich with dimensions Latitude, Longitude, and Time.

## Data generation and inputs
- Forcing data: bias-corrected CMIP5 outputs (precipitation, near-surface air temperature, daily max/min temps); potential evaporation estimated from temperature.
- Model design: parameterization uses physical/soil properties; accounts for anthropogenic water use, wetland inundation, and endorheic regions; not calibrated to individual catchments to ensure global spatial consistency and applicability to ungauged locations.
- Performance: validated against observed daily river discharge (GRDC) for 1981–2010 with NSE median ~0.62 and NSElog median ~0.82; higher skill for high flows, lower for some small/upstream catchments.

## Usage guidance and caveats
- Data are ensemble-based; no single realization is preferred—use the full ensemble to assess uncertainty.
- Direct comparisons to observed historical river flows are not appropriate; data are model-based projections.
- Spatial resolution (~10 km) limits applicability for catchments smaller than ~5000 km2.
- Suitability: planning for future floods and droughts, scenario analysis across RCPs, and exploration of flood-frequency relationships using annual maximum series.
- File naming conventions illustrate BC (bias-corrected) and WO (without population-driven changes); example patterns provided.

## Data access and provenance
- Data access: https://doi.org/10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4
- Primary reference and citation: Rameshwaran et al. (2021) NERC EDS Environmental Information Data Centre (EIDC) dataset; further access/usage terms at the same DOI.
- Contextual project: AMMA-2050 (Africa-focused climate and hydrology study); underpinning data and methodology referenced in accompanying literature.
- Data sources: CMIP5 bias-corrected variables available via AMMA-2050 data portal; observed river discharge from GRDC.

## Related outputs and formats
- Example outputs: maps and plots illustrating monthly means and AM flows (e.g., Niger River), and monthly/AM grids across West Africa for selected scenarios.
- Data format details: NetCDF with three dimensions (Latitude, Longitude, Time); suitable for GIS and programming environments (ArcGIS, NCView, Python, Fortran).

## Acronyms and terms (selected)
- AM: Annual Maximum
- MM: Monthly Mean
- CMIP5: Coupled Model Intercomparison Project Phase 5
- RCP: Representative Concentration Pathway
- NSE: Nash-Sutcliffe Efficiency
- WO: Water use that is the same as present day (without population-driven change)

## Key takeaways for analysts
- The HMF-WA dataset offers a comprehensive, grid-based, bias-corrected view of historical and future river flows across West Africa, suitable for ensemble-based impact assessments and policy planning.
- Use the full CMIP5 ensemble to capture the range of possible outcomes; avoid over-interpretation of any single realization.
- Combine with additional data layers (e.g., demographic, land-use, water management) to explore interactions with policy scenarios and to enhance usefulness for decision-making.
- Be mindful of limitations: coarse resolution, non-catchment-calibrated parameters, and non-direct comparability to observed historical flows. Access and cite using the provided DOIs.