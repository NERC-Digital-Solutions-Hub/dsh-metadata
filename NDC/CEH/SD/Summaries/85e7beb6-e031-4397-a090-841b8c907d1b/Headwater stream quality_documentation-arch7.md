# Headwater stream quality (Countryside Survey)

## Overview
- Purpose: create a GIS-compatible data product that indicates headwater stream quality across sampled areas, enabling mapping and exploration of water quality indicators.
- Study scope: 478 headwater stream sites surveyed in 1998 and 2007, downstream of sources marked on 1:50,000 maps; sites suitable for RIVPACS.
- Data product: a 1 km raster where each cell represents water quality as Observed BWMP divided by Expected BWMP.
- Modelling approach: Boosted Regression Tree used to relate observed stream quality to catchment/stream characteristics; extrapolated to unmonitored 1 km grid squares containing headwater streams.
- Output constraints: only Strahler order 1–3 headwater streams included.

## Experimental Design, Sampling Regime and Data Collected
- Macroinvertebrate sampling: standard protocols (3 minutes active sampling plus 1 minute hand search) over a 5–15 m stream length; collected with a pond net and returned to CEH for processing.
- Supplemental measurements: stream width, depth, substrate; BMWP scores calculated (biological quality index based on macroinvertebrates).
- RIVPACS used to estimate expected macroinvertebrate communities from physical characteristics.
- Two-year pooled data (1998 and 2007) used to model relationships between headwater stream quality and catchment/stream characteristics.

## Data Product and Modelling Details
- Output data product: a 1 km raster with a single attribute “Value” = Observed BWMP / Expected BWMP.
- Observed BWMP modelling: using Boosted Regression Tree; training/testing split; extrapolation to national scale for 1 km squares with headwater streams.
- Expected BWMP calculation: derived from RIVPACS scores for sampling sites averaged by land class (Bunce et al. 2007) for each unmonitored grid square.
- Model predictors (per 1 km square): 
  - % Arable
  - % Improved Grassland
  - % Urban
  - % Woody cover along the stream
  - Slope over a 1 km length (from 500 m upstream to 500 m downstream)
  - Altitude
  - Strahler stream order (1, 2 or 3)
  - Easting and Northing
  - Survey year
- Data scope: includes only squares containing Strahler order 1–3 headwater streams.

## Spatial Reference and Data Attributes
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)
- Data attribute: Value – Observed BWMP divided by Expected BWMP

## Collection Methods, Processing and Quality Control
- Collection: same sampling approach as above using standard netting protocol and field measurements.
- Laboratory processing: taxonomic identification harmonised to a common modern taxonomy; standardisation to derive a mutually exclusive taxa list for calculating species richness.
- Quality control: followed Defra/NERC Joint Codes of Practice; detailed QA and methods described in Dunbar et al. (2008, 2010) and Murphy & Weatherby (2008).

## References / Supporting Documents
- Armitage et al. 1983; Bunce et al. 2007; Dunbar et al. 2010; Morton et al. 2011; Murphy et al. 2008; Norton et al. 2016.