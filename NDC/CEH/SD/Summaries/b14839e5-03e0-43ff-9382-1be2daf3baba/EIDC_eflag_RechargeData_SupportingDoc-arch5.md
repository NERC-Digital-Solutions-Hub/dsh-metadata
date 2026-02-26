# Distributed potential recharge projections for the UK, based on UK Climate Projections 2018 (UKCP18) data, from the Enhanced Future Flows and Groundwater (eFLaG) project Supporting Documentation

## Overview
- Dataset: 2 km gridded daily projections of potential groundwater recharge for mainland Great Britain (1981–2080) using the ZOODRM model driven by bias-corrected UKCP18 climate projections; includes corresponding gridded observation-driven time series (1962–2018).
- Origin: eFLaG project funded by the Met Office component of the Strategic Priorities Fund Climate Resilience Programme; collaboration between BGS, UKCEH, and HR Wallingford.
- Related data: Area-averaged groundwater recharge estimates at groundwater-body scale (link provided in the documentation).

## Data generation methods
- ZOODRM (distributed recharge model): 2 km grid; estimates potential recharge using the FAO 56 approach, removing actual evaporation and soil moisture deficit to compute potential recharge as a fraction of excess water via a runoff coefficient.
- UKCP18 processing: 12 km high-resolution projections downscaled to 2 km for ZOODRM; precipitation bias-corrected using monthly means; daily time series created for 1980s–2080.
- Data types:
  - simobs: Observation-driven daily gridded simulations (1962–2018).
  - simrcm: Regional Climate Model-driven daily gridded simulations (1981–2080).
- Calibrations and evaluations: Two-stage QA–QC against observed river flows and climate-model-driven baselines to assess performance.

## Nature and units of recorded values
- Units: millimetres per day (mm/day).
- Spatial grid: 2 km, British National Grid coordinates (meters).
- Time indexing:
  - simobs: Standard Gregorian calendar (days since 1950-01-01).
  - simrcm: 360-day calendar (days since 1950-01-01).

## Data structure and access
- File format: NetCDF.
- Time segmentation: Data split into continuous 5-year slices for both simobs and simrcm simulations.
- File naming conventions:
  - simobs: eflag_gridded_potential_recharge-simobs-YEAR_FROM-YEAR_TO.nc
  - simrcm: eflag_gridded_potential_recharge-simrcm-RCM-YEAR_FROM-YEAR_TO.nc
  - RC M = UKCP18 RCM code (e.g., rcm1).
- Related materials: Observation-driven dataset available via CEH catalogue; accompanying scientific articles and references provided.

## Quality control and validation
- Stage 1: Compare model simulations driven by observed climate data with observed river flow statistics (National River Flow Archive).
- Stage 2: Compare climate-model-driven recharge with observation-driven recharge over the common baseline period (1989–2018).
- Documentation cites detailed methods in the associated ESSD journal article and related references.

## Governance, metadata, and provenance considerations for Data Stewards
- Provenance: Datasets produced by BGS with UKCEH collaboration; based on ZOODRM, UKCP18 (HadGEM3-GC3.05 and HadREM3GA705), and bias correction steps.
- Metadata needs:
  - Model versions and configurations (ZOODRM, UKCP18 processing steps, bias correction method).
  - Grid resolution, coordinate reference system, and calendar details (including 360-day calendar for simrcm).
  - Time period coverage for each file and grouping (5-year slices).
  - Data lineage linking simobs to observed baselines and simrcm to UKCP18 projections.
- Access and sharing:
  - NetCDF data with explicit file-level time slices; ensure discoverability via catalogues (e.g., CEH) and related project pages.
  - Note and document any embargoes, licensing, or usage restrictions; include clear caveats on calendar differences and potential applicability limitations.
- Update and maintenance:
  - Track UKCP18 updates or newer downscaling/bias-correction schemes; plan versioned releases if updated.
  - Maintain cross-links to area-averaged recharge dataset and to the primary publications.
- Usability improvements:
  - Provide companion metadata records and usage guidelines to assist data users in applying the 2 km, 2D grid data for hydrological or groundwater studies.
  - Document any known limitations, such as resolution constraints, calendar differences, or model assumptions.

## Key takeaways for Data Stewards
- Ensure complete, versioned metadata capturing model components, processing steps, calendar conventions, and file-structure details.
- Maintain clear provenance links between raw simulations, bias-corrected outputs, and derived recharge estimates.
- Preserve accessibility through standard formats (NetCDF) and well-documented file naming and time indexing conventions.
- Communicate limitations and appropriate use cases, particularly regarding spatial resolution, temporal coverage, and calendar differences between simobs and simrcm.
- Plan for ongoing governance to incorporate methodological updates and related datasets within the eFLaG framework.