# AFEX Experiment

## Overview
- Location: AFEX project area, BDFFP/INPA, ~80 km north of Manaus, Amazonas, Brazil (02°25'S, 59°43'W)
- Climate context: mean air temperature ~26°C; mean annual precipitation ~2,400 mm; relative humidity 75–92% during rainy season
- Study aim: a full factorial nutrient addition experiment to assess how nutrient inputs affect root dynamics and nutrient status

## Experimental Design and Data Scope
- Treatments: eight nutrient treatments (8 total)
  - Control (untreated)
  - N only
  - P only
  - Cations (K, Mg, Ca)
  - N + P
  - N + Cations
  - N + P + Cations
- Plot arrangement: 32 plots across 4 independent blocks (n=4 per block), with at least 250 m between blocks
- Plot size: 50 m x 50 m; central measurement area 30 m x 30 m
- Replication: four replicates per treatment
- Nutrient application rates (dry granules, surface application, three times per year):
  - N: 125 kg ha^-1 year^-1 (as urea)
  - P: 50 kg ha^-1 year^-1 (as triple superphosphate)
  - Ca: 50 kg ha^-1 year^-1
  - Mg: 20 kg ha^-1 year^-1 (as dolomitic limestone)
  - K: 50 kg ha^-1 year^-1
- Data collection window: focused on response in plots over time with central plot area as the measurement zone

## Root Sampling and Morphology
- Root sampling design: five ingrowth cores per plot (n=32 plots)
  - Core specifics: 12 cm diameter, 30 cm depth, root-free, installed August 2017
  - Collection interval: every three months
  - Within-plot aggregation: cores homogenized by plot and soil depth (0–10 cm; 10–30 cm)
- Measurements:
  - Fine roots (<2 mm diameter) extracted and dried (60°C) to determine dry root mass
  - After one year (Nov 2017–Aug 2018), root samples from all cores pooled per plot and depth for nutrient analysis
- Subsampling for traits: fine roots from both depths used to determine morphological traits, then dried for dry mass

## Chemical Analysis and Nutrient Metrics
- Nutrient analysis on <2 mm root material, pooled by plot and depth (0–10 cm; 10–30 cm) across four time intervals (Nov 2017–Aug 2018)
- Analytical methods:
  - Micronutrients, phosphorus, and cations via nitroperchloric digestion (Malavolta et al. 1989)
  - Mcation concentrations (K, Ca, Mg) and micronutrients via atomic absorption spectrophotometry
  - Total phosphorus via colorimetry and spectrophotometry
  - Carbon and nitrogen contents via CN analyzer
- Species-level identification: not performed; reported as mean values for the plant community within each plot

## Data Structure and Metadata
- Spreadsheet fields (sample schema):
  - Block (1–4)
  - Plot (1–8 within each block)
  - TRT (treatment description: control, N, P, cations, N+P, N+cations, N+P+cations)
  - Depth (0–10 cm; 10–30 cm)
  - Fe, Zn, Mn, Ca, Mg, K, P (root concentrations)
  - N (%), C (%)
- Data provenance considerations:
  - Centralized data by plot and depth; repeated measures over time
  - Methods and units aligned to established soil/root analysis protocols
- Study references for methods:
  - Anderson & Ingram (1993)
  - Araújo (2002)
  - Malavolta et al. (1989)
  - Metcalfe et al. (2007)

## Temporal and Spatial Considerations
- Timeframe: nutrient addition implemented in 2017 with sampling extending through August 2018
- Spatial scope: 32 plots across 4 blocks; measurements focused on central 30 m x 30 m area per plot to standardize assessments
- Temporal granularity: quarterly root sampling for the first year to capture growth and nutrient response dynamics

## Data Use and Implications for Data Leaders
- Data assets include a comprehensive, multi-depth, time-series dataset linking nutrient treatments to root biomass and root elemental composition for a community-level plant stock
- Strengths:
  - Robust factorial design with replication and block structure
  - Detailed metadata on treatments, depths, and measurement intervals
  - Established and documented laboratory protocols for reproducibility
- Considerations and potential limitations:
  - No species-level identification; results reflect community averages
  - Data are localized to a specific forest fragment system; cross-study harmonization may require careful alignment of methods
  - Temporal window covers one year post-treatment; longer-term dynamics may require continued sampling
- Opportunities for data strategy:
  - Integrate with other BDFFP soil-plant datasets to build broader nutrient-cynamics models
  - Use standardized metadata to facilitate data sharing and re-use within the wider data community studying tropical forest nutrient dynamics