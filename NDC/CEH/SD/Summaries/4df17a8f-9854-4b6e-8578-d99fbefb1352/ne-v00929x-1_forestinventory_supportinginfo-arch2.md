# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021.

## Purpose and setting
- Objective: Assess post-drought canopy condition to monitor forest health and inform policy-related environmental health assessments.
- Location: Core protected areas of the UNESCO Rhӧn Biosphere Reserve, dominated by European beech (Fagus sylvatica).
- Timeframe: 2021, with drought-impact stratification based on the 2018/19 extreme drought event.

## Methods overview
- Field design: 38 plots surveyed using fixed 10 m radius plots; stratified random sampling based on estimated canopy impacts from drought.
- Data collected per tree (DBH > 5 cm): DBH, species, canopy condition (extent of damage, defoliation, discolouration); three trees per plot increment cores; height and Relative Crown Distance for cored trees.
- Canopy health assessment: Followed ICP Forest Manual Part IV (Visual Assessment of Crown Condition and Damaging Agents).
- Remote sensing linkage: Stratification informed by satellite-based canopy damage (Sentinel-2 MSI) comparing post-drought to pre-drought baselines.

## Data structure and key variables
- Dataset: BRRhon_2021_TreeSurveys.csv containing the following types of fields:
  - Site and plot metadata: Site ID, Date, PlotRadius_m, PlotArea_m2, Latitude_N, Longitude_E, GPSaccuracy_m, Elevation_m, Slope_deg, SlopeForm (Convex/Concave/Even), Aspect_deg, Stoniness (0–5), Humus Form.
  - Canopy and vegetation context: Canopycover_% (with five location-specific measurements: CanopyCover_Cen, CanopyCover_Nor, CanopyCover_Eas, CanopyCover_Sou, CanopyCover_Wes, plus average); Understory_% and UnderstorySpecies; GroundVegetationCover_% and GroundVegetationSpecies.
  - Tree and plot anatomy: Tree ID, TreeCoreID (link to increment core dataset), Species, DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y, DBH_cm, BasalArea, Height_m (for cored trees), CrownVisibility (1–4), SocialClass (1–5), RelativeCrownDistance (for cored trees).
  - Health and damage metrics: Mortality (0 = alive, 1 = dead); Defoliation (1–5 scale with quantitative ranges); Discolouration (1–5 with quantitative ranges); ExtentofDamage (1–5 with quantitative ranges).
  - Calculations and notes: CDRD_N (computed as (Score1 + Score2 + Score3 + Score4) / 4); description notes on damage components (branch damage, stem damage, leaf-area loss, etc.).

## Data processing, outputs, and integration
- Scoring: Crown health scores per tree aggregated into CDRD_N to represent overall crown damage rating.
- Data linkage: Tree increment cores stored separately; TreeCoreID enables cross-dataset linking for in-depth age/growth analyses.
- Outputs: Site-level descriptive characteristics and a harmonised, geolocated dataset suitable for cross-site comparisons and temporal monitoring when repeated.

## Quality, management and access
- Standardised data collection: ICP Forest Manual-based methods ensure comparable canopy-health assessments across plots and over time.
- Data management: Clear field/column documentation supports reproducibility and reuse; dataset designed for integration with satellite-derived canopy metrics and other environmental datasets.
- Reusability for monitoring: Enables evaluation of drought impacts on canopy condition, supports long-term environmental health monitoring within the biosphere reserve.

## Relevance for the Analysts Monitoring the Environment archetype
- Provides a replicable, standardized dataset enabling long-term environmental health monitoring and policy performance evaluation.
- Combines ground-based canopy assessments with satellite-based stratification to improve data relevance and comparability.
- Supports data sharing and interoperability through explicit data structure and field definitions, aligning with aims to broaden data value and access to underlying datasets.