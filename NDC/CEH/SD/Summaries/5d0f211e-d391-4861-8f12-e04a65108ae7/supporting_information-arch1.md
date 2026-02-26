Supporting information for: Hydraulic properties of peat extracted from 20 locations at Rensjön palsa mire, Sweden in July 2022

- Purpose and scope
  - Provides laboratory measurements of peat hydraulic properties from degrading palsas at Rensjön palsa mire, Norrbotten, Sweden.
  - Variables include depth, horizontal saturated hydraulic conductivity (Kh), dry bulk density, and peat humification (von Post scale).
  - Data collected in July 2022; supported by Natural Environment Research Council Grant NE/S007458/1.

- Study site and collection methods
  - Location: 20 locations on degrading palsas at Rensjön palsa mire (68.0868°N, 19.8314°E).
  - Sampling: peat cores collected in PVC downpipes; transported to University of Leeds for analysis.
  - Subsampling: 82 subsamples analyzed for hydraulic properties.
  - Measurements:
    - Kh: determined using a split-cylinder permeameter.
    - Dry bulk density: measured on adjacent peat core offcuts (Chambers et al., 2011 method).
    - Peat humification: von Post classification applied to adjacent peat core offcuts (Ekono, 1981 method).

- Quality control
  - Measurements conducted by the authors.
  - Instruments checked; outliers removed (e.g., anomalously high Kh values) and measurements repeated when necessary.

- Data structure and contents
  - Data file: fewster_2023_wrr_data.csv (CSV, seven columns).
  - Variables:
    - FID: Field identifier.
    - Subsample_ID: Subsample code used during laboratory analyses.
    - Kh_m_s: Horizontal saturated hydraulic conductivity (m s^-1).
    - Depth_midpoint_m: Midpoint depth of each sample (m).
    - Von_Post_score: Degree of peat humification (von Post scale; H-score).
    - Dry_bulk_density_g_cm3: Dry bulk density (g cm^-3).
    - Degradation_stage: Categorical descriptor of palsa degradation (desiccating or collapsed).
  - Units: Kh in m s^-1; Depth and density with standard metric units; Von Post as scale value; Degradation_stage as category.

- Methods and references
  - Kh measurement: split-cylinder permeameter method.
  - Dry bulk density: standard method (Chambers et al., 2011).
  - Humification: von Post scale (Ekono, 1981).
  - References for methods provided in the dataset documentation.

- Potential analyses for data users (analysts)
  - Explore correlations between Kh and depth, dry bulk density, and von Post humification.
  - Assess variation in Kh, density, and humification across the 20 locations and 82 subsamples.
  - Develop predictive relationships or simple models for Kh as a function of depth, degradation stage, and humification.
  - Use degradation stage and location metadata to investigate spatial or degradation-related drivers of hydraulic properties.
  - Integrate with other datasets to assess implications for peatland hydrology and carbon dynamics under degradation scenarios.

- Limitations and considerations
  - Spatial coverage limited to 20 locations on degrading palsas; may affect generalizability.
  - 82 subsamples; potential within-site heterogeneity.
  - Von Post measurements based on adjacent offcuts; assumes representative humification of sampled peat.
  - July 2022 timing; seasonal influences not captured.

- Data provenance and access
  - Dataset supports published work on hydraulic properties of peat at Rensjön palsa mire.
  - Data generated and quality-checked by the study authors; aims to be accessible for replication and further analysis.
  - Grant support: Natural Environment Research Council (NE/S007458/1).