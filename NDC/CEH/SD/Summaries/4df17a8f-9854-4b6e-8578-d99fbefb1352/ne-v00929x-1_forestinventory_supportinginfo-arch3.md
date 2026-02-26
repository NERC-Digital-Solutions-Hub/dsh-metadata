# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021.

## Overview
- This study collects forest inventory and canopy health data from core protected areas of the UNESCO Rhӧn Biosphere Reserve, focusing on European beech (Fagus sylvatica).
- Aims to assess canopy condition after the 2018/19 extreme drought and to support monitoring and decision-making for environmental health policy.
- Data include field measurements, plot-level characteristics, and a dataset designed for integration with satellite-based drought impact assessments.

## Study design and methods
- Plots and sampling
  - 38 plots surveyed using 10 m fixed-radius plots.
  - Stratified random sampling based on estimated canopy impacts from the drought event, using satellite-derived indicators (Sentinel-2 MSI) of canopy damage to stratify sites.
- Field measurements
  - For all trees with DBH > 5 cm: DBH measured at 1.3 m, species recorded, and canopy condition assessed (extent of damage, defoliation, and discolouration).
  - Three trees per plot increment cores collected (height and Relative Crown Distance measured for cored trees; core data stored separately).
  - Height recorded for cored trees; other architecture variables recorded as part of crown condition assessment.
- Standards and protocols
  - Canopy condition assessments follow the ICP Forest Manual (Part IV) for visual crown condition and damaging agents.
  - Relative site characteristics (elevation, slope, aspect, etc.) and plot-level descriptors were recorded to support environmental health interpretation.
- Remote sensing integration
  - Baseline (pre-drought) and post-drought canopy assessments derived from satellite observations to quantify canopy damage and support stratification and interpretation.

## Data collected and structure
- Dataset: BRRhon_2021_TreeSurveys.csv
- Core fields (selected highlights):
  - Site and plot identifiers: Site ID, SiteID_treeCore, Date, PlotRadius_m, PlotArea_m2
  - Location and topography: Latitude_N, Longitude_E, GPSaccuracy_m, Elevation_m, Slope_deg, SlopeForm (Convex/Concave/Even), Aspect_deg
  - Substrate and ground attributes: Stoniness (0-5), Humus Form; Canopycover_% with subfields CanopyCover_Cen, CanopyCover_Nor, CanopyCover_Eas, CanopyCover_Sou, CanopyCover_Wes; Understory_% and UnderstorySpecies; GroundVegetationCover_% and GroundVegetationSpecies
  - Vegetation and trees: Species; DBH_cm; BasalArea; Height_m (for cored trees); Tree X/Y coordinates; DistanceToTree_m; DirectionToTree_deg; SocialClass (1-5); RelativeCrownDistance (scores 1-6 across four directions for cored trees)
  - Crown condition and damage: CanopyVisibility (1-4); Defoliation and Discolouration (1-5 scales with quantified ranges); ExtentofDamage (1-5 with quantified ranges); Mortality (0 = alive, 1 = dead)
  - Tree and core relationships: Tree ID; TreeCoreID (links to increment core dataset)
- Notable computed metric:
  - CDRD_N: a composite score calculated as (Score1 + Score2 + Score3 + Score4) / 4 for crown-related damage measures.
- Data notes
  - Height_m is recorded only for trees from which cores were taken.
  - Quality Control: Not specified (NA) in the dataset documentation.
  - Data are tied to a DOI for satellite-based canopy impact methods (Planta, DOI: 10.1111/plb.13391).

## Measurements and indicators relevant to environmental health monitoring
- Canopy health indicators
  - Defoliation: proportion of leaf area lost, scaled 1-5 with quantified percentages.
  - Discolouration: proportion of leaves showing discoloration, scaled 1-5 with quantified percentages.
  - Extent of Damage: overall proportion of the tree affected (leaves, branches, or stem), scaled 1-5 with quantified percentages.
  - Mortality: alive/dead status (0/1).
  - Crown visibility and relative crown distance to neighboring trees to infer competition and crowding effects.
- Structural and site descriptors
  - DBH, Basal Area, Height (for cores) to characterize tree size and growth status.
  - Stand and site context (elevation, slope, aspect, humus form, stoniness, understory and ground vegetation cover and composition) to understand habitat conditions.
  - Canopy cover (Canopycover_%) with multi-point measurements within each plot to quantify light interception and stand structure.
- Data synthesis
  - A linearly averaged composite (CDRD_N) provides an integrative measure of crown damage across four directional assessments for each core tree, facilitating comparisons within and across plots.

## Data governance and applicability for monitoring frameworks
- Alignment with established monitoring practices (ICP Forest Manual) ensures comparability with other forest health datasets.
- Integration with satellite-derived drought impact indicators enables robust cross-validation between ground truth and remote sensing.
- Data structure supports transparency and reproducibility: unique identifiers for sites, plots, and trees; clear column naming; and explicit measurement protocols.
- Potential data governance considerations for monitoring frameworks:
  - Data accessibility and sharing, given the need to assemble multiple linked datasets (field, core, and satellite-derived data).
  - Metadata completeness to support verification and reuse (notes indicate some metadata gaps and a reliance on external manuals for standard methods).
  - Data updating and timeliness to address concerns about keeping information current across monitoring cycles.

## Endnotes
- The methods reference a supplementary source for satellite-based canopy impact assessment (DOI provided) and follow ICP Forest guidelines for crown condition evaluation.
- Increment cores and additional height data are available in related datasets not included in BRRhon_2021_TreeSurveys.csv.