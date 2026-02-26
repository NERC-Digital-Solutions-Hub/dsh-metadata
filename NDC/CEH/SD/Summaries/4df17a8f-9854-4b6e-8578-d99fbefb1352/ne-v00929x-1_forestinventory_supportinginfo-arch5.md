# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021.

## Overview
- Study in core protected areas of the UNESCO Rhӧn Biosphere Reserve, dominated by European beech (Fagus sylvatica).
- Year: 2021; aims to assess canopy health and tree condition following the 2018/19 extreme drought.
- Data collection follows ICP Forest Manual guidelines for visual crown condition assessment and damaging agents.
- Sampling design uses a stratified random approach based on satellite-detected canopy impacts (Sentinel-2 MSI), comparing post-drought vs. pre-drought vegetation indices.

## Field methods and data collection
- Plot design: 38 plots surveyed using 10 m fixed-radius plots; stratification by estimated canopy impact from drought.
-Tree measurements within plots (DBH > 5 cm):
  - DBH at 1.3 m height, species identification.
  - Canopy condition assessment: extent of damage, canopy discolouration, defoliation.
- Increment cores: 3 trees per plot cored with increment borers; height and Relative Crown Distance recorded for cored trees.
- Additional site data: site-level descriptive characteristics collected (as described in section 2).
- Data file: BRRhon_2021_TreeSurveys.csv records the measurements and observations.

## Data file and structure
- Dataset: BRRhon_2021_TreeSurveys.csv (one csv file).
- Core fields (examples): 
  - Site ID, SiteID_treeCore, Date, PlotRadius_m, PlotArea_m2, Latitude_N, Longitude_E, GPSaccuracy_m, Elevation_m, Slope_deg, SlopeForm, Aspect_deg, Stoniness (0-5), HumusForm, Canopycover_% (including CanopyCover_Cen, CanopyCover_Nor, CanopyCover_Eas, CanopyCover_Sou, CanopyCover_Wes, and average Canopycover_%), Understory_%, UnderstorySpecies, GroundVegetationCover_%, GroundVegetationSpecies, Tree ID, TreeCoreID, Species, DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y, DBH_cm, BasalArea, Height_m (only for core trees), CrownVisibility (1-4), SocialClass (1-5), RelativeCrownDistance, plus derived fields like CDRD_N, Defoliation, Discolouration, ExtentofDamage, Mortality (0 = alive, 1 = dead).
- Data notes: Height_m is only measured for cored trees; some fields use 0-5 or 1-5 scales with qualitative-to-quantitative mappings; Mortality is a binary indicator; Quality Control column is NA.

## Measurements, scales and derived metrics
- Crown condition metrics follow ICP Forest Manual: Defoliation, Discolouration, and ExtentofDamage described with corresponding percent quantifications.
- CDRD_N (crown distance-related damage) calculated as the average of four directional scores.
- Canopy cover measured as a percent with five point measurements (Center and four cardinal points) using Canopeo guidance.
- Structural and micro-site characteristics captured (elevation, slope, aspect, stoniness, humus form) and tree-level attributes (DBH, height for core trees, basal area, distance and direction from plot center).

## Data governance and provenance
- Provenance: field campaign supported by grant NE/V00929X/1; satellite-based stratification method linked to a DOI for the full satellite method.
- Metadata alignment: dataset structured with explicit column names and units; clear spatial coordinates and temporal information for discovery and reuse.
- Linkage opportunities: TreeCoreID enables connection to related increment core datasets (EIDC); single CSV format facilitates upload to data portals and catalogue systems.

## Considerations for data stewardship
- Height data limited to cored trees; interpretive analyses should account for missing height values for non-core trees.
- Multiple scales and qualitative-to-quantitative mappings require consistent handling when merging with other datasets.
- Ensure metadata remains aligned with ICP Forest standards and that derived metrics (e.g., Defoliation, Discolouration, ExtentofDamage, CDRD_N) are documented for reproducibility.