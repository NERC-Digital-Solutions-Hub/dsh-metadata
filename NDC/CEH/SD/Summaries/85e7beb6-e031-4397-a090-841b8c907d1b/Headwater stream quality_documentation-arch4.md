# Headwater stream quality (Countryside Survey)

## Overview
- Investigates headwater stream quality using standard CS macroinvertebrate protocols across two survey years (1998 and 2007).
- 478 headwater stream sites surveyed in both years, located downstream of sources on 1:50,000 maps; focused on headwater streams (Strahler order 1–3).
- Sampling area per site: 5–15 m of stream, with ~3 minutes of active sampling plus 1 minute hand search; samples collected with a standard pond net and later sorted/identified at CEH.
- Supplemental measurements captured: width, depth, substrate; used to run RIVPACS.

## Data products and modelling
- BMWP score (1–10) calculated per site as a measure of biological quality; BMWP taxa and metrics processed in the lab.
- RIVPACS used to generate an expected (reference) BMWP score based on site physical characteristics.
- Observed BWMP score (from sampling) and Expected BWMP score used to derive a headwater stream quality measure: observed/expected BMWP ratio.
- Data pooled across 1998 and 2007 to model relationships between headwater quality and catchment/stream characteristics.
- A Boosted Regression Tree (BRT) model was employed to predict quality at national scale, extrapolating to 1 km squares containing headwater streams; sites lacking Strahler order 1–3 were excluded.
- Output presented as a 1 km raster where each square represents the headwater stream quality and location.

## Data attributes and variables
- Primary attribute: Value = Observed BMWP score divided by the Expected BMWP score.
- Model parameters considered at 1 km square scale:
  - % Arable
  - % Improved Grassland
  - % Urban
  - % Woody cover along the stream
  - Slope (within ±500 m of site)
  - Altitude of sampling site
  - Strahler stream order (1, 2, or 3)
  - Easting and Northing
  - Survey year
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Data collection, processing, and standardization
- Field collection followed the Freshwater Biological Association pattern, with standardized protocols for sampling and recording site characteristics.
- Laboratory processing included recording species numbers, BMWP Taxa (TAXA), and RIVPACS status; taxonomy harmonised to a common modern standard to control for taxonomy changes.
- A separate standardisation exercise defined a mutually exclusive list of taxa for calculating species richness.

## Quality control and governance
- QA/QC adhered to Defra/NERC Joint Codes of Practice; detailed QA documentation referenced (Murphy & Weatherby 2008; Murphy et al. 2008, 2010; Dunbar et al. 2010).
- Calibration and methods detailed in accompanying technical reports and related literature.
- Data scope restricted to Strahler order 1–3 headwater streams; areas without suitable headwater streams not included in models.

## Data provenance and references
- References include foundational BMWP methodology (Armitage et al., 1983), land classification inputs (Bunce et al., 2007), headwater streams report (Dunbar et al., 2010), land cover mapping (Morton et al., 2011), QA reports (Murphy et al., 2008; Murphy & Weatherby, 2008), and methodological papers on scale and ecosystem indicators (Norton et al., 2016).