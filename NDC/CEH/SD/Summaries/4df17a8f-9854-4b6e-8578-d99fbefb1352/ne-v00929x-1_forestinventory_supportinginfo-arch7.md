# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021.

## Aim
- Document post-drought canopy condition assessments in the UNESCO Rhӧn Biosphere Reserve.
- Provide field-collection methods and a structured dataset to support GIS-based visualization and analysis of canopy health.

## Methods (Section 1)

- Study area and focus
  - Core protected areas within the Rhӧn Biosphere Reserve, dominated by European beech (Fagus sylvatica).
  - Field assessments of individual trees and stands to evaluate canopy health after extreme drought (2018/19).
- Sampling design
  - 38 plots surveyed using 10 m fixed-radius plots.
  - Stratified random sampling based on estimated canopy impact from drought, using satellite-derived metrics.
  - Satellite-based canopy damage assessed via Sentinel-2 MSI; used pre- vs post-drought vegetation indices to stratify sites.
- Data collected per tree and plot
  - For trees with DBH > 5 cm: DBH at 1.3 m, species, and a canopy condition assessment capturing damage extent, canopy discoloration, and defoliation.
  - Three trees per plot were cored with increment borers; height and Relative crown distance measured for cored trees.
- Protocols and standards
  - Canopy condition assessments follow the ICP Forest Manual (Part IV) for harmonized crown-condition sampling and analysis.
- Additional site characteristics
  - Site-level descriptive characteristics recorded (see Section 2 for details).

## Data Structure, Nature and Units (Section 2)

- Dataset
  - One CSV file: BRRhon_2021_TreeSurveys.csv.
- Key column groups (with representative fields)
  - Site and plot identifiers
    - Site ID, SiteID_treeCore
    - Date of survey
    - PlotRadius_m, PlotArea_m2
  - Location and topography
    - Latitude_N, Longitude_E
    - GPSaccuracy_m
    - Elevation_m
    - Slope_deg, SlopeForm (Convex, Concave, Even)
    - Aspect_deg
  - Substrate and environment
    - Stoniness (0–5 scale with detailed definitions)
    - Humus Form
  - Canopy and vegetation context
    - Canopycover_% (overall canopy cover)
    - CanopyCover_Cen, CanopyCover_Nor, CanopyCover_Eas, CanopyCover_Sou, CanopyCover_Wes (per-point canopy cover measurements)
    - Understory_% and UnderstorySpecies
    - GroundVegetationCover_% and GroundVegetationSpecies
  - Tree-level data
    - Tree ID, TreeCoreID
    - Species
    - DistanceToTree_m, DirectionToTree_deg
    - Tree_X, Tree_Y (spatial coordinates of tree stem)
    - DBH_cm, BasalArea
    - Height_m (measured for cored trees)
    - CrownVisibility (1–4 scale)
    - SocialClass (Dominant, Codominant, Subdominant, Suppressed, Dying)
    - RelativeCrownDistance (for cored trees; 4 directions on a 16-point scale)
    - Defoliation (1–5 scale with percentage quantifications)
    - Discolouration (1–5 scale with percentage quantifications)
    - ExtentofDamage (1–5 scale with percentage quantifications)
    - Mortality (0 = alive, 1 = dead)
- Computed metrics
  - Canopy Damage Rating Denominator (CDRD_N): calculated as the average of four directional scores (Score1–Score4) around the sample tree.
- Additional notes
  - Core data availability: increment core data exists in a separate related dataset.
  - Canopy cover methodology: five measurements per plot, taken with Canopeo app, averaged (center + four cardinal points).
  - References for methods: ICP Forest Manual; satellite-based canopy-damage method DOI 10.1111/plb.13391.

## Spatial and GIS considerations

- Spatial resolution and scale
  - Plot-level fixed-radius (10 m) plots with georeferenced centers; per-tree coordinates provided (Tree_X, Tree_Y) and plot center coordinates.
- Data integration opportunities
  - Link field data with Sentinel-2 derived canopy-damage metrics for stratification and validation.
  - Combine with elevation, slope, aspect, stoniness, and humus form for environmental analyses.
- Map-ready outputs
  - Canopy health indicators (defoliation, discolouration, extent of damage, mortality) can be mapped at tree and plot levels.
  - CDRD_N provides a summarized canopy damage metric for visualization across the landscape.
  - Per-tree height, DBH, and crown characteristics support multi- layer forest visualizations and stand structure maps.

## Practical GIS usage tips

- Data integration
  - Use Tree_X and Tree_Y for precise point mapping; cross-validate with Latitude_N and Longitude_E.
  - Integrate plot-level attributes (PlotRadius_m, PlotArea_m2, CanopyCover measures) for polygon-based analyses around each plot center.
- Visualization ideas
  - Create thematic maps showing mortality and canopy damage intensity by plot and by individual trees.
  - Build layered maps combining environmental covariates (elevation, slope, aspect, stoniness, humus form) with canopy health indicators.
- Quality and consistency considerations
  - Rely on standardized field protocols (ICP Forest Manual) to ensure comparability across plots and trees.
  - Be mindful of GPS accuracy field when aligning datasets with other geospatial layers.
- Data gaps and planning
  - Acknowledge the separate increment-core dataset when analyzing growth and age structure in relation to canopy health.
  - Use stratification variable (drought impact) to interpret spatial patterns in the context of initial drought risk.

## Summary of relevance for GIS specialists

- The dataset provides a rich, geo-referenced, multi-scale view of post-drought canopy health across 38 plots in a beech-dominated biosphere reserve.
- It combines precise tree-level measurements (DBH, height for cores, crown condition) with plot-level environmental context and canopy context, enabling detailed GIS analyses and map-based data products.
- The inclusion of satellite-derived stratification data, standardized protocols, and per-tree coordinates makes it suitable for integrating field observations with remote sensing data to produce informative canopy health visualizations and risk assessments.