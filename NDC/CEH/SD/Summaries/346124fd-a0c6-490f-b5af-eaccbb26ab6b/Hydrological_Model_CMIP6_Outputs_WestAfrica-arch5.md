# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows on a 0.1° × 0.1° grid across West Africa.
- Covers historical period (1950–2014) and projected future period (2015–2100).
- Driven by bias-corrected CMIP6 climate data, using a distributed hydrological model (HMF-WA).
- Two future water-use scenarios: (i) linked to projected population changes, (ii) same as present day (WO).

## Dataset scope and domain
- Spatial domain: West Africa, roughly 3°–26° N and -18°–25° E.
- Grid resolution: 0.1° × 0.1° (~10 km × 10 km).
- Variables: monthly mean flows (m3 s−1) and annual maximum daily flows (m3 s−1).
- Temporal coverage: 1950–2014 (historical) and 2015–2100 (future).

## Hydrological model and climate data
- Model: Hydrological Modelling Framework – West Africa (HMF-WA), a grid-based, physically-based rainfall–runoff model.
- Domain features: accounts for anthropogenic water use, wetland inundation, and regional hydrological features (endorheic regions).
- Calibration: parameters are not calibrated to individual catchments; relies on spatial physical and soil data to configure hydrology for a broad domain.
- Climate inputs: bias-corrected CMIP6 daily variables (precipitation, near-surface temperature, daily max/min temperature); potential evaporation estimated from temperature data.
- Climate ensembles: 44 CMIP6 realizations across SSP126, SSP245, and SSP585 (plus 17 CMIP6 historical realizations).

## Climate projections and ensemble design
- SSP-RCP contexts: SSP126 (sustainability), SSP245 (middle of the road), SSP585 (fossil-fuelled development).
- Two future water-use scenarios: population-driven water use vs present-day water use (WO).
- Historical runs: driven by climate model realizations for 1950–2014 (not direct observations).
- Future runs: 2015–2100, providing an envelope of possible river-flow changes under different climate and water-use futures.

## Data format, structure, and access
- Output format: NetCDF4 files with header metadata; three dimensions: Latitude, Longitude, and time.
- Data products:
  - MMFLOW_BC_<model>_HIST_195001-201412.nc (monthly mean flows, historical, bias-corrected)
  - MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc (monthly mean flows, future, bias-corrected)
  - MMFLOW_BC_WO_<model>_<SSP-RCP>_201501-210012.nc (monthly mean flows, future, no population-driven water-use)
  - AMFLOW_BC_<model>_HIST_195001-201412.nc (annual maximum flows, historical, bias-corrected)
  - AMFLOW_BC_<model>_<SSP-RCP>__201501-210012.nc (annual maximum flows, future, bias-corrected)
  - AMFLOW_BC_WO_<model>_<SSP-RCP>_201501-210012.nc (annual maximum flows, future, no population-driven water-use)
- Example file naming: HMF-WA_MMFLOW_BC_BCC-CSM2-MR_SSP585_201501-210012.nc.
- Model ensemble notes: no single model is rated as preferred; use full ensemble to assess uncertainty. Comparison across CMIP6 realizations is valid within the same model, but not directly to observed flows.

## Data quality, limitations, and interpretation
- Performance assessment: validation against observed flows (1981–2010) shows moderate to good skill for high flows (NSE ~0.62; NSE log ~0.82), with smaller catchments and flashy systems often performing worse.
- Calibration caveat: parameters are not catchment-calibrated; may reduce accuracy for some locations but increases spatial coverage, including ungauged sites.
- Baseline vs future: baseline flows are driven by climate model realizations rather than observed data; future projections reflect model ensembles and bias correction, not a single forecast.
- Spatial resolution limitation: 10 km grid does not resolve rivers below ~5000 km2 catchments; suitable for regional planning and sectoral assessments rather than pinpoint hydrographs for small basins.
- Data product trade-off: bias-corrected climate inputs reduce some uncertainty but may narrow overall uncertainty ranges; users should consider both bias-corrected and, where useful, uncorrected perspectives.

## Governance, metadata, and provenance
- Provenance: outputs are part of AMMA-2050, a UK NERC/DFID FCFA project; data are documented with metadata in NetCDF headers.
- Documentation references: detailed methodology and performance assessments are documented in Rameshwaran et al. (2021a, 2021b).
- Data model and versioning: ensemble-based approach with multiple CMIP6 models; file naming encodes model, SSP-RCP, and WO/BC status, aiding traceability.

## Suggested applications and use cases
- Planning: support for future flood and drought scenario planning in West Africa.
- Country/rivers analysis: assess impacts of climate change across countries or broad river sectors; explore different SSP-RCP futures and water-use assumptions.
- Extreme value analysis: derive flood-frequency curves by ordering annual maxima and fitting distributions (e.g., Gringorten plotting positions with L-moments) while noting potential non-stationarity caveats.
- Comparison across climate frameworks: analyze differences between CMIP5 and CMIP6-derived hydrological projections using HMF-WA (noting methodological differences).

## Data sources and acknowledgments
- Observed daily river discharge data used for validation sourced from the Global Runoff Data Centre (GRDC).
- Climate inputs derived from CMIP6 models; baseline and future scenarios coordinated with FAO AQUASTAT, UN population projections, and related data sources.
- Acknowledgments to AMMA-2050 and FCFA program support.