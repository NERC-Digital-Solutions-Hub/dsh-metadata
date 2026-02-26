# Trees have the potential to recapture ammonia emissions from animal housing units or areas where animals are able to roam free range under the canopy, with associated benefits for animal welfare and the environment.

## Overview
- Dataset provides model outputs for scenarios where tree shelterbelts downwind of an ammonia source recapture ammonia, potentially reducing environmental and social impacts.
- Focuses on Great Britain with a grid-based approach to evaluate spatial variation in recapture and dispersion.
- Combines canopy physics, dispersion/deposition modelling, and seasonal meteorology to quantify ammonia recapture.

## Dataset coverage and scope
- Spatial coverage: Great Britain in a 100x100 km grid (10,000 km² per grid cell); Northern Ireland represented by a single 10,000 km² area.
- Scenarios vary tree canopy depths and heights while keeping source area and distance to trees constant.
- Outputs include recapture percentages for main canopy, backstop canopy, and combined canopy.

## Meteorological and input data
- Meteorology: CHESS-met dataset (GB, 1961–2017) aggregated to 100 km x 100 km resolution; 10-year representative year (2008–2017) used with four days representing each season.
- Derived inputs: PAR from CHESS incoming shortwave radiation; RH, air temperature, and wind speed from CHESS; Northern Ireland weather approximated from the nearest GB grid square on the west coast of Scotland.
- Tree heights vary by grid square using Forest Research Decision Support tools; Northern Ireland heights derived from similar tools (not public).
- Seasonal variation in Leaf Area Index (LAI) applied for main canopy across ages (0, 5, 15, 25, 50 years) and seasons; backstop canopy LAI fixed with seasonal variation not applied.

## Treebelt design and canopy properties
- Shelterbelt structure: main canopy (2–4 m spacing, open to plume entry) in front of shelter belt; backstop canopy (2 m or less spacing, evergreen/conifer) to form a thick barrier.
- Backstop canopy uses Sika spruce; main canopy comprises mixed broadleaf/conifer plantings.
- LAI values provided as functions of height, spacing, age, and season (main canopy) and constant for backstop canopy.

## Modelling framework
- MODDAS-2D v2.7.1: two-dimensional Lagrangian stochastic dispersion model to calculate ammonia recapture.
- OpenFOAM v1706: turbulence model used to provide canopy-physics inputs; Segersson modifications applied.
- Coupling: OpenFOAM and MODDAS linked via a Python (2.7) coupler.
- Computation performed on a high-performance LOTUS cluster on the JASMIN platform, running in parallel.

## Constant variables across runs
- Ammonia source area: 15 m² (2D domain).
- Distance from source to trees: 20 m.
- Particles: 80,000 from source; 800,000 within canopy.
- Ammonia source density: 951 particles per m³ per second.

## Outputs and data fields
- Outputs: percentage recapture for the chosen scenario, including total, main canopy, and backstop canopy.
- Data structure fields include:
  - SEASON (winter, spring, summer, autumn)
  - LAD_BACK and LAD_MAIN (leaf area density one-sided per unit volume)
  - HEIGHT_MAIN, HEIGHT_BACK (canopy heights)
  - DEPTH_MAIN, DEPTH_BACK (canopy depths along X axis)
  - LAI_BACK, LAI_MAIN (leaf area index)
  - TOTAL_RECAPTURE, MAIN_RECAPTURE, BACK_RECAPTURE (percent recapture)
  - SDEN (source particle density)
  - LATITUDE_WGS84, LONGITUDE_WGS84 (coordinates)
  - SQ_NUMBER (grid square ID for GB; not for Northern Ireland)
  - YEAR (tree age in years: 5, 15, 25, 50)
  - TIME (3am or 3pm)
- A schematic figure describes the shelterbelt configuration and the recapture mechanism (entry of plume into main canopy and barrier effect of backstop).

## Data quality and quality control
- Visual QA of input data; QA plots/maps of meteorological data.
- LAI data reviewed by Forest Research experts.
- Input-file generation code reviewed by experts.
- Models (MODDAS-2D, OpenFOAM) are peer-reviewed; OpenFOAM has a broad support community.

## Data use, integration, and accessibility considerations
- Data intended to support environmental monitoring and policy evaluation by assessing ammonia recapture potential of tree shelterbelts.
- Part of a broader effort to increase dataset value by combining with other relevant data and facilitating access to underlying data used to produce outputs.
- Described data structure and metadata to enable reuse and integration with other environmental datasets.

## References
- Forrester, D. I. & Tang, X. (2016). Analysing spatial/temporal dynamics in mixed-species forests using the 3-PG model.
- Loubet et al. (2006). A coupled dispersion and exchange model for short-range dry deposition of atmospheric ammonia.
- Robinson et al. (2020). CHESS meteorology data for GB (CHESS-met).
- Segersson (2017). Tutorial on urban wind flow using OpenFOAM.
- Bealey et al. et al. (2014). Modelling agro-forestry scenarios for ammonia abatement.