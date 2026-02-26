# This document provides metadata accompanying the dataset 'Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019'

## Overview
- Metadata accompany a dataset used to analyze allometric relationships for predicting aboveground biomass and sapwood area of Oneseed Juniper (Juniperus monosperma).
- The associated analysis is described in a submitted manuscript by Cunliffe et al. (authors listed in the document).

## Data files and parameter descriptions
- all_stems.csv
  - Tree_ID: unique tree identifier
  - Stem_ID: unique stem identifier
  - diameter_at_root_collar_wet (cm): stem diameter at root collar in the field (wet wood)
  - diameter_at_root_collar_dry (cm): stem diameter at root collar in the lab (on dried disks)
  - basal_area_from_image (cm^2): basal area calculated from disk images
  - sapwood_area (cm^2): sapwood area from dried disks (image analysis)
  - canopy_area_CA1 (m^2): canopy area from manually digitized polygon
  - a, b (m): canopy diameters at its widest point and perpendicular
  - Canopy_area_CA2 (m^2): canopy area derived from ellipse using a and b
  - max_tree_height (m): maximum plant height (see methods)
- tree_level_data.csv
  - Tree_ID: unique tree identifier
  - wet_mass_of_<3cm> (Kg): wet mass of components < 3 cm diameter
  - wet_mass_of_>3cm (Kg): wet mass of components > 3 cm diameter
  - wet_mass_total (Kg): total wet mass per tree
  - water_content_<3cm>, water_content_>3cm, water_content_total: water content proportions
  - dry_mass_<3cm>, dry_mass_>3cm, dry_mass_total (Kg): dry masses
  - stem_number: number of stems observed at the root collar
  - Equivalent_stem_diameter_wet (cm): whole-tree equivalent stem diameter (wet)
  - Equivalent_stem_diameter_dry (cm): whole-tree equivalent stem diameter (dry)
  - Basal_area_from_wet_diameter (cm^2): basal area from wet diameter
  - Basal_area_from_dry_diameter (cm^2): basal area from dry diameter
  - Basal_area_from_image_analysis (cm^2): whole-tree basal area from image analysis
  - Sapwood_area (cm^2): whole-tree sapwood area from image analysis
  - Canopy_area_CA1 (m^2), a (m), b (m): as above
  - Canopy_area_CA2 (m^2): ellipse-based canopy area from a and b
  - max_tree_height (m): maximum plant height
- Study site details, collection, and processing methods are described in the subsequent sections and the referenced methods article.

## Study site and sampling design
- Location: ca. 3 ha juniper-savannah in the Southwestern Tablelands, central New Mexico
  - Coordinates: 34.429°N, 105.861°W
  - Elevation: 1930 m above sea level
- Sampling period: biomass sampling mid-October 2018; additional stem harvesting in May 2019
- Tree set: 20 J. monosperma trees selected to represent size distribution of largest individuals near a flux tower; focus on isolated trees
- Supplementary material: an additional 10 large stem cross-sections (stem IDs 'X') collected to extend sapwood area analysis for larger diameters

## Maximum plant height measurement
- Instrument: RTK-GNSS system (GS08Plus Leicа Geosystems)
- Precision: ~15 mm relative to local reference station
- Method: height difference between the maximum point of the plant and the interpolated ground surface across four corners of harvest plots (inverse distance weighting)

## Canopy area measurement
- Field imagery: UAV survey on 2018-10-06 using a DJI Phantom 4 Advanced
  - Flight setup: nadir and oblique imagery (~20°) at ~21–25 m above ground
  - Overlap: ~75% forward/side
  - Ground control: thirteen 20 cm x 20 cm markers placed and geolocated with RTK-GNSS
- Processing: structure-from-motion photogrammetry
  - Software: Agisoft PhotoScan (v1.4.3), exported GeoTIFF orthomosaic (0.01 m resolution)
  - Quality controls: sharpness score ≥ 0.84; reprojection errors trimmed; bundle adjustment with calibrated lens parameters
- Canopy delineation and area derivation
  - CA1: canopy area from manually digitized canopy edges on the orthomosaic
  - a and b: major and minor canopy diameters from minimum bounding geometry
  - CA2: canopy area calculated as an ellipse from a and b
  - Validation: spatially constrained by ground control and consistent across methods

## Biomass measurement and moisture analysis
- Harvest: 18 of 20 trees harvested in October 2018 due to logistical constraints
- Component separation: wood tissue (> 3 cm diameter) and leaf/twig tissue (< 3 cm diameter)
- Mass measurements: wet weights recorded within 2 hours of felling
- Subsampling: portions of each component dried at 80°C for ≥ 93 hours to constant weight to determine water content
- Moisture content: calculated as (wet mass − dry mass) / wet mass
- Biomass proportions: expressed on a dry-weight basis

## Basal and sapwood area measurements
- Root collar diameter (DRC) definitions and measurements
  - Wet DRC: field measurement for disks > 5 cm using a tape
  - Dry DRC: diameter measurements on dried disks (< 5 cm) using calipers
- Disk sampling: 200 disks from 20 individuals
  - Drying: air-dried for ≥ 30 days to minimize cracking
  - Sapwood-heartwood differentiation: disks prepared for imaging and analysis
- Equivalent stem diameter (ESD)
  - Wet ESD and Dry ESD: computed as the square root of the sum of squared DRCs across stems for each tree
- Basal area (BA)
  - BA_wet = π * (ESD_wet / 2)^2
  - BA_dry = π * (ESD_dry / 2)^2
  - Units: BA in cm^2
- Image-based measurements
  - BA_Image and Sapwood_area derived from high-resolution disk images using ImageJ
- Canopy and sapwood data
  - Sapwood_area: whole-tree sapwood area from dried stems (image analysis)
  - Canopy_area_CA1: area from manually digitized canopy polygons
  - Canopy_area_CA2: ellipse-based canopy area derived from a and b

## References and methodological context
- Key methodological sources and prior work underpinning measurements and analysis (listed in the document) include:
  - Canopy and biomass measurement protocols for Juniperus species
  - Methods for converting root collar diameter to diameter at breast height and equivalent diameters
  - Prior drone-based biomass and structural quantification approaches, including structure-from-motion photogrammetry and image analysis
  - Foundational work on sapwood-heartwood differentiation, basal area calculations, and related allometric methods

## Purpose and use
- Data are intended to support the development of allometric models for predicting aboveground biomass and sapwood area in Juniperus monosperma
- The dataset provides both raw measurements and derived metrics (e.g., ESD, BA, CA1/CA2) to enable robust statistical analyses and model validation
- The metadata also details data collection and processing steps to facilitate reproducibility and data discovery for downstream analyses or meta-analyses