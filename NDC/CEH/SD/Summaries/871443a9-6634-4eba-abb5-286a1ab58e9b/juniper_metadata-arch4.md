# Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019

## Overview
- Metadata for a dataset on Juniperus monosperma from a study in New Mexico (2018–2019) focused on aboveground biomass, canopy area, stem diameter, and sapwood area.
- Supports analysis of allometric relationships for predicting biomass and sapwood area; broader methods described in the associated article.
- Data dictionary and methodology are provided to enable reuse and integration with related research.

## Datasets and key fields
- all_stems.csv
  - Tree_ID and Stem_ID: unique identifiers for trees and their stems.
  - diameter_at_root_collar_wet (cm): stem diameter at root collar measured in the field (wet wood).
  - diameter_at_root_collar_dry (cm): stem diameter at root collar measured on dried disks (lab).
  - basal_area_from_image (cm^2): basal area from image analysis of dried disks.
  - sapwood_area (cm^2): sapwood area from image analysis.
  - Canopy_area_CA1 (m^2): canopy area from manually digitised polygons.
  - a, b (m): canopy diameters at widest point and perpendicular to widest point.
  - Canopy_area_CA2 (m^2): canopy area derived from ellipse-based calculation using a and b.
  - max_tree_height (m): maximum canopy height for each tree.
- tree_level_data.csv
  - wet_mass_of_<3cm> (kg), wet_mass_of_>3cm (kg), wet_mass_total (kg): wet biomass components and totals.
  - water_content_<3cm>, water_content_>3cm>, water_content_total: moisture content proportions.
  - dry_mass_<3cm>, dry_mass_>3cm, dry_mass_total: dry biomass components and totals.
  - stem_number: number of stems observed at root collar.
  - Equivalent_stem_diameter_wet (cm), Equivalent_stem_diameter_dry (cm): whole-tree equivalent stem diameters in field and lab.
  - Basal_area_from_wet_diameter (cm^2), Basal_area_from_dry_diameter (cm^2): basal area derived from diameters.
  - Basal_area_from_image_analysis (cm^2): basal area from image analysis of disks.
  - Sapwood_area (cm^2): whole-tree sapwood area from disks.
  - Canopy_area_CA1 (m^2), a (m), b (m), Canopy_area_CA2 (m^2), max_tree_height (m): canopy metrics and height at the tree level.

## Study site and sampling design
- Location: ~3 ha juniper-savannah in the Southwestern Tablelands, central New Mexico; elevation ~1930 m; coordinates 34.429°N, 105.861°W.
- Timing: biomass sampling in mid-October 2018 (peak mass) with additional stem harvesting in May 2019.
- Tree selection: 20 J. monosperma trees representing size distribution around a flux tower; focus on isolated individuals to avoid neighbor influence; 10 additional large stems (diameter 20–30 cm) to supplement sapwood-area analyses.

## Measurements and methods

### Height and canopy measurements
- Maximum height (H Max) measured with RTK-GNSS (precision ~15 mm) using four corners around each harvest plot; height calculated from a terrain surface interpolated by inverse distance weighting.
- Canopy area measured via UAV photogrammetry:
  - Platform: DJI Phantom 4 Advanced; nadir and oblique flights (about 21 m and 25 m AGL).
  - Processing: structure-from-motion in Agisoft PhotoScan; 0.01 m orthomosaic resolution; dense point cloud and TIN created; canopy edges manually digitised in ArcPro to derive CA1 and canopy diameters a and b.
  - Canopy areas: CA1 from digitised polygons; CA2 computed as π/4 × a × b (ellipse-based).

### Biomass measurement
- Harvest: 18 of 20 selected trees (two were not harvested due to logistical constraints).
- Biomass separated into:
  - Wood tissue (>3 cm stem diameter) and leaf/twig tissue (<3 cm diameter).
- Procedures:
  - Wet weights measured within 2 hours of felling.
  - Subsamples weighed, oven-dried at 80°C for ≥93 hours to constant mass; moisture content calculated on a wet basis and used to convert wet to dry masses.
  - Component proportions reported on a dry-weight basis.

### Basal and sapwood area measurements
- Root collar diameter (DRC) defined as the lowest primary branching point; wet measurements in the field for disks > 5 cm, caliper-based measurements for disks < 5 cm; n = 200 disks from 20 trees.
- Disks air-dried ≥30 days, re-measured to obtain DRC Dry; sapwood-heartwood interface distinguished on disks.
- Equivalent stem diameter (ESD) calculated as sqrt(sum of squared DRCs) for wet and dry measurements.
- Basal area computations:
  - BA_wet = π × (ESD_wet / 2)^2
  - BA_dry = π × (ESD_dry / 2)^2
- Image-based measurements:
  - High-resolution (300 DPI) disk images taken; BA_Image and Sapwood_area derived from ImageJ analysis with known scale.

## Data quality, provenance, and notes
- UAV data quality controlled via image sharpness threshold and robust photogrammetry parameters; bundle adjustment and dense point cloud processing performed with predefined camera models and accuracy settings.
- Canopy edges manually delineated by a single operator to ensure consistency.
- Disk measurements and imaging followed standardized protocols; wet-to-dry conversions based on moisture content determined from subsamples.
- References provided for methods and data collection workflows, including drone-based biomass assessment and allometric approaches.

## Usage considerations for data leaders
- The dataset provides a rich, multi-scale view linking per-disk, per-tree, and canopy-level measurements, suitable for validating or extending allometric models for Juniperus monosperma.
- Metadata and two complementary data files (all_stems.csv and tree_level_data.csv) enable integration with other datasets and support end-to-end biomass and canopy analyses.
- Notable limitations: modest sample size (20 trees, 18 harvested), manual canopy delineation, and potential constraints related to data collection windows; these should be considered when scaling analyses or applying models to broader populations.
- For full methods and context, refer to the accompanying analysis article on allometric relationships and the cited methodological references.