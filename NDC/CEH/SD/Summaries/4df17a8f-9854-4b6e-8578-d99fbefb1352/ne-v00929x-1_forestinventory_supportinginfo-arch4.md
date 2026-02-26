# Post-drought tree canopy condition assessments in the Rhӧn Biosphere Reserve, Germany, 2021.

## Overview
- Objective: Assess tree canopy condition after the 2018/19 extreme drought within the UNESCO Rhӧn Biosphere Reserve, focusing on European beech (Fagus sylvatica).
- Data product: Field measurements of canopy health and individual tree size across 38 plots, plus core samples from a subset of trees.
- Data structure: Central dataset BRRhon_2021_TreeSurveys.csv; some increment core data linked via SiteID_treeCore; site-level characteristics described in data section.
- Data sources: Ground-based canopy assessments complemented by satellite-derived drought impact stratification (Sentinel-2) used to define stratification groups; full satellite-method details available via referenced DOI (10.1111/plb.13391).

## Methods (summary)
- Study area: Core protected areas within the Rhӧn Biosphere Reserve dominated by European beech.
- Plot design: 38 plots using a fixed radius of 10 meters (10 m fixed-radius plots) with stratified random sampling based on drought impact estimates.
- Measurements per tree: DBH measured at 1.3 m, species recorded; canopy condition assessed (damage extent, defoliation, discolouration). Increment cores taken from 3 trees per plot; for cored trees, height and Relative Crown Distance recorded.
- Canopy assessment protocol: Follow ICP Forest Manual (Part IV) for visual crown assessment and damaging agents; mortality recorded as binary (0 = alive, 1 = dead).
- Additional site descriptors: GPS accuracy, elevation, slope (deg), slope form (Convex/Concave/Even), aspect (deg), stoniness (0–5 with defined categories), humus form (soil layer degradation/mixing).
- Canopy and vegetation measures: Canopy cover (%) measured with Canopeo at five positions per plot (center plus four cardinal points), with five readings (CanopyCover_Cen, Nor, Eas, Sou, Wes) and an average; understory and ground vegetation cover and dominant species recorded.
- Data linkage: Tree core data linked to corresponding plots via TreeCoreID; some fields are only measured for cored trees (e.g., Height_m, RelativeCrownDistance).

## Data Structure and Variables
- Dataset: BRRhon_2021_TreeSurveys.csv with the following key columns (definitions as listed in the document):
  - Site ID, SiteID_treeCore, Date, PlotRadius_m, PlotArea_m2
  - Latitude_N, Longitude_E, GPSaccuracy_m, Elevation_m, Slope_deg, SlopeForm (Convex/Concave/Even), Aspect_deg
  - Stoniness (0–5 scale with explicit definitions)
  - Humus Form
  - Canopycover_% and CanopyCover_Cen/Nor/Eas/Sou/Wes (five measurements and average)
  - Understory_% and UnderstorySpecies
  - GroundVegetationCover_% and GroundVegetationSpecies
  - Tree ID, TreeCoreID, Species
  - DistanceToTree_m, DirectionToTree_deg, Tree_X, Tree_Y
  - DBH_cm, BasalArea, Height_m (only for cored trees)
  - CrownVisibility (1–4 scale with guidance)
  - SocialClass (dominant/codominant/subdominant/suppressed, etc.)
  - RelativeCrownDistance (for cored trees; scoring across four directions)
  - Defoliation (1–5 scale with quantifications), Discolouration (1–5 scale with quantifications)
  - ExtentofDamage (1–5 scale with quantifications)
  - Mortality (binary: 0 = alive, 1 = dead)
- Notes on data standards: CanopyCover_% is an average of five readings; height and crown distance are recorded only for increment-core trees. The dataset provides extensive scale definitions and quantitative mappings for several fields (e.g., Stoniness, Defoliation, Discolouration).

## Data Quality, Provenance, and Governance
- Provenance: Field data collected in 2021 by a coordinated field campaign; satellite data used for stratification of drought impact (Sentinel-2).
- Standards and references: ICP Forest Manual guidelines inform crown assessments; DOI provided for satellite-based canopy impact methods (10.1111/plb.13391).
- Metadata and discoverability: Column names and detailed definitions are provided within Section 2 of the document, enabling interpretation and reuse; some data quality controls are not explicitly described (Quality Control: NA in this dataset).
- Data integration: Core data linked via SiteID_treeCore; increment core data referenced to a related dataset in EIDC.

## Implications for Data Leaders
- Data assets: A rich, multi-parameter forest health dataset combining ground-based canopy assessments with plot-level environmental descriptors and satellite-based stratification input.
- Data strategy opportunities:
  - Ensure complete metadata and standardization across datasets (e.g., aligning scales for canopy damage, defoliation, and mortality).
  - Enable discoverability and reuse by maintaining clear links between field data, core samples, and any related datasets in EIDC.
  - Facilitate cross-site comparisons and longitudinal analyses by preserving standardized plotting, measurement protocols, and units.
  - Integrate with broader data communities to support forest health monitoring and drought impact assessment.
- Potential uses: Post-drought canopy health assessment, mortality risk modeling, cross-site health trend analysis, and integration with remote sensing data for enhanced monitoring.

## Challenges and Considerations
- Complexity and heterogeneity: Many variables with different scales and annotations; only subset of measurements (e.g., height, Relative Crown Distance) available for cored trees.
- Metadata completeness: Some fields have rich qualitative definitions; ensure consistency in future updates and across datasets.
- Data accessibility: Primary CSV described; additional increment-core data may reside in linked datasets (EIDC) requiring cross-referencing for full data reuse.

## References and Supporting Materials
- ICP Forest Manual: Visual crown condition assessment and damaging agents (Part IV).
- Satellite-method reference for drought impact stratification: DOI 10.1111/plb.13391.