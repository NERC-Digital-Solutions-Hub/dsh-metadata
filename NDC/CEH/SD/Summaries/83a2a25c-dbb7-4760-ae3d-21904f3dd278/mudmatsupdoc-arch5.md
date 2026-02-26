# DESCRIPTION

## Overview
- This dataset presents model output for different scenarios of treebelts situated downwind of an ammonia source, aiming to recapture ammonia and reduce emissions and their environmental/social impacts.
- Coverage: Great Britain (GB) on a 100 by 100 km grid (10,000 km²). Northern Ireland is represented by a single 10,000 km² square.
- Key focus: effect of canopy recapture and dispersion on ammonia concentrations near sensitive habitats; includes seasonal and meteorological variation.

## Contents and data scope
- Primary data file: GB_NH3recapture.csv, containing grid-based model outputs (latitude/longitude, grid square, year, season, and recapture metrics).
- Model inputs include:
  - Meteorology derived from CHESS-met (GB 1961–2017), aggregated to 100 km resolution; 2008–2017 used to represent a typical year with four days per season to capture seasonal variation.
  - Leaf Area Index (LAI) data varying by species, height, season, and grid-square; main canopy and backstop canopy specifics.
  - Tree height estimates by grid-square using Forest Research tools; backstop canopy fixed to conifer (Sitka Spruce) with seasonal constancy.
- Model framework:
  - MODDAS-2D (2D Lagrangian Stochastic dispersion model) for ammonia recapture.
  - OpenFOAM for turbulence input, with Segersson canopy modifications.
  - Coupled via a Python (2.7) coupler.
- Constant design parameters across runs: ammonia source area 15 m², 20 m distance to trees, 80,000 source particles, 800,000 canopy particles, ammonia source density 951 s m⁻³.

## Data content and structure details
- Variables and units (selected):
  - SEASON, Description and units: season (winter, spring, summer, autumn).
  - YEAR, TIME: year and time of runs (3 am or 3 pm).
  - LAD_BACK, LAD_MAIN: leaf area density for backstop and main canopy.
  - HEIGHT_MAIN, HEIGHT_BACK: canopy heights (m).
  - DEPTH_MAIN, DEPTH_BACK: canopy depths (m along X axis).
  - LAI_BACK, LAI_MAIN: leaf area index (dimensionless).
  - TOTAL_RECAPTURE: overall percentage recapture for the scenario (backstop + main canopy).
  - MAIN_RECAPTURE, BACK_RECAPTURE: recapture percentages for main and backstop canopies individually.
  - SDEN: source particle density (s m⁻³).
  - LATITUDE_WGS84, LONGITUDE_WGS84: geographic coordinates (WGS84).
  - SQ_NUMBER: GB grid square ID (1000 km² units; note Northern Ireland not in this field).
  - Other fields capturing year fractions and time steps.
- Grid design and seasonality:
  - Grid squares 1000 km²; GB coverage ensures full spatial context for the study area.
  - Seasonal LAI and meteorology incorporated via four-day-season representations.

## Provenance, methods, and processing
- Meteorology:
  - CHESS-met data used (GB 1961–2017), aggregated to 100×100 km and representative year (2008–2017) to reduce inter-annual variability; four days per season used for seasonal variation.
- Biological/physical inputs:
  - Tree height per grid-square derived with Forest Research DSS tools; LAI values derived from 3PGmix model using Sitka Spruce (conifer) and Aspen (broadleaf) references.
  - Backstop canopy fixed with conifer evergreen species (Sika spruce) and associated LAI values across years.
- Modeling workflow:
  - Input files created for MODDAS-2D and OpenFOAM; models run in parallel on LOTUS cluster (JASMIN).
  - Outputs provide percentage ammonia recapture for combined canopies and for each canopy separately.

## Quality control and validation
- Quality assurance steps:
  - Visual inspection of input data, mapping and QA/QC checks of meteorology.
  - LAI data reviewed by Forest Research experts.
  - Code reviews for input file generation; reliance on peer-reviewed models (OpenFOAM, MODDAS) with broad community support.

## Data accessibility and structure
- Data structure section (selected fields):
  - SEASON, Description and units
  - LAD_BACK, LAD_MAIN
  - HEIGHT_MAIN, HEIGHT_BACK
  - DEPTH_MAIN, DEPTH_BACK
  - LAI_BACK, LAI_MAIN
  - TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE
  - SDEN, LATITUDE_WGS84, LONGITUDE_WGS84
  - SQ_NUMBER, YEAR, TIME
- Northern Ireland:
  - Weather data sourced from the closest GB grid-square on the west coast of Scotland; NI is represented as a single 10,000 km² square in the grid scheme.

## Limitations and considerations for data stewards
- Northern Ireland meteorology uses a proxy from the nearest GB grid-square, which may introduce approximation errors for NI-specific conditions.
- Year aggregation (2008–2017) represents a typical year; inter-annual variability is reduced, which may limit applicability to atypical conditions.
- Some inputs (e.g., detailed NI forestry data) use non-public Forest Research tools; availability of exact inputs may be limited.
- The dataset uses specific model configurations (MODDAS-2D v2.7.1, OpenFOAM v1706 with Segersson canopy modifications); users should ensure compatibility with their analysis pipelines.

## Governance and stewardship recommendations
- Metadata enhancements:
  - Add dataset-level metadata including license, data creator, contact, version, update frequency, and data provenance trail.
- Provenance and lineage:
  - Document exact model versions, parameter values (beyond the constants listed), and any data transformations performed.
- Access and reuse:
  - Provide clear usage rights, citations, and recommended references (as listed) to ensure reproducibility.
- Data quality and maintenance:
  - Maintain QA logs and versioned releases; consider providing a sample workflow or scripts to reproduce the datasets.
- Cataloging guidance:
  - Register in data catalogs with fields for spatial resolution, temporal scope, input data sources (CHESS-met, LAI sources), model chain, and known limitations.

## References
- Forrester, D. I. & Tang, X. (2016). Analysing the spatial and temporal dynamics of species interactions in mixed-species forests and the effects of stand density using the 3-PG model.
- Loubet, B. et al. (2006). A coupled dispersion and exchange model for short-range dry deposition of atmospheric ammonia.
- Robinson, E. L. et al. (2020). CHESS-met meteorology dataset for Great Britain (1961–2017).
- Segersson, D. (2017). Tutorial to urban wind flow using OpenFOAM.
- Bealey, W. J. et al. (2014). Modelling agro-forestry scenarios for ammonia abatement in the landscape.