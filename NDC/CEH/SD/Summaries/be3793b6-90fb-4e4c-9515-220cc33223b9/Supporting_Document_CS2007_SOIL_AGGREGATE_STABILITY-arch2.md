# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

## Overview
- Data from Countryside Survey 2007 in Great Britain, focusing on soil aggregate stability measured by laser granulometry.
- Two CSV data products: particle size distribution (PSD) data and derived aggregate stability metrics.
- Sampling across 1 km squares and plots to support national statistics and environmental monitoring.

## Data Files and Key Variables
- Particle_Size_Distribution_data.csv
  - Covers water-stable aggregates (pre-sonication) and post-sonication aggregates.
  - 419 soils sampled across 150 1 km squares (GB) in 2007.
  - Columns: SQUARE (1 km grid code), PLOT (plot within square), PSIZE (particle size class), VOL_WS (PSD for water-stable aggregates), VOL_SON (PSD after sonication).

- Aggregate_stability_metrics.csv
  - Derived metrics from the same 419 soils.
  - Columns include: MWD1 (Mean Weight Diameter, water-stable), MWD2 (Mean Weight Diameter, post-sonication), DR (Disaggregation Reduction), LC07 and LC07_NUM (Land Class 2007), COUNTRY, COUNTY07, EZ_DESC_07, plus related identifiers.

## Sampling and Study Design
- Part of Countryside Survey 2007 with stratification by Land Classes to ensure national representativeness.
- 591 sample squares surveyed nationwide; selection yielded 424 plots, with 419 analyzed for aggregate stability.
- Sampling locations span England, Scotland, and Wales; distribution designed to support reliable GB and country-level statistics.
- Soil samples were sourced from archived 2007 material, prepared (air-dried, 2 mm sieved) and homogenised before analysis.

## Laboratory and Measurement Method
- Technique: Laser granulometry to obtain Particle Size Distribution (PSD) and calculate Mean Weight Diameter (MWD).
- Aggregate stability metric DR = MWD after pre-wetting of the 1–2 mm fraction (water-stable aggregates) minus MWD after a sonication step (fundamental particles).
- Protocol specifics for this dataset:
  - Larger aggregate mass used (1.8× previous protocol) and PSD measured for 60 seconds (instead of 30 seconds previously).
  - No rescaling to <500 µm in this dataset; DR values reported as DR 2000 (no rescaling). Earlier rescaled method is referred to as DR 500 (not in this dataset).
  - Instrument and setup: laser granulometer with 92 size classes from 0.375 µm to 2000 µm; pump speed fixed to 60 (about 45 ml/s) to avoid biased settling.
  - Material masses used for analysis by texture: 0.55 g (fine), 1.0 g (medium), 1.3 g (coarse).
  - Protocol adjustments included increasing circulating water volume (via a 7 m pipe) and extending measurement time to improve representation of larger aggregates.
- Pre-wetting and measurement steps:
  - Specific pre-wetting procedure to prepare 1–2 mm aggregates on a dual-filter setup.
  - 30 seconds wait before PSD measurement to allow initial fragmentation, followed by 60 seconds of PSD analysis.
  - Post-sonication PSD measured again for 60 seconds; temperature monitoring used to estimate energy input.
  - Quality checks included obscuration limits (<30%) and re-analysis with adjusted mass if limits were exceeded.

## Quality Control and Assurance
- Field and laboratory staff trained with a dedicated manual; standardized processing from logging to archiving.
- Use of a palaeosol reference material (Ospringe) and standard beads (32 µm and 500 µm) to ensure accuracy and precision.
- Repeated PSD measurements when obscuration exceeded limits; QA documented under UKCEH Quality Management System (ISO 9001:2015 certified).

## Context, Data Management, and Access
- Countryside Survey sampling based on Land Class and AVC (Agricultural/Vegetation context) classifications to ensure environmental representativeness.
- Data held by UK Centre for Ecology & Hydrology (UKCEH); data use requires acknowledgment.
- Related technical and methodological references are provided, including Countryside Survey reports and method papers.

## Implications for Environmental Monitoring
- Enables standardized, cross-country assessment of soil aggregate stability and its response to disturbance, supporting policy performance evaluation and soil health monitoring over time.
- The standardized data products (PSD and derived DR/MWD metrics) support integration with other environmental datasets and broader analyses of soil stability under varying land uses.

## Acknowledgements
- Funded by the NERC Soil Security Programme (Project NE/P014364/1).
- Data usage and publication require acknowledgement of Countryside Survey data ownership and rights.