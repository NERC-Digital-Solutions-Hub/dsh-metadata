# Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019

## Purpose and data context
- Provides metadata accompanying the dataset on field measurements of Juniperus monosperma in New Mexico (2018–2019).
- Underpins the analysis of allometric relationships for predicting aboveground biomass and sapwood area; see the referenced article for comprehensive methods.

## Data content and parameter descriptions
- all_stems.csv
  - Key fields include:
    - Tree_ID: unique tree identifier
    - Stem_ID: unique stem identifier
    - diameter_at_root_collar_wet: wet stem diameter at root collar (cm)
    - diameter_at_root_collar_dry: dry stem diameter at root collar after drying (cm)
    - basal_area_from_image: basal area from image analysis (cm^2)
    - sapwood_area: sapwood area from image analysis (cm^2)
    - canopy_area_CA1: manually digitised canopy area (m^2)
    - a, b: canopy diameters at the widest point and perpendicular (m)
    - max_tree_height: maximum tree height (m)
- tree_level_data.csv
  - Key fields include:
    - Tree_ID
    - wet_mass_of_<3cm, wet_mass_of_>3cm: wet mass of subcomponents (kg)
    - wet_mass_total: total wet mass (kg)
    - water_content_<3cm, water_content_>3cm, water_content_total: moisture contents (proportions)
    - dry_mass_<3cm, dry_mass_>3cm, dry_mass_total: dry masses (kg)
    - stem_number: number of stems observed at the root collar
    - Equivalent_stem_diameter_wet/dry: whole-tree equivalent stem diameter (cm)
    - Basal_area_from_wet_diameter/dry_diameter: basal area from corresponding diameters (cm^2)
    - Basal_area_from_image_analysis: whole-tree basal area from image analysis (cm^2)
    - Canopy_area_CA1, Canopy_area_CA2: canopy areas derived from polygon and ellipse methods (m^2)
    - max_tree_height: maximum canopy height (m)

## Study site
- Location: ~3 ha juniper-savannah in southwestern Tablelands, central New Mexico.
- Coordinates: 34.429°N, 105.861°W; elevation ~1930 m above sea level.
- Vegetation context: Juniperus monosperma with Bouteloua gracilis (Blue Grama) as dominant grass.
- Timing: biomass sampling in mid-October 2018; additional stem harvesting in May 2019.

## Tree selection and sampling design
- Selected 20 J. monosperma trees representing size distribution near a flux tower; emphasis on isolated trees.
- An additional 10 large stem cross-sections (20–30 cm diameter) collected to supplement sapwood area analysis (denoted as stem IDs 'X').

## Measurements and methods

### Maximum plant height
- Height measured with RTK-GNSS (GS08Plus) at four corner points around each harvest plot.
- Precision ~15 mm; H Max = height difference between plant peak and interpolated terrain surface.

### Canopy area
- UAV-based survey on 2018-10-06 using DJI Phantom 4 Advanced.
- Two flight geometries: nadir and oblique (~20°) at ~21–25 m above ground.
- Ground control: 13 markers; RTK-GNSS geolocation.
- Processing: structure-from-motion in Agisoft PhotoScan v1.4.3; dense cloud and TIN for orthomosaic at 0.01 m resolution.
- GIS work: canopy edges manually digitised to obtain Canopy_area_CA1 (m^2); canopy diameters a and b extracted.
- Canopy_area_CA2 computed as an ellipse-based estimate: CA2 = π/4 × (a × b).

## Biomass measurements
- Harvest: two days in Oct 2018; 18 trees successfully harvested.
- Tissue separation: wood (>3 cm diameter) and leaf/twig (<3 cm).
- Wet weights measured within 2 hours; sub-samples dried at 80°C for ≥93 hours to constant mass.
- Water content calculated on a green weight basis; used to convert wet to dry mass; component proportions reported on a dry-weight basis.

## Basal and sapwood area measurements
- Root collar diameter (DRC) defined as the lowest point of primary branching.
- Wet DRC measured in the field for >5 cm disks; for <5 cm disks, average of major/minor axes via calipers.
- 200 disks from 20 trees; air-dried ≥30 days; re-measured for DRC Dry.
- Equivalent stem diameter (ESD) calculated as sqrt(sum of squared DRCs) for both wet and dry measurements.
- Basal area calculations:
  - BA_wet = π × (ESD_wet / 2)^2
  - BA_dry = π × (ESD_dry / 2)^2
- Image-based measurements:
  - Basal_area_from_image and Sapwood_area per disk measured with ImageJ from high-resolution (300 DPI) disk images.
  - Images scaled using known lengths; sapwood-heartwood interface visually distinguished.
  - Whole-tree Basal_area_from_image_analysis and Sapwood_area derived per tree.

## Data processing and quality assurance
- UAV workflow and data quality controls detailed (sharpness ≥ 0.84; marker accuracy; bundle adjustment; dense cloud filtering).
- Canopy delineation performed by a single operator for consistency.
- Standardized protocols and software versions documented (Agisoft PhotoScan v1.4.3; ESRI ArcPro v2.1.3; ImageJ referenced).

## References and methodological background
- Key references detailing canopy measurement protocols, allometry, and related biomass methods cited (e.g., Cunliffe et al.; Grier et al.; Krofcheck et al.; Schneider et al.; Tiedemann & Klemmedson; Ansley et al.; Chojnacky & Rogers).

## Practical GIS usage notes
- Data enable spatially explicit biomass, canopy area, and sapwood area mapping at both disk and tree scales.
- Compatible with GIS workflows for area-based biomass estimation, allometric model validation, and cross-scale integration (in-field measurements, disk-level, and tree-level aggregates).
- Metadata supports reproducibility and cross-dataset integration with similar juniper biomass studies.