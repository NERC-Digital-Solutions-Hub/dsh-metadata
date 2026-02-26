# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2

## Overview
- A GIS-ready dataset estimating annual average percentage yield loss due to ozone for maize, rice, soybean, and wheat for 2010–2012.
- Outputs are four 1° by 1° grid-based shapefiles (one per crop) with yield-loss estimates suitable for map-based analysis and visualization.

## Data and grid construction
- Grid system: 1° by 1° cells; crop production data from FAO Global Agro-Ecological Zones (GAEZ) at 0.0833° resolution (year 2000) aggregated to 1° cells.
- Production filtering: Only grid cells with more than 500 tonnes total crop production are included in mapping.
- Irrigation classification: Cells labeled irrigated if more than 75% of crop production is irrigated; otherwise non-irrigated.
- Geospatial attributes: Each cell assigned to a hemisphere (Northern/Southern) and a climate zone using the ESDAC GIS climate zone layer (JRC).

## Growing periods and climate context
- For each hemisphere-climate zone combination, a 90-day growing period is defined per crop, based on main growing seasons (data from USDA and FAO).
- Climate-zone/hemisphere specifics are detailed in Mills et al. 2018a (Table S1) and applied to maize, rice, soybean, and wheat.

## Crop-specific processing methodology
- Wheat:
  - Ozone exposure modeled with EMEP MSC-W chemical transport model (v4.16) to produce POD3IAM (phytotoxic ozone dose above 3 nmol m-2 s-1).
  - Accumulated 90-day POD3IAM per grid cell; subtract a reference POD3IAM of 0.1 mmol/m2 before yield-loss calculation.
  - Yield loss: Percent Yield Loss = (POD3IAM - 0.1) × 0.64.
- Maize, rice, soybean:
  - No crop-specific ozone flux-response data available; apply wheat-based yield loss and adjust using relative ozone sensitivity.
  - Relative sensitivity for each crop is the ratio of its M7 (7-hour mean ozone) response slope to that of wheat.
  - Final yield loss per grid cell = wheat-yield-loss × relative sensitivity.

## Data outputs and fields
- Four GIS shapefiles (maize, rice, soybean, wheat) at 1° grid resolution.
- Attribute fields per cell:
  - ID: Unique grid cell identifier
  - Zone: Climate zone
  - Long_Lat: Center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South (for Cool temperate)
  - Yloss: Annual average percentage yield loss (2010–2012)

## Quality control and validation
- EMEP model validation (Mills et al. 2018b): comparison with Global Atmosphere Watch (GAW) network data shows good spatial/temporal performance; r² for Dmax and M7 between 0.88 and 0.93.
- Stomatal uptake proxy validation: strong correlation (r² = 0.63) between AET/PET and POD3IAM/M7 proxy, supporting model plausibility.
- Key caveats:
  - Flux-response data are lacking for maize, rice, and soybean; all rely on wheat flux as a basis.
  - Potential climate- and season-specific variability not fully captured where multiple growing seasons exist (only the primary season used per climate).
  - Maize data carry higher uncertainty due to limited cultivar data (only three older varieties).

## Data sources and references
- EMEP MSC-W chemical transport model (v4.16) inputs and methodology.
- CLRTAP modeling and validation references; supplementary information and Figures from Mills et al. 2018a, 2018b.
- Crop production data from FAO GAEZ dataset; climate zone layer from ESDAC/JRC.
- Related methodological details and validation figures available in the cited papers and supplementary materials.

## Usage considerations for GIS specialists
- Suitable for overlay with other spatial datasets to assess ozone-related agricultural risk.
- Be mindful of crop-specific uncertainties, especially for maize, rice, and soybean.
- The 1° resolution enables broad-scale analyses and visualization across regions; consider higher-resolution local analyses if data become available.