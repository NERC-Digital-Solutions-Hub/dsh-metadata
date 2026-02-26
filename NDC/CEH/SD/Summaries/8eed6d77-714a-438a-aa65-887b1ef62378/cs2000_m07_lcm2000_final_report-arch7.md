# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- Purpose: Map broad habitats to LCM2000 Target classes, Subclasses, and Variants to facilitate map-based data products and spatial analysis.
- Structure: For each Broad Habitat, the document lists:
  - LCM Target class
  - LCM Subclasses
  - Variants
- Example mappings: 
  - Inshore Sublittoral mapped to Sea / Estuary target class (with sea as variant)
  - Standing water/canals mapped to Water (inland) target class (with water (inland) variant)
  - Littoral rock mapped to Littoral rock and sediment target class (with rock, algae/mud variants, etc.)
  - Supra-littoral rock, Inland rock, Suburban/urban and others appear under corresponding LCM target classes and variants
- Presentation note: The table pairs broad habitat names with their LCM2000 classifications and map display colours for variants.

## Table 5: LCM2000 and FS coverage by Broad Habitats (km2) and aggregates (UK and constituent countries)

- Purpose: Show how much area is covered by each broad habitat subclass (and aggregates) in LCM2000 vs. field survey (FS).
- Key totals:
  - UK total LCM2000 coverage: 246,688 km2
  - By country (LCM2000 totals):
    - England: 130,362 km2
    - Wales: 20,689 km2
    - Scotland: 77,898 km2
    - Northern Ireland: 17,739 km2
  - UK field survey (FS) totals are shown for many classes (where available), with some entries “n/a” (not available)
- Notable patterns:
  - Substantial differences exist between LCM2000 and FS estimates for several habitats, reflecting calibration, resolution, and survey coverage differences.
  - Aggregated classes such as Arable & Horticultural, Improved grassland, Neutral grassland, Bog, Fen, Marsh & Swamp, Built up areas & gardens, etc., appear repeatedly with country-specific totals.
- Data notes: 
  - LCM2000 statistics come from a full count at 25 m grid
  - FS (field survey) statistics come from Haines-Young et al. 2000
  - Coastal coverage varies due to tidal states and inclusion/exclusion of intertidal areas
  - NI FS data sometimes not available or defined by different survey populations

## Table 6: LCM2000 cover (km2) for Broad Habitats (uncalibrated) vs Field Survey estimates (95% CI) by country and GB

- Purpose: Compare uncalibrated LCM2000 cover with field survey estimates (FS) at 95% confidence for major broad habitats.
- Examples (GB totals with FS 95% CI):
  - Broadleaved/mixed and yew woodland: LCM2000 15,259 km2; FS Low 12,750; FS High 16,670
  - Coniferous woodland: LCM2000 12,879; FS Low 10,672; FS High 16,808
  - Arable and horticulture: LCM2000 56,638; FS Low 47,944; FS High 57,036
  - Improved grassland: LCM2000 50,024; FS Low 50,536; FS High 59,104
  - Neutral grassland: LCM2000 10,770; FS Low 5,046; FS High 7,214
  - Calcareous grassland: LCM2000 10,647; FS Low 72; FS High 1,228
  - Acid grassland: LCM2000 14,483; FS Low 10,594; FS High 15,306
  - Bracken: LCM2000 1,892; FS Low 3,258; FS High 5,522
  - Fen/marsh/swamp: LCM2000 1,197; FS Low 4,138; FS High 6,802
  - Bog: LCM2000 5,134; FS Low 18,696; FS High 25,664
  - Standing open water and canals: LCM2000 2,095; FS Low 790; FS High 3,010
  - Built up areas and gardens: LCM2000 16,132; FS Low 11,028; FS High 15,592
- Across GB, some habitat groups show FS estimates close to LCM2000, while others exhibit larger discrepancies, reflecting calibration and methodological differences between map-based and field survey approaches.
- Notes:
  - FS estimates reported where available; many cells are n/a
  - “Uncalibrated” indicates LCM2000 figures not yet adjusted to field survey data

## Tables 8–10: Summary correspondence matrices between LCM2000 and CS2000 field survey squares (GB, England & Wales, Scotland)

- Purpose: Cross-walk between LCM2000 broad habitats and CS2000 field survey categories, expressed per 1000 or as weighted estimates.
- How to read:
  - Matrices present correspondences for Broad Habitats (yellow), urban generalisation (blue), Target class (pink), and Aggregate class levels (green)
  - Values reflect how often CS2000 categories align with LCM2000 categories across strata (40 Land Classes) and are bootstrapped to provide confidence intervals
- Key takeaway:
  - There is variable alignment between LCM2000 and CS2000 across habitat categories, with some pairs showing strong correspondences and others showing notable mismatches or generalisation effects (e.g., urban generalisation, built-up areas).
- Implication for GIS work:
  - When integrating LCM2000 with CS2000 or other field-survey-based layers, expect habitat-class mismatches for certain groups; plan for crosswalk adjustments or calibration steps in map products.

## Practical implications for GIS specialists

- Data structure and provenance
  - LCM2000 provides broad habitat classifications with target classes, subclasses, and variants suitable for map-based visuals and spatial analysis.
  - CS2000 field survey data are used as a reference for validation and cross-walking; differences between map-based and field-based classifications are common.
- Spatial scale and resolution
  - LCM2000 is built on a 25 m grid; FS information is aggregated to 1 km square units in cross-walks, introducing potential scale-related differences.
- Data gaps and variability
  - Data are distributed across multiple sources and jurisdictions (England, Wales, Scotland, NI); coverage and availability vary by habitat type.
  - Coastal and intertidal areas add complexity due to tidal states and inclusion rules.
- Data quality and standards
  - Inconsistencies in data standards and data storage locations pose challenges for GIS workflows.
  - Large or complex datasets require cleaning, transformation, and careful packaging into manageable chunks.
  - Development of skilled teams and robust data governance is important to maintain, validate, and update map-based assets.
- Practical workflow recommendations for GIS production
  - Use LCM2000 as the primary broad-habitat layer, with explicit crosswalks to CS2000 or field-survey layers for validation and calibration.
  - Be mindful of resolution and coastal area definitions; apply tides/intertidal considerations where relevant.
  - When combining datasets across the UK, account for country-specific differences in totals and FS availability; document assumptions clearly.
  - Use the summary correspondence matrices to anticipate potential classification mismatches and plan QA steps accordingly.
  - Maintain traceability from target class definitions (and their variants) to their map display colors and aggregated groupings for consistent visualization.