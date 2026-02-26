# Supporting information for: Hydraulic properties of peat extracted from 20 locations at Rensjön palsa mire, Sweden in July 2022

## Overview
- Provides laboratory measurements for peat depth, horizontal saturated hydraulic conductivity (Kh), dry bulk density, and the degree of peat humification (von Post scale) from degrading palsas at Rensjön palsa mire, Norrbotten, Sweden.
- Study supported by Natural Environment Research Council Grant NE/S007458/1.
- Dataset supports environmental monitoring and analysis of peatland hydraulic properties in a degraded permafrost context.

## Study site and sampling
- Location: Rensjön palsa mire, Norrbotten, Sweden (68.0868°N, 19.8314°E).
- Sampled July 2022 from 20 locations on degrading palsas.
- Peat cores collected in PVC downpipes and transported to the University of Leeds, UK for analysis.
- In total, 82 subsamples analyzed.

## Measurements and laboratory methods
- Peat hydraulic conductivity (Kh) determined using a split-cylinder permeameter method.
- Dry bulk density measured from immediately adjacent peat core offcuts using the standard method of Chambers et al. (2011).
- Degree of peat humification measured on adjacent peat core offcuts using the von Post classification (Ekono, 1981).
- Depth_midpoint (m) recorded for each sample; Kh_m_s reported in m s^-1; Von_Post_score reported as H-score; Dry_bulk_density_g_cm3 reported in g cm^-3.

## Quality control
- Measurements conducted by the authors.
- Instrument checks performed; outliers (e.g., anomalously high Kh) removed; repeat measurements conducted when necessary.

## Data file structure
- Data file: fewster_2023_wrr_data.csv (CSV format).
- Columns (7 total):
  - FID: Field ID (na)
  - Subsample_ID: Subsample code (na)
  - Kh_m_s: Horizontal saturated hydraulic conductivity (m s^-1)
  - Depth_midpoint_m: Sample midpoint depth (m)
  - Von_Post_score: Degree of peat humification (H-score)
  - Dry_bulk_density_g_cm3: Dry bulk density (g cm^-3)
  - Degradation_stage: Stage of palsa degradation (desiccating or collapsed), categorical

## Variable definitions and units
- Kh_m_s: Laboratory Kh from split-cylinder permeameter (m s^-1)
- Depth_midpoint_m: Midpoint depth of each sample (m)
- Von_Post_score: Peat humification level according to von Post scale (H-score)
- Dry_bulk_density_g_cm3: Dry bulk density of adjacent peat offcuts (g cm^-3)
- Degradation_stage: Categorical description of degradation extent (desiccating or collapsed)

## Data provenance and metadata
- Dataset contains 82 subsamples from 20 locations.
- Provides methodological references for reproducibility:
  - Chambers, F.M., Beilman, D.W. and Yu, Z. (2011). Methods for determining peat humification and for quantifying peat bulk density, organic matter and carbon content for palaeostudies of climate and peatland carbon dynamics. Mires and Peat, 7(7), 1-10.
  - Ekono, I. (1981). Report on energy use of peat. In UN Conference contributions.

## Funding
- Supported by Natural Environment Research Council Grant NE/S007458/1.