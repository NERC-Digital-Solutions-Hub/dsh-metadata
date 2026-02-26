# Headwater stream quality (Countryside Survey)

## Overview
- Objective: model relationships between headwater stream quality and catchment/stream characteristics to inform predictions of water quality at broader scales.
- Data scope: 478 headwater stream sites sampled in two survey years (1998 and 2007); sites downstream of marked sources on 1:50,000 maps.
- Output: a national-scale 1 km raster representing water quality, via observed vs. expected BMWP-derived scores.
- Core indicators: BMWP score (macroinvertebrate-based biological quality) and RIVPACS-predicted reference communities.

## Experimental Design / Sampling Regime
- Sampling protocol: standard Freshwater Biological Association method; one 5–15 m stream segment per site plus a 1-minute hand search (total active sampling ~3 minutes).
- Habitat and site data: supplemental measurements of width, depth, substrate recorded for RIVPACS.
- Biological indicators: BMWP score calculated from macroinvertebrate taxa; RIVPACS used to generate expected reference scores based on site characteristics.
- Field processing: macroinvertebrate samples processed to record taxa, BMWP taxa, and RIVPACS status; taxonomy harmonised to modern standards.

## Data and Variables
- Observed vs. expected: BMWP-derived Observed BWMP vs. Expected BWMP scores; the dataset stores the ratio (Observed BWMP / Expected BWMP).
- Model inputs (per 1 km square and sampling site): 
  - % Arable
  - % Improved Grassland
  - % Urban
  - % woody cover along the stream within 1 km
  - Slope (1 km length around the site, 500 m upstream to 500 m downstream)
  - Altitude of sampling site
  - Strahler stream order (1, 2, or 3)
  - Easting and Northing
  - Survey year
- Data scope for modelling: only Strahler orders 1–3 headwater streams included.

## Modelling Approach
- Method: Boosted Regression Tree (BRT) model to estimate water quality indicators.
- Training and validation: model trained on a subset of data and validated on the remainder; results extrapolated to unmonitored 1 km grid squares containing headwater streams.
- Spatial output: data presented as a 1 km raster with the water quality measure for each headwater location.

## Spatial Reference and Data Attributes
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Primary data attribute: Value = Observed BWMP score divided by Expected BWMP score (O/E BWMP).

## Data Collection Methods and Processing
- Field sampling: as described, using a standardized pond net method and a fixed sampling duration.
- Supplemental measurements: width, depth, substrate for RIVPACS integration.
- Analytical processing: lab processing of macroinvertebrate data to derive taxa counts, BMWP taxa, and RIVPACS status; taxonomy harmonisation to current standards; standardisation to produce a mutually exclusive taxa list for species richness.

## Quality Control
- Compliance: Defra/NERC Joint Codes of Practice followed.
- Documentation: detailed QA and methodology references (Murphy & Weatherby, 2008; Murphy et al., 2008; Dunbar et al., 2018; and related Countryside Survey reports).
- Cross-referencing: model context and validation discussed in related literature (Dunbar et al. 2010; Norton et al. 2016; Bunce et al. 2007; Armitage et al. 1983).

## Outputs and Limitations
- Outputs: nationwide 1 km raster maps of headwater stream quality, based on O/E BWMP.
- Scope limitation: areas without Strahler order 1–3 headwater streams are not included in the model outputs.
- Scale considerations: the approach emphasizes scale effects, relying on land cover, topography, and location coordinates to predict headwater quality.

## References / Supporting Documents
- Foundational BMWP and bioassessment methods (Armitage et al. 1983).
- Land classification and land cover data (Bunce et al. 2007; Morton et al. 2011).
- Countryside Survey headwater streams (Dunbar et al. 2010; Murphy & Weatherby 2008; Murphy et al. 2008).
- Methodological context for scale and indicators (Norton et al. 2016; additional CS reports).