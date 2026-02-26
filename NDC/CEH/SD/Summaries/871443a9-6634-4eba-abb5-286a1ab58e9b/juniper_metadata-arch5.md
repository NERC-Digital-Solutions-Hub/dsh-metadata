# This document provides metadata accompanying the dataset 'Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019'

## Overview
- Metadata accompany the dataset that underpins a related allometric analysis of Juniperus monosperma biomass and sapwood area.
- For full methodological context, refer to the associated (submitted) article: Allometric relationships for predicting aboveground biomass and sapwood area of Oneseed Juniper (Juniperus monosperma) trees.
- The document defines parameters, units, and data structure across two CSV files and outlines study-site procedures.

## Data Files and Variables
- all_stems.csv
  - Tree_ID: unique tree identifier.
  - Stem_ID: unique stem identifier per tree.
  - diameter_at_root_collar_wet: field-measured stem diameter at root collar (wet wood); units: cm.
  - diameter_at_root_collar_dry: lab-measured diameter at root collar on dried disks; units: cm.
  - basal_area_from_image: basal area from image analysis of disks; units: cm^2.
  - sapwood_area: sapwood area from dried disks; units: cm^2.
  - Canopy_area_CA1: canopy area from manually digitized polygons; units: m^2.
  - a, b: canopy diameters (wide point and perpendicular); units: m.
  - max_tree_height: maximum tree height; units: m.
  - (Additional fields include various equivalent diameters and basal areas derived from wet/dry measurements and image analyses.)

- tree_level_data.csv
  - Tree_ID: unique tree identifier; Units: n/a.
  - wet_mass_of_<3cm, wet_mass_of_>3cm: wet mass of small/large diameter components; Units: kg.
  - wet_mass_total: total wet mass; Units: kg.
  - water_content_<3cm, water_content_>3cm, water_content_total: water content proportions; Units: proportion.
  - dry_mass_<3cm, dry_mass_>3cm, dry_mass_total: dry masses; Units: kg.
  - stem_number: number of stems observed at the root collar; Units: count.
  - Equivalent_stem_diameter_wet/dry: whole-tree equivalent stem diameter for wet/dry stems; Units: cm.
  - Basal_area_from_wet_diameter/dry_diameter: whole-tree basal area from wet/dry diameter; Units: cm^2.
  - Basal_area_from_image_analysis: whole-tree basal area from image analysis; Units: cm^2.
  - Sapwood_area: whole-tree sapwood area; Units: cm^2.
  - Canopy_area_CA1: canopy area from polygon digitization; Units: m^2.
  - a, b: canopy diameters as above; Units: m.
  - Canopy_area_CA2: alternative canopy area calculation; Units: m^2.
  - max_tree_height: maximum height; Units: m.

## Study Site and Sampling
- Location: approximately 3-hectare juniper-savannah in the Southwestern Tablelands, central New Mexico; coordinates 34.429°N, 105.861°W; elevation ~1930 m.
- Sampling period: biomass sampling in mid-October 2018 (peak mass) with additional stem harvesting in May 2019.
- Species context: Juniperus monosperma with dominant C4 grasses (Bouteloua gracilis) in the understory.

## Tree Selection
- 20 J. monosperma trees selected to cover a size distribution including the largest individuals near a flux tower.
- Preference for isolated trees to minimize neighbor canopy effects.
- Supplemental large-stem data: an additional 10 large (20–30 cm diameter) stem cross-sections (denoted by stem IDs 'X').

## Maximum Plant Height
- Height measured with a GS08Plus RTK-GNSS instrument at four corner plots.
- Precision ~15 mm relative to a local reference station.
- Hmax computed as the difference between the maximum plant height and an interpolated terrain surface (inverse-distance weighting) to account for low-relief topography.

## Canopy Area
- UAV-based survey conducted on 2018-10-06 using a DJI Phantom 4 Advanced.
- Two flight configurations: nadir (≈21 m) and oblique (≈20°; ≈25 m).
- 75% forward/side overlap; minimum 34 images per study area segment.
- Ground control: 13 markers (20 cm × 20 cm) geolocated with RTK-GNSS.
- Processing: structure-from-motion in Agisoft PhotoScan; EPSG: 26913; dense point cloud generation; orthomosaic at native resolution (0.01 m).
- Canopy delineation:
  - CA1: edge-digitized canopy polygons in ArcPro; area extracted in m^2.
  - a and b: canopy diameters from minimum bounding geometry; used to compute CA2: CA2 = π/4 × (a × b).
  - CA2 is also derived from an ellipse constrained by a and b to compare with CA1.

## Biomass Measurement
- Harvest: two days (8–9 October 2018); 18 of 20 targeted trees harvested due to logistics.
- Component separation: wood tissue (>3 cm diameter) and leaf/twig tissue (<3 cm diameter).
- Wet weights collected within 2 hours of felling; subsamples weighed and oven-dried at 80°C for ≥93 hours to constant weight.
- Water content calculated as (wet mass − dry mass) / wet mass; used to convert wet mass to dry mass; component proportions expressed on a dry-weight basis.

## Basal and Sapwood Area
- Root collar diameter (DRC) defined as the lowest primary branching point.
- Wet DRC measured in the field for disks >5 cm; disks <5 cm measured as mean of major/minor axes.
- 200 disks from 20 trees; disks air-dried ≥30 days and re-measured for DRC Dry.
- Equivalent Stem Diameter (ESD) calculated per tree as the square root of the sum of squared DRC values for wet and dry measurements.
- Basal Area (BA) computed from ESD wet and dry:
  - BA_wet = π × (ESD_wet / 2)^2
  - BA_dry = π × (ESD_dry / 2)^2
- High-resolution images of disks (300 DPI) captured; basal area (BA Image) and sapwood area (SWA) measured via ImageJ, using scale references and clear differentiation of sapwood-heartwood.
- All measurements reported on a whole-tree basis.

## Data Provenance and Usage
- The metadata document accompanies the dataset and supports reproducibility of the linked analysis on allometry.
- Data processing and quality assurance steps are described at the level of field measurements, imagery processing, and image analysis to ensure traceability and reuse in related studies.

## References
- Citations for canopy measurement protocols, biomass methodology, basal area calculations, and supporting literature used in data collection and processing.