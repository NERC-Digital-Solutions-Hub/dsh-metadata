# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

## Overview
- Provides soil aggregate stability data from arable and grassland across Great Britain, collected in 2007 as part of Countryside Survey.
- Data capture includes two CSV files: Particle Size Distribution (PSD) data and derived aggregate stability metrics.
- Sample scope: 419 soils analyzed for aggregate stability from 1 km squares across GB (150 squares for these analyses; 424 plots selected, with 419 analysed).
- Sampling strategy aligns with Countryside Survey’s rigorous, stratified design to support national statistics and environmental interpretation.

## Data files and structure
- Particle_Size_Distribution_data.csv
  - 419 soils across 150 1 km squares; PSD measured for water-stable aggregates (pre-sonication) and post-sonication.
  - Key columns: SQUARE, PLOT, PSIZE, VOL_WS, VOL_SON.
- Aggregate_stability_metrics.csv
  - Derived metrics for water-stable vs post-sonication aggregates.
  - Key columns: SQUARE, PLOT, MWD1 (water-stable), MWD2 (post-sonication), DR (Disaggregation Reduction), LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
- DR measurement
  - DR 2000: no rescaling to 500 µm; DR 500 variant exists in other protocols but not in this dataset.
  - Protocol adjustments include increased aggregate mass and longer measurement time (leading to no rescaling in this dataset).
- Laboratory and measurement notes
  - Laser granulometer (Beckman LS 13320) used to derive PSD and Mean Weight Diameter (MWD).
  - 7 m-long pipe added to circulating system to increase sample mass and measurement precision; PSD measured for 60 seconds (instead of 30).
  - Post-sonication PSD obtained after applying a 100 W sonicator for five minutes.
  - Data include obscuration values and temperature readings to assess energy delivery and measurement quality.

## Sampling design and background
- Countryside Survey approach
  - GB stratified into Land Classes based on environmental gradients; sample squares (1 km × 1 km) randomly selected within classes.
  - 591 sample squares surveyed in 2007; 289 England, 107 Wales, 195 Scotland.
- Sample selection for aggregate stability
  - Sequential filters: Broad Habitat (Arable/Improved/Neutral Grass), previously sampled in 1998 and 2007, AVC categories (Crops and Weeds, Tall Grass and Herb, Fertile/Infertile Grassland), sufficient archived soil mass.
  - Result: 424 plots selected; 419 soils analysed for aggregate stability.
- Soil sampling and preparation
  - Archived 2007 soils (air-dried, 2 mm sieved) used; 15 g subsamples taken for analysis.
  - Sampling locations and plots chosen to enable national statistics and regional reporting (England, Scotland, Wales).

## Laboratory protocol (aggregate stability testing)
- Pre-wetting and mass determination
  - Determine approximate mass of aggregates (1–2 mm) per soil using pre-wet procedure to avoid optical obscuration issues.
  - Pre-wetting conducted on a two-filter-paper setup with 1 ml RO water, allowing 30 minutes capillary wetting.
- Measurement procedure
  - Initial PSD measured for 60 seconds after pre-wetting, using the laser granulometer to obtain PSD across 0.375–2000 µm.
  - Temperature recorded; 100 W UP100H sonicator applied for five minutes to fragment aggregates.
  - Post-sonication PSD measured for another 60 seconds.
  - Obscuration values >30% trigger a re-test with smaller initial aggregate mass.
- Calculation
  - MWD calculated from PSD; DR 2000 = MWD(post-sonication) subtracted from MWD(pre-sonication).
- Quality control
  - Palaeosol reference material used in each session.
  - Two standard PSD materials (32 µm and 500 µm) employed to verify instrument accuracy.
  - Re-testing with smaller sample masses if obscuration exceeded 30% after sonication.

## Quality assurance and governance
- UKCEH maintains ISO 9001:2015 certified Quality Management System; QA policy and procedures in place across sites.
- Data provenance and archiving
  - Soil samples and data are archived at the UKCEH Soil Archive (Lancaster).
  - Countryside Survey outputs are documented in related technical reports and published references.
- Data accessibility and use
  - Data are produced under Countryside Survey governance; use requires proper acknowledgment of UKCEH/Countryside Survey.
  - Several foundational references and methodological papers support transparency and reproducibility.

## Implications for monitoring frameworks
- The dataset provides standardized, nationally representative measures of soil aggregate stability, enabling monitoring of soil functional health across arable and grassland systems.
- Key metrics (MWD1, MWD2, DR 2000) allow assessment of soil structural resilience to wetting and mechanical disruption.
- Metadata and sampling design support cross-region comparisons (England, Scotland, Wales) and integration with broader environmental health indicators.
- Documentation of data collection, laboratory methods, QA, and data governance highlights practical considerations for data sharing, metadata completeness, and reproducibility in monitoring frameworks.

## References and acknowledgments
- Countryside Survey and related methodological references (careful documentation of land classification, sampling strategy, and soils manuals).
- Funding: NERC Soil Security Programme; acknowledgement requirements to Countryside Survey data.
- Acknowledgements emphasize data ownership by UK Centre for Ecology & Hydrology and the need to credit Countryside Survey in publications and presentations.