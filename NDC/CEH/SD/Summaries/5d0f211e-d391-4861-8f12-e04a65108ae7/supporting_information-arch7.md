# Supporting information for: Hydraulic properties of peat extracted from 20 locations at Rensjön palsa mire, Sweden in July 2022

- Purpose and scope
  - Provides laboratory measurements of peat hydraulic properties and related characteristics for degrading palsas at Rensjön palsa mire, Norrbotten, Sweden.
  - Data collected in July 2022; study supported by Natural Environment Research Council Grant NE/S007458/1.

- Study site and sampling
  - 20 locations on degrading palsas sampled.
  - Peat cores collected in PVC downpipes and transported to the University of Leeds for analysis.
  - Total subsamples analyzed: 82.

- Measured variables (data product)
  - Horizontal saturated hydraulic conductivity (Kh) in m s^-1, measured with a split-cylinder permeameter.
  - Dry bulk density (g cm^-3) measured from immediately adjacent peat core offcuts.
  - Degree of peat humification (von Post score), measured on adjacent offcuts.
  - Depth_midpoint_m: midpoint depth of each sample (m).
  - Degradation_stage: categorical description of palsa degradation (desiccating or collapsed).

- Data file structure
  - File: fewster_2023_wrr_data.csv
  - Seven columns:
    - FID: Field identifier (NA units)
    - Subsample_ID: Subsample code used during laboratory analyses (NA units)
    - Kh_m_s: Horizontal saturated hydraulic conductivity (m s^-1)
    - Depth_midpoint_m: Sample midpoint depth (m)
    - Von_Post_score: Degree of peat humification (H-score)
    - Dry_bulk_density_g_cm3: Dry bulk density (g cm^-3)
    - Degradation_stage: Stage of palsa degradation (desiccating or collapsed)

- Quality control and data handling
  - All measurements conducted by the authors.
  - Instrument checks performed; outliers removed (e.g., anomalously high Kh values).
  - Measurements repeated when necessary to ensure reliability.

- Practical notes for GIS use
  - Enables spatial analysis of peat hydraulic properties and degradation status when linked with location data.
  - Attributes suitable for map-based visualization: Kh_m_s, Depth_midpoint_m, Von_Post_score, Dry_bulk_density_g_cm3, Degradation_stage.
  - Data integrity depends on linking 20 location coordinates with subsample data; the CSV provides subsample-level measurements and sample midpoint depths.

- References (method context)
  - Chambers, F.M., Beilman, D.W., and Yu, Z. 2011. Methods for determining peat humification and for quantifying peat bulk density, organic matter and carbon content. Mires and Peat.
  - Ekono, I. 1981. Report on energy use of peat. UN Conference on New and Renewable Sources of Energy.