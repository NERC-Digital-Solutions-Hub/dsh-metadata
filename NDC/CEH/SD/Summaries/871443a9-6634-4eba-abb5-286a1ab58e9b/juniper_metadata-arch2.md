# Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019

## Overview
- Metadata accompanying the dataset supporting the analysis of allometric relationships for predicting biomass and sapwood area in Oneseed Juniper (Juniperus monosperma).
- Data quality and description reference a comprehensive methods article; the current document focuses on parameter definitions and study details.

## Study site and sampling
- Location: approximately 3-hectare juniper-savannah in the Southwestern Tablelands of central New Mexico; 34.429°N, 105.861°W; elevation about 1930 m above sea level.
- Study period: biomass sampling in mid-October 2018; additional stem harvesting in May 2019.
- Tree selection: 20 J. monosperma trees representing size distribution near a flux tower; emphasis on isolated trees. An extra 10 large stem cross-sections (IDs 'X') were collected to extend sapwood-area analyses for larger diameters.
- Maximum plant height: measured with RTK-GNSS (±≈15 mm precision) using four-corner ground samples; height calculated as the difference between the tallest point and an interpolated ground surface (inverse distance weighting).
- Canopy area: surveyed with a consumer UAV (DJI Phantom 4 Advanced) on 2018-10-06; nadir and oblique imagery; ground control markers used; photogrammetric workflow (structure-from-motion) produced an orthomosaic at 0.01 m resolution; canopy boundaries digitised to derive CA1; bounding diameters a and b measured to compute CA2 via an ellipse-based method.
- Biomass sampling: harvests on 2018-10-08 and 2018-10-09; 18 of the 20 trees were harvested due to logistics. Biomass separated into two components: (i) wood tissue (>3 cm diameter) and (ii) leaf/twig tissue (<3 cm diameter). Wet weights measured promptly; subsamples dried at 80°C until constant mass to determine water content; moisture contents expressed on a green weight basis and used to convert wet to dry mass.
- Basal and sapwood area: root collar diameter (DRC) measured in the field for all disks; disks dried and re-measured to obtain DRC Dry; sapwood-heartwood interface identified via image analysis of dried disks; equivalent stem diameter (ESD) calculated per tree from stem diameters; basal area computed from wet and dry ESD; additional basal area and sapwood area per disk measured via high-resolution images and ImageJ; 200 disks from 20 trees analyzed.

## Data products and structure
- all_stems.csv
  - Key fields include: Tree_ID; Stem_ID; diameter_at_root_collar_wet (cm); diameter_at_root_collar_dry (cm); basal_area_from_image (cm2); sapwood_area (cm2); canopy_area_CA1 (m2); a (m); b (m); canopy_area_CA2 (m2); max_tree_height (m); and related canopy/diameter descriptors.
- tree_level_data.csv
  - Key fields include: Tree_ID; wet_mass_of_<3cm> (kg); wet_mass_of_>3cm (kg); wet_mass_total (kg); water_content_<3cm>, water_content_>3cm, water_content_total (all proportions); dry_mass_<3cm> (kg); dry_mass_>3cm (kg); dry_mass_total (kg); stem_number (count); Equivalent_stem_diameter_wet (cm); Equivalent_stem_diameter_dry (cm); Basal_area_from_wet_diameter (cm2); Basal_area_from_dry_diameter (cm2); Basal_area_from_image_analysis (cm2); Sapwood_area (cm2); Canopy_area_CA1 (m2); a (m); b (m); Canopy_area_CA2 (m2); max_tree_height (m).
- Units and calculation notes are provided within the dataset documentation; the variables summarize whole-tree and component-level biomass, water content, and geometrical properties used in allometric analyses.

## Data quality and processing
- Field and lab procedures ensure consistency: rapid wet mass measurements, standardized oven-drying to constant weight for moisture content, and conversion of wet to dry mass based on measured moisture.
- Canopy-area measurements combine direct polygon delineation (CA1) with an ellipse-based calculation (CA2) to compare field-derived estimates against image-derived measurements.
- Height and canopy geometry rely on high-precision RTK-GNSS and structure-from-motion photogrammetry with ground control and rigorous quality checks (image sharpness, reprojection error thresholds, and bundle adjustment).
- Basal and sapwood-area assessments use direct disk measurements, imaging, and validated equations to compute wet/dry basal areas and sapwood areas.

## Data usage and relevance for environment monitoring
- The dataset provides standardized, traceable measurements of aboveground biomass, canopy area, stem diameter, and sapwood area across a representative sample of juniper trees in a New Mexico savannah.
- These data support the development and validation of allometric relationships for predicting biomass and sapwood area, enabling temporal monitoring and policy-relevant assessments of vegetation structure and carbon stocks.
- Data quality and documentation align with the Analysts Monitoring the Environment archetype by offering transparent methods, standardised outputs, and accessibility of underlying measurements (e.g., disk images, per-tree components, and derived metrics).

## References and methodological context
- Core data and methods linked to: Cunliffe et al., Allometric relationships for predicting aboveground biomass and sapwood area of Oneseed Juniper (Juniperus monosperma) trees (submitted).
- Methodological foundations and protocols cited for canopy photogrammetry, root-collar to diameter conversions, and imaging-based analyses, including:
  - Canopy-area and biomass measurement protocols
  - Structure-from-motion photogrammetry and orthomosaic generation
  - Wet/dry mass determination and moisture content calculations
  - Root collar diameter measurement and equivalent-stem-diameter calculations
  - ImageJ-based analysis for basal area and sapwood area from disks

## Notes
- The dataset and metadata are intended to accompany the main analysis and provide comprehensive parameter definitions to support reproducibility, verification, and reuse in environmental monitoring contexts.