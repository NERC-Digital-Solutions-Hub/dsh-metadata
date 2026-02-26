# Supporting information for: Hydraulic properties of peat extracted from 20 locations at Rensjön palsa mire, Sweden in July 2022

## What this dataset contains
- Laboratory measurements of peat depth, horizontal saturated hydraulic conductivity (Kh), dry bulk density, and the degree of peat humification (von Post scale) for degrading palsas at Rensjön palsa mire, Norrbotten, Sweden.
- Study supported by Natural Environment Research Council Grant NE/S007458/1.

## Study site and collection methods
- Location: Rensjön palsa mire, Norrbotten, Sweden (68.0868°N, 19.8314°E).
- Sampling period: July 2022.
- Sampling approach: Peat cores collected from 20 locations on degrading palsas using PVC downpipes.
- Transport: Cores moved to University of Leeds, UK laboratory for analysis.
- Subsampling: 82 total subsamples analyzed for hydraulic properties.
- Measurements:
  - Kh: determined via split-cylinder permeameter method.
  - Dry bulk density: measured on adjacent peat core offcuts (standard method).
  - Von Post peat humification: measured on adjacent peat core offcuts (Von Post classification).

## Quality control
- All measurements conducted by the authors.
- Instrument checks performed; outliers removed (e.g., anomalously high Kh values).
- Repeated measurements conducted when necessary.

## Data structure and units
- File: single comma-separated values (CSV) file named fewster_2023_wrr_data.csv.
- Columns (seven total):
  - FID: Field ID (subsample identifier); Units: NA.
  - Subsample_ID: Subsample code used during laboratory analyses; Units: NA.
  - Kh_m_s: Horizontal saturated hydraulic conductivity; Units: m s^-1.
  - Depth_midpoint_m: Sample midpoint depth; Units: m.
  - Von_Post_score: Degree of peat humification; Units: H-score.
  - Dry_bulk_density_g_cm3: Dry bulk density; Units: g cm^-3.
  - Degradation_stage: Stage of palsa degradation (desiccating or collapsed); Units: NA.

## Variable details and interpretation
- Kh_m_s: Lab measurements of Kh from split-cylinder permeameter.
- Depth_midpoint_m: Midpoint depth of each peat sample.
- Von_Post_score: Humification level of peat using von Post scale.
- Dry_bulk_density_g_cm3: Dry bulk density from adjacent offcuts.
- Degradation_stage: Field-observed degradation status of the palsa.

## References (methods used)
- Chambers, F.M., Beilman, D.W. and Yu, Z. (2011). Methods for determining peat humification and for quantifying peat bulk density, organic matter and carbon content for palaeostudies of climate and peatland carbon dynamics. Mires and Peat, 7(7), 1-10.
- Ekono, I. (1981). Report on energy use of peat. In Contribution to UN Conference on New and Renewable Sources of Energy, Nairobi, Kenya.

## Relevance to monitoring frameworks
- Standardized measurement methods (split-cylinder permeameter, established von Post scale) support consistent environmental health monitoring.
- Clear metadata and unit definitions facilitate data integration, comparison, and trend analysis across monitoring programs.
- Quality control practices (instrument checks, outlier removal, replication) illustrate governance steps to ensure data reliability.
- Data sharing considerations implied by explicit data structure and open references; potential data governance barriers noted in monitoring frameworks (e.g., metadata completeness, access, and transparency).

## Data quality and governance considerations for monitoring
- Strengths:
  - Well-documented methodology and measurement techniques.
  - Explicit data structure with clear variable definitions and units.
  - QA steps outlined (outlier handling, re-measurement).
- Potential barriers:
  - Data accessibility and broader sharing practices are not fully described beyond file naming.
  - Metadata scope is explicit for variables but broader dataset documentation (e.g., sensor calibration details, field conditions) is limited.
  - Sample size (20 locations, 82 subsamples) may affect representativeness for broader monitoring purposes.
  - Single-study, laboratory-based measurements may require cross-site standardization for nationwide monitoring.

## Data provenance and funding
- Data collected in July 2022 from degradation-focused peatlands, with analysis conducted at the University of Leeds.
- Funded by Natural Environment Research Council Grant NE/S007458/1.