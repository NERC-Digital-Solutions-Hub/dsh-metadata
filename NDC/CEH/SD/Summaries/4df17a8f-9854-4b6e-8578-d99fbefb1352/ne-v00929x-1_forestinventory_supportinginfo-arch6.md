# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021

## Overview
- Study of post-drought canopy condition for European beech (Fagus sylvatica) within core protected areas of the Rhӧn Biosphere Reserve, Germany (2021).
- Fieldwork collected canopy health data, tree size measurements, and related site characteristics across 38 plots.

## Methods (data collection and design)
- Plot design and sampling:
  - 38 plots surveyed using 10 m fixed-radius plots.
  - Stratified random sampling based on estimated canopy impacts from the 2018/19 drought (using satellite-based canopy damage metrics, Sentinel-2; reference DOI provided for methods).
- Tree and canopy measurements:
  - For each tree with DBH > 5 cm: DBH (1.3 m height) and species recorded; canopy condition assessed for damage extent, discolouration, and defoliation.
  - Increment cores: 3 trees per plot cored; height and Relative Crown Distance measured for core trees.
  - Canopy assessment follows ICP Forest Manual Part IV for visual crown condition and damaging agents.
- Additional site data:
  - Site-level descriptive characteristics recorded (as described in Section 2).

## Data structure and contents
- Dataset: BRRhon_2021_TreeSurveys.csv containing one row per plot and per sampled tree with extensive fields.
- Key fields (selected):
  - Site and plot: SiteID, SiteID_treeCore, Date, PlotRadius_m, PlotArea_m2, Latitude_N, Longitude_E, GPSaccuracy_m, Elevation_m, Slope_deg, SlopeForm (Convex/Concave/Even), Aspect_deg.
  - Soil and ground cover: Stoniness (0-5 scale with defined categories), HumusForm, Canopycover_% with five directional measurements (CanopyCover_Cen, CanopyCover_Nor, CanopyCover_Eas, CanopyCover_Sou, CanopyCover_Wes) and the average canopy cover; Understory_% and UnderstorySpecies; GroundVegetationCover_% and GroundVegetationSpecies.
  - Tree and measurement data: Tree ID, TreeCoreID, Species, DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y, DBH_cm, BasalArea, Height_m (only for CORED trees), CrownVisibility, SocialClass, RelativeCrownDistance.
  - Canopy health metrics (per tree): Mortality (0 alive, 1 dead); Defoliation, Discolouration, ExtentofDamage (each on a 1-5 scale with defined quantifications; see notes in Section 2 for interpretation).
  - Derived metric: CDRD_N (Crown Damage Rating) calculated as the average of four directional scores: (Score1 + Score2 + Score3 + Score4) / 4.
- Notes on coding:
  - Tree cores include Height_m only for cored trees; Tree ID allows multiple stems to be labeled (e.g., 1a, 1b).
  - Canopy cover measurements are based on Canopeo methodology (upward view) with five measurements per plot.

## Measurements and scales
- Canopy and cover:
  - Canopycover_%: overall canopy cover; five directional measurements plus average.
  - Understory_% and GroundVegetationCover_% with dominant species identifiers.
- Tree and crown health:
  - Defoliation: scale 1-5 with percentage quantifications of leaf loss.
  - Discolouration: scale 1-5 with percent leaf material showing discoloration.
  - ExtentofDamage: scale 1-5 representing overall proportion of the tree impacted.
  - Mortality: binary (0 alive, 1 dead).
  - CrownVisibility: 1-4 scale describing visibility of crown parts from ground.
  - RelativeCrownDistance: 1-6 scale describing crown distance relationships to neighboring trees (only for CORED trees); used in calculating CDRD_N.
- Other site and tree attributes:
  - Stoniness (0-5) with detailed field definitions.
  - HumusForm (soil humus degradation/mixing).
  - SocialClass and HeightRank (RelativeCrownDistance describe canopy position and competition).
  - Spatial context: Tree coordinates (Tree_X, Tree_Y) and plot center coordinates.

## Data quality and governance
- Quality control: Noted as NA in the dataset; no explicit QC steps described in the document.
- Data provenance: Field data collected in 2021; linked to satellite-based drought impact assessments and ICP Forest Manual standards for crown condition.
- Data linkage: Site-level and tree-core records are linked via SiteID and TreeCoreID; TreeCoreID corresponds to related core dataset in the European Inventory of Data Collections (EIDC).

## Data products and reuse
- Primary output: A single CSV file enabling plot- and tree-level analyses of post-drought canopy condition and related site characteristics.
- Potential end-user products:
  - Dashboards or pivot-table reports for per-plot canopy health summaries.
  - Maps and spatial analyses integrating plot locations with canopy cover and damage indicators.
  - Cross-dataset analyses linking tree-core data to canopy health (via TreeCoreID and SiteID_treeCore).
- Use cases: Assessing drought impact on canopy health, monitoring regeneration or mortality, and informing forest management or conservation planning.

## References and provenance notes
- Canopy impact assessment methodology references satellite-based approaches (Sentinel-2) and cites a related full-method DOI: 10.1111/plb.13391.
- ICP Forest Manual used for visual crown condition assessment and damaging agents.