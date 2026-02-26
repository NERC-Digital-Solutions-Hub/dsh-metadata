# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021

## Aim
- Assess post-drought canopy condition of European beech (Fagus sylvatica) forests within core protected areas of the Rhön Biosphere Reserve.
- Collect field measurements of canopy health and individual tree size to evaluate drought impacts and support subsequent analyses.

## Methods

- Plot design and sampling
  - 38 plots surveyed using a fixed 10 m radius plot.
  - Stratified random sampling based on estimated canopy impact from the 2018/19 extreme drought.
  - Stratification informed by satellite-based canopy damage indicators (Sentinel-2 MSI) comparing post-drought vs pre-drought baselines.
- Data collection at tree level (DBH > 5 cm)
  - Recorded DBH at 1.3 m height, species, and canopy condition (extent of damage, defoliation, and discolouration).
  - Three trees per plot were cored with increment borers; height and Relative Crown Distance measured for coring trees.
- Canopy health assessment and protocols
  - Canopy assessments followed the ICP Forest Manual Part IV (Visual Assessment of Crown Condition and Damaging Agents).
- Site and stand characteristics
  - Collected descriptive site data per plot (elevation, slope, aspect, stoniness, humus form, etc.).
  - Documented understory and ground vegetation cover and composition.
- Data quality and structure notes
  - Quality control field: NA.

## Data collected and key measurements

- Tree and plot measurements
  - Tree DBH (cm), Basal Area, Height (m for cored trees), Species
  - Tree position and distance metrics: DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y
  - Crown health metrics: Defoliation, Discolouration, ExtentofDamage, Mortality (0 = alive, 1 = dead)
  - Crown visibility (1–4) and relative tree position in canopy (SocialClass: 1–5)
  - Relative Crown Distance for cored trees (scores 1–6 across four directions)
- Plot and site characteristics
  - PlotRadius_m, PlotArea_m2
  - GPS accuracy (m), Latitude/Longitude, Elevation_m, Slope_deg, SlopeForm (Convex, Concave, Even), Aspect_deg
  - Stoniness (0–5 scale)
  - Humus Form (soil humus classification)
  - Canopy cover (%; five measurements CanopyCover_Cen, Nor, Eas, Sou, Wes with an average Canopycover_%)
  - Understory % cover and dominant UnderstorySpecies
  - Ground Vegetation Cover % and dominant GroundVegetationSpecies
- Derived measures
  - Crown Damage Rating Distance (CDRD_N) calculated as (Score1 + Score2 + Score3 + Score4) / 4
  - Mortality flag per tree
- Data file
  - BRRhon_2021_TreeSurveys.csv containing all the fields above
  - Each row corresponds to a tree (or plot-level entry) with associated plot and site data
  - TreeCoreID links to increment core records in related datasets
- Notes on data interpretation
  - Damage components reflect multiple aspects: leaf and branch damage, defoliation, and discolouration; extent-of-damage integrates the proportion of tree area affected
  - Additional guidance from ICP Forests handbook clarifies that damage extent combines both proportion affected and damage intensity on leaf/branch/stem levels

## Data Structure and key variables

- Columns and meaning (examples)
  - Site ID, Date, PlotRadius_m, PlotArea_m2, Latitude_N, Longitude_E, Elevation_m, Slope_deg, SlopeForm, Aspect_deg, Stoniness, Humus Form
  - Canopycover_% and CanopyCover_Cen/Nor/Eas/Sou/Wes (individual and average)
  - Understory_% and UnderstorySpecies
  - GroundVegetationCover_% and GroundVegetationSpecies
  - Tree ID, TreeCoreID, Species, DBH_cm, BasalArea, Height_m
  - DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y
  - CrownVisibility (1–4)
  - SocialClass (1–5)
  - RelativeCrownDistance (4-direction scores for cores)
  - Defoliation, Discolouration, ExtentofDamage (1–5 scales with quantified percentages)
  - Mortality (0 = alive, 1 = dead)
- Units
  - Lengths in meters; DBH in centimeters; Height in meters
  - Angles in degrees; Canopy cover and understory in percent
  - Humus form and slope form categorical descriptors
- Data provenance
  - Field measurements taken in 2021, with reference to 2018/19 drought conditions
  - Satellite-derived stratification used to select plots for sampling

## References and data access

- Grant support: NE/V00929X/1
- Satellite method DOI for canopy damage assessment: 10.1111/plb.13391

## Relevance for analysis

- Enables examination of correlations between post-drought canopy condition and site factors (elevation, slope, aspect, stoniness, humus form) and stand structure (canopy cover, understory, ground vegetation).
- Allows analysis of tree-level responses to drought via Defoliation, Discolouration, ExtentofDamage, and Mortality, including how these relate to DBH, height (for cored trees), and crown position (SocialClass, RelativeCrownDistance).
- Provides a derived metric (CDRD_N) to quantify crown-distance related damage, enabling spatially-informed modeling of canopy health.
- Facilitates multi-source data integration given the dataset’s explicit cross-references (TreeCoreID, can be combined with increment core datasets) and standardized measurement protocol (ICP Forest Manual).

## Considerations and limitations

- Sample scope limited to 38 plots within core protected areas and beech-dominated stands; may limit broader generalizability.
- Data capture relies on field assessments with potential observer variability; uses ICP Forest guidelines to standardize scoring.
- Quality Control field is marked NA, which may affect replicability checks; cross-reference with related datasets recommended.