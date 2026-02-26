# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Modelled topsoil pH (0–15 cm) across Great Britain at 1 km2 resolution using Countryside Survey (CS) data from 2007.
- Represents soil acidity to inform understanding of soil biodiversity, nutrient availability, plant growth and species distributions.
- Dataset built to provide comprehensive, model-based estimates with metadata and data provenance described in supporting literature.

## Modelling approach
- Generalized Additive Mixed Model (GAMM) with a random factor to account for nesting of samples within 1 km2 survey squares.
- Non-linear smooth terms for climate and atmospheric deposition; two-dimensional tensor product smooths for latitude/longitude to capture large-scale spatial variation.
- Tweedie distribution (variance power ≈ 1.01) used instead of Gaussian; implemented via gamm in the R mgcv package.
- Based on 2446 measurement locations; full methodological details available in Thomas et al. (2020).

## Variables and data structure
- Model inputs include:
  - Climate: 5-year mean winter, spring, summer, autumn temperatures (units: °C; 5 km spatial resolution; 2003–2007).
  - Climate: 5-year mean winter, spring, summer, autumn precipitation (units: mm; 5 km; 2003–2007).
  - Atmosphere: 3-year mean NO3, NH4, and SO4 deposition (units: kg ha−1 yr−1; 5 km; 2005–CBED data).
  - Spatial terms: Easting/Northing coordinates (OSGB 1936), and tensor product interactions.
  - Broad Habitat, CACO3 Rank, Soil Group (with respective 1 km or qualitative/soil-model inputs and 2007 land cover data).
- Table-like presentation of variables used (s = smoothed term; te = tensor product term) detailing sources and temporal/spatial contextualization.

## Data attributes and format
- Dataset: CS_topsoil_ph_gam.nc
- Primary variable: Soil_pH — mean pH value for 2007 modeled via GAM.
- VAR: standard error divided by predicted mean (uncertainty measure).
- Spatial references: x (Easting), y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); transverse_mercator for mapping.
- Coordinate system and units: metres; consistent with GB mapping standards.
- Depth: topsoil defined as 0–15 cm.

## Sampling and quality control
- Sampling and analytical methods described in CS Soil Manuals:
  - Sampling using a 15 cm long by 5 cm diameter core.
  - Soil used: 10 g with 25 ml deionised water (soil-to-water ratio 1:2.5 by weight).
  - Protocols followed Defra/NERC Joint Codes of Practice.
- Original field data published in Reynolds et al. (2013); methodological details in Emmett et al. (2008, 2010).

## Data governance and accessibility
- Full methodological transparency via CS technical reports and associated literature.
- Data provenance includes model fitting details and data sources; guidance for metadata is embedded in the data attributes.
- Public sharing of underlying data is a general considerations area for monitoring frameworks (noting potential barriers such as metadata sufficiency and data access).

## Implications for monitoring frameworks
- Provides spatially comprehensive soil pH estimates enabling policy scrutiny where direct measurements are sparse.
- The GAMM framework supports integration of climate change and deposition trends into soil health indicators.
- Model-based outputs facilitate trend analyses and scenario evaluations for soil management and environmental policy.
- Highlights the importance of robust metadata, data sharing practices, and governance to ensure data quality, reproducibility, and usefulness across organisations.