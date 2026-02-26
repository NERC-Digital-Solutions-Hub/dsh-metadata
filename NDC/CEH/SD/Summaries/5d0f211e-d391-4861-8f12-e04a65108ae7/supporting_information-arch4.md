# Supporting information for: Hydraulic properties of peat extracted from 20 locations at Rensjön palsa mire, Sweden in July 2022

## Overview
- Dataset of laboratory measurements on degrading palsas at Rensjön palsa mire, Norrbotten, Sweden.
- Variables include horizontal saturated hydraulic conductivity (Kh), dry bulk density, degree of peat humification (von Post), peat sample depth (depth midpoint), and degradation stage.
- Study supported by Natural Environment Research Council Grant NE/S007458/1.

## Study design and data collected
- 20 locations on degrading palsas sampled in July 2022 (coordinates: 68.0868°N, 19.8314°E).
- Peat cores collected in PVC downpipes and transported to the University of Leeds, UK lab.
- Subsampling for analysis: 82 total subsamples.
- Measurements focused on:
  - Kh using a split-cylinder permeameter method.
  - Dry bulk density from adjacent peat core offcuts (Chambers et al., 2011).
  - Degree of peat humification using von Post scale on adjacent offcuts (Ekono, 1981).

## Data structure and variables
- Data file: fewster_2023_wrr_data.csv (CSV, seven columns).
- Variables:
  - FID: Field identifier (no units).
  - Subsample_ID: Subsample code (no units; used to identify subsamples during analyses).
  - Kh_m_s: Horizontal saturated hydraulic conductivity (m s^-1).
  - Depth_midpoint_m: Sample midpoint depth (m).
  - Von_Post_score: Degree of peat humification (von Post scale; H-score).
  - Dry_bulk_density_g_cm3: Dry bulk density (g cm^-3).
  - Degradation_stage: Stage of palsa degradation (categorical; desiccating or collapsed).

## Methods and quality control
- Kh measured with split-cylinder permeameter.
- Dry bulk density measured on adjacent offcuts using standard method (Chambers et al., 2011).
- Von Post humification assessed on adjacent offcuts (Ekono, 1981).
- Quality control:
  - All measurements performed by the authors.
  - Instrument checks, outlier removal (e.g., anomalous Kh values), and repeat measurements when needed.

## Provenance and references
- Field collection and laboratory analysis conducted in 2022.
- References for methods:
  - Chambers, F.M., Beilman, D.W., Yu, Z. (2011). Methods for determining peat humification and for quantifying peat bulk density, organic matter and carbon content. Mires and Peat.
  - Ekono, I. (1981). Report on energy use of peat. UN Conference on New and Renewable Sources of Energy.

## Potential uses and data stewardship notes
- Useful for analyzing spatial variation of hydraulic properties across 20 locations and across degradation stages.
- Enables examination of relationships between Kh, dry bulk density, humification, depth, and degradation state.
- Data is in a single CSV with clear variable definitions and units, facilitating discoverability and reuse.
- For broader integration, consider aligning with any sector data standards and documenting any additional metadata (e.g., sampling depths, exact field conditions) if expanding the dataset.