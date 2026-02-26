# Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019

## Overview
- Metadata accompanying the dataset set that underpins the analysis of allometric relationships for predicting biomass and sapwood area in Oneseed Juniper (Juniperus monosperma).
- Primary data are organized in two CSV files with detailed parameter explanations:
  - all_stems.csv
  - tree_level_data.csv
- Study context and methods are described to support data provenance, quality, and reuse.

## Datasets and key variables

- all_stems.csv
  - Tree_ID: unique tree identifier
  - Stem_ID: unique stem identifier within the dataset
  - diameter_at_root_collar_wet (cm): stem diameter at root collar in the field (wet wood)
  - diameter_at_root_collar_dry (cm): stem diameter at root collar in the laboratory (dried disks)
  - basal_area_from_image (cm^2): basal area from image analysis of dried disks
  - sapwood_area (cm^2): sapwood area from image analysis
  - Canopy_area_CA1 (m^2): canopy area measured as polygon area from manually digitized canopy outlines
  - a (m): widest canopy diameter
  - b (m): canopy diameter perpendicular to a
  - Canopy_area_CA2 (m^2): canopy area calculated from ellipse constrained by a and b
  - max_tree_height (m): maximum height of the tree canopy

- tree_level_data.csv
  - Tree_ID: unique tree identifier
  - wet_mass_of_<3cm (kg): wet mass of component < 3 cm diameter
  - wet_mass_of_>3cm (kg): wet mass of component > 3 cm diameter
  - wet_mass_total (kg): total wet mass per tree
  - water_content_<3cm (proportion): water content of <3 cm component
  - water_content_>3cm (proportion): water content of >3 cm component
  - water_content_total (proportion): weighted average water content for the entire tree
  - dry_mass_<3cm (kg): dry mass of <3 cm component
  - dry_mass_>3cm (kg): dry mass of >3 cm component
  - dry_mass_total (kg): total dry mass per tree
  - stem_number (count): number of stems observed at the root collar
  - Equivalent_stem_diameter_wet (cm): whole-tree equivalent stem diameter for fresh stems
  - Equivalent_stem_diameter_dry (cm): whole-tree equivalent stem diameter for dried stems
  - Basal_area_from_wet_diameter (cm^2): basal area calculated from wet diameter
  - Basal_area_from_dry_diameter (cm^2): basal area calculated from dry diameter
  - Basal_area_from_image_analysis (cm^2): whole-tree basal area from image analysis
  - Sapwood_area (cm^2): whole-tree sapwood area from image analysis
  - Canopy_area_CA1 (m^2): canopy area from polygon digitization
  - a (m): canopy major axis diameter
  - b (m): canopy minor axis diameter
  - Canopy_area_CA2 (m^2): canopy area from ellipse method CA2
  - max_tree_height (m): maximum height of the tree

## Study site and sampling design

- Location: ca. 3 ha juniper-savannah in the Southwestern Tablelands, central New Mexico; 34.429°N, 105.861°W; elevation ~1930 m above sea level.
- Timing: biomass sampling at peak mass in mid-October 2018, with additional stem harvesting in May 2019.
- Species focus: Juniperus monosperma (Oneseed Juniper) with C4 grasses (Bouteloua gracilis) as dominant understory.

## Tree selection and sampling details

- Selected 20 J. monosperma trees representing a range of sizes, prioritizing isolated individuals to avoid canopy interactions.
- To support sapwood-area analysis for larger diameters, an additional 10 large stem cross-sections (IDs labeled 'X') were collected.

## Height and canopy measurements

- Maximum height (H Max) determination:
  - Instrument: RTK-GNSS (GS08Plus) with ~15 mm precision.
  - Method: height difference between the highest point of the plant and a terrain surface interpolated from four corner measurements around each plot.
- Canopy area measurement:
  - Aerial surveys conducted with a DJI Phantom 4 Advanced UAV on 2018-10-06.
  - Flights included nadir imagery (~21 m AGL) and oblique imagery (~20°) at ~25 m AGL; 75% forward/side overlap; at least 34 images per area.
  - Ground control: 13 markers (20 cm × 20 cm), precisely geolocated with RTK-GNSS.
  - Photogrammetry: structure-from-motion using Agisoft PhotoScan; dense point cloud to orthomosaic at 0.01 m resolution.
  - Canopy edges traced manually on the orthomosaic to derive CA1; canopy diameters a (widest) and b (perpendicular) were extracted.
  - CA2 calculated to compare with CA1 using the ellipse-constrained formula CA2 = (π/4) × a × b.

## Biomass and component measurements

- Harvest and separation:
  - Trees felled in Oct 2018; 18 of 20 were harvested for intensive analysis.
  - Biomass separated into:
    - Wood tissue (>3 cm diameter, including bole wood)
    - Leaf/twig tissue (<3 cm diameter)
- Mass and moisture:
  - Wet weights measured within 2 hours of felling.
  - Subsamples weighed, dried at 80°C for ≥93 hours to constant weight to determine water content.
  - Water content calculated on a wet-weight basis; component proportions derived on a dry-weight basis.
- Outputs:
  - Total wet/dry masses per component and totals (per tree).
  - Component-wise and total moisture contents reported.

## Basal and sapwood area measurements

- Root collar diameter (DRC) measurements:
  - Wet measurements in the field for disks > 5 cm; for disks < 5 cm, measurements from two axes were averaged.
  - Dry measurements taken after air-drying disks ≥30 days to minimize cracking.
- Disk processing:
  - 200 disks from 20 trees analyzed; disks dried and prepared to distinguish sapwood-heartwood interfaces.
  - Basal area calculations:
    - ESD (equivalent stem diameter) computed per tree for both wet and dry diameters.
    - Wet and dry basal areas calculated from ESD using BA = π × (ESD/2)^2.
  - Imaging:
    - High-resolution (300 dpi) disk images captured with Nikon D850.
    - Basal area (BA Image) and Sapwood Area (SWA) determined from image analysis in ImageJ, scaled to known lengths, with sapwood-heartwood interface identified visually.
- Outputs:
  - Basal area and sapwood area per disk and per tree (via multiple calculation methods).

## Data quality, processing, and references

- Processing workflow for canopy data:
  - SfM photogrammetry with strict quality controls (image sharpness, tie points, reprojection error filtering).
  - Dense cloud to TIN, height-field model, and orthomosaic exported as GeoTIFF for analysis.
  - Canopy delineation performed by a single operator for consistency.
- Image analysis and measurement tools:
  - ImageJ used for measuring BA and SWA from disk images; calibrated with known lengths.
- References and methodological context:
  - Numerous references detailing canopy measurement, allometry, and disk-based biomass methods (e.g., Cunliffe et al.; Grier et al.; Krofcheck et al.; Tiedemann & Klemmedson; and others).

## Usage and provenance

- This metadata describes both the data structure and the collection/processing methodology to support reuse, validation, and replication.
- Data underpin the allometric analysis in the associated submitted article: Allometric relationships for predicting aboveground biomass and sapwood area of Oneseed Juniper (Juniperus monosperma) trees.
- Full methodological details and rationale are described in the accompanying article referenced within the metadata.