# Trees have the potential to recapture ammonia emissions from animal housing units or areas where animals are able to roam free range under the canopy, with associated benefits for animal welfare and the environment.

## Overview
- Dataset of model outputs for different scenarios of treebelts situated downwind of an ammonia source.
- Geographic coverage: Great Britain (GB) and Northern Ireland (NI); GB modeled on a 100 km × 100 km grid (10,000 km²), NI treated as a single 10,000 km² square.
- Purpose: assess ammonia recapture by canopy and its effect on dispersion near sensitive habitats; supports map-based analyses of spatial influence of shelterbelts.

## Spatial coverage and data structure
- GB grid: 100 × 100 km cells (10,000 km² total); NI: single 10,000 km² cell.
- Each grid cell identifies center coordinates (latitude and longitude in WGS84) and a grid ID (SQ_NUMBER).
- Outputs include season, year (5, 15, 25, 50 years since planting), and time of day (3 am or 3 pm).
- Key spatially-referenced variables:
  - LATITUDE_WGS84, LONGITUDE_WGS84
  - SQ_NUMBER (GB grid cell ID; note NI uses a single entry)
  - YEAR, TIME
- Ammonia recapture metrics:
  - TOTAL_RECAPTURE (overall percent recapture for the chosen canopy configuration)
  - MAIN_RECAPTURE (recapture by main canopy)
  - BACK_RECAPTURE (recapture by backstop canopy)
- Canopy parameters:
  - LAD_MAIN, LAD_BACK (Leaf Area Density for main and backstop canopies)
  - LAI_MAIN, LAI_BACK (Leaf Area Index)
  - HEIGHT_MAIN, HEIGHT_BACK (canopy heights)
  - DEPTH_MAIN, DEPTH_BACK (canopy depths along the X axis)

## Meteorology and input data
- Meteorological data from CHESS-met (GB, 1961–2017); aggregated to 100 km × 100 km resolution for GB.
- 2008–2017 daily CHESS data averaged to represent a typical year; four days representing each season used to capture seasonal variation.
- Variables used: relative humidity, air temperature, wind speed; Photosynthetically Active Radiation (PAR) derived from CHESS shortwave radiation.
- NI weather data derived by selecting the closest GB grid-square on the west coast of Scotland.

## Treebelt design and LAI modeling
- Treebelt design follows a common structure: a main canopy and a backstop canopy.
- Main canopy:
  - Mixed planting (broadleaf/conifer) with 2–4 m spacing.
  - Open to allow ammonia plume entry; positioned at the front of the shelter belt.
- Backstop canopy:
  - Conifer/evergreen type (e.g., Sika spruce) with spacing ≤ 2 m for a thick barrier.
- Leaf Area Index (LAI) calculations:
  - Main canopy LAI varies with tree age (0, 5, 15, 25, 50 years) and season; values provided for spring, summer, autumn, winter.
  - Backstop canopy LAI fixed by design (seasonal variation not applied); LAI values provided for 1–5 years corresponding to canopy development.
- LAI tables derived from the 3PGmix model (Sitka spruce for conifers; Aspen for broadleaf).

## Modelling approach and data generation
- Coupled models:
  - MODDAS-2D v2.7.1: 2D Lagrangian stochastic dispersion/deposition model to compute ammonia recapture.
  - OpenFOAM v1706 (with Segersson canopy physics modifications): turbulence input for MODDAS.
  - Python (2.7) coupler to integrate inputs and outputs.
- Computation performed on a high-performance LOTUS cluster on JASMIN; runs executed in parallel.
- Constant variables across all runs:
  - Ammonia source area: 15 m² (2D domain)
  - Distance between shed and trees: 20 m
  - Number of source particles: 80,000
  - Number of canopy particles: 800,000
  - Ammonia source density: 951 s m⁻³

## Data quality and validation
- Visual QA of input data; meteorological data mapped and QA/QC checked.
- LAI data reviewed by Forest Research experts.
- Input-file generation code reviewed; OpenFOAM and MODDAS are peer-reviewed models.
- OpenFOAM Segersson canopy physics incorporated for improved canopy interaction.

## Data structure and variable details
- Season: description and units (winter, spring, summer, autumn).
- LAD_BACK, LAD_MAIN: leaf area density (one-sided leaf area per unit layer volume).
- HEIGHT_MAIN, HEIGHT_BACK: canopy heights (m).
- DEPTH_MAIN, DEPTH_BACK: canopy depths along X axis (m).
- LAI_BACK, LAI_MAIN: leaf area index (dimensionless).
- TOTAL_RECAPTURE: overall percentage recapture for the chosen scenario (backstop + main canopy).
- MAIN_RECAPTURE: percentage recapture for the main canopy only.
- BACK_RECAPTURE: percentage recapture for the backstop canopy only.
- SDEN: source particle density (s m⁻³).
- LATITUDE_WGS84, LONGITUDE_WGS84: grid cell coordinates.
- SQ_NUMBER: GB grid cell ID (note: NI uses a single ID).
- YEAR: years since planting (5, 15, 25, 50).
- TIME: time of runs (3 am or 3 pm).

## References
- Forrester, D. I. & Tang, X. (2016). Ecological Modelling.
- Loubet et al. (2006). QJRMS.
- Robinson et al. (2020). CHESS-met dataset, NERC EIDC.
- Segersson (2017). Tutorial on urban wind flow with OpenFOAM.
- Bealey et al. et al. (2014). Env. Res. Lett. on agro-forestry ammonia abatement.