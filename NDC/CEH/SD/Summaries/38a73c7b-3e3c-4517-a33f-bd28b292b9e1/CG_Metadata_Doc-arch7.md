# Survey of British Calcareous Grasslands, 1990 and 2007

## Overview
- National survey of calcareous grasslands in Britain conducted across 1990 (128 plots) and 2007 (48 plots).
- Data focus on vegetation (vascular plants, bryophytes, macrolichens) and soils (pH, organic content, nutrients).
- Spatial scope: Great Britain; plots are nature reserves with standardized, relocatable 12x12 m plots.
- GIS-ready elements: explicit OS grid references, easting/northing coordinates, altitude, aspect, slope, coastal status, and site metadata.

## Data structure and files
- CG_SITES.csv
  - Site and plot metadata for each plot (unique PLOT_ID, PLOT, SITE, YEAR).
  - Spatial data: OSGR, EASTING, NORTHING.
  - Environment and habitat: NVC class, ALT, ASPECT, SLOPE, COASTAL, SCREE, PH_LE_6, NOTES, SOIL_TYPE.
  - Soil measures: AMMONIUM, NITRATE, AVE_SOIL_DEPTH, ORG (organic content), plus pH measures and related soil properties.
- CG_VEG.csv
  - Vegetation species data per plot-year.
  - Fields: PLOT_ID, YEAR, SPECIES_REC, BRC_NUM/BRC_NAME, COUNT, GROWTH.
  - 36 quadrats per plot (0.5x0.5 m each) used to derive presence/absence and frequency across quadrats.
- Notes on data
  - 999 indicates no data.
  - 1990 dataset includes bryophytes and lichens; 2007 dataset does not.

## Sampling design and methods
- Plot design
  - 12x12 m plots subdivided into four 6x6 m blocks, each into nine 2x2 m units.
  - 36 quadrats per plot, each 0.5x0.5 m, located using a stratified systematic unaligned pattern.
  - Grid position marked with seven buried copper marker loops for relocation (approx. 5–15 cm depth; relocation accuracy ~5 cm).
- Vegetation recording
  - Recording categories: grasses (V/F), other herbs, and lower plants (bryophytes/lichens in 1990; not in 2007).
  - Percent cover not generally estimated; presence/absence frequency used to calculate constancy and compare with NVC profiles.
  - VESPAN II and related tools used for data handling and analysis.
- Soil sampling
  - 1990: field pH measurement on top 10 cm soil (slurry method).
  - 2007: composite soil sample from top 10 cm; analysis includes pH (water and extracts), Olsen-P, NO3−/NH4+, base cations (Ca, Na, Mg, K), Al3+, organic content (loss on ignition).
  - Data capture includes soil depth, soil type, and other site-level soil properties.
- Data limitations and notes
  - Some plots lost or data not recoverable (data for seven plots in 1990).
  - 1990 and 2007 data are not perfectly directly comparable for all taxa due to methodological differences (e.g., bryophytes/lichens inclusion).

## GIS considerations and potential uses
- Spatial layers
  - Point layer of plots using OS grid coordinates (OSGR, Easting, Northing); ready for projection to lon/lat or other CRS.
  - Attribute-rich point data with site-level (CG_SITES) and plot-level vegetation/soil (CG_VEG) attributes.
- Thematic mapping opportunities
  - Soil chemistry and base cations by plot-year (pH, Olsen-P, NO3−/NH4+, organic content).
  - Vegetation constancy and dominant taxa by plot-year; crosswalk to National Vegetation Classification (NVC).
  - Topographic context: altitude, aspect, slope, proximity to coastal features.
  - Change detection: compare 1990 vs 2007 data to explore shifts in vegetation and soil parameters.
- Data integration
  - Link species data (CG_VEG) with external plant trait datasets (e.g., PLANTATT, BRYOATT) via BRC_NUM/BRC_NAME for enhanced habitat modelling.
  - Combine with climate and deposition datasets to assess drivers of change in calcareous grasslands.

## Provenance and references
- Origin and management
  - 1990: DoE Contract; T.C.G. Rich, E.A. Cooper, J.S. Rodwell, A.J.C. Malloch.
  - 2007: NERC Grant; L.J.L. van Den Berg, P. Vergeer, T.C.G. Rich, S.M. Smart, D. Guest, M.R. Ashmore.
- Publication and data access
  - Rich et al. (2015). Survey of British calcareous grasslands, 1990 and 2007. NERC Environmental Information Data Centre. DOI: 10.5285/38a73c7b-3e3c-4517-a33f-bd28b292b9e1.
- Tools and methodological references
  - Malloch (1988, 1990) on VESPAN II and MATCH; 1993 study on climate and deposition effects.

## Usage notes for GIS Specialists
- Prepare a point shapefile with CG_SITES data and a related CG_VEG dataset joined by PLOT_ID and YEAR for year-specific analyses.
- Convert OS grid coordinates to a geographic CRS as needed; preserve all spatial attributes (EASTING/NORTHING/OSGR, ALT, ASPECT, SLOPE).
- Be mindful of year-specific data availability and taxonomy changes when performing temporal analyses.
- Consider creating derived rasters or polygons for continuous surfaces (e.g., soil pH, organic content) by spatial interpolation, while documenting the sampling design and potential biases.