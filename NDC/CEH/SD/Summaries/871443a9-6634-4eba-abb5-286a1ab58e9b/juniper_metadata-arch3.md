# Field measurements of aboveground biomass, canopy area, stem diameter and sapwood area of Juniperus monosperma trees in New Mexico, collected in 2018 and 2019

## Purpose and scope
- Metadata accompanying a dataset used to develop allometric relationships for predicting aboveground biomass and sapwood area of Oneseed Juniper (Juniperus monosperma).
- Data collected in a roughly 3-hectare juniper-savannah in central New Mexico (34.429°N, 105.861°W; ~1930 m above sea level).
- Biomass sampling conducted in October 2018 with additional stem harvesting in May 2019.

## Study design and sampling
- 20 J. monosperma trees selected for intensive analysis; emphasis on isolated trees; included 10 additional large stem cross-sections (IDs ‘X’) for larger diameters.
- Height (maximum plant height) measured using RTK-GNSS with ~15 mm precision; height derived from elevation difference between the tallest point and a terrain surface interpolated from four corner measurements.
- Canopy area surveyed with a UAV (DJI Phantom 4 Advanced) on 2018-10-06, with nadir and oblique flights, ground control markers, and structure-from-motion processing to produce an orthomosaic (0.01 m resolution) for canopy delineation.
- 13 ground control markers used for geolocation; photogrammetry workflow included dense point cloud generation, TIN creation, and height-field interpolation.

## Biomass and component measurements
- Harvesting of 18 of the 20 selected trees (two harvesting constraints prevented two trees from being collected).
- Biomass separated into two components: (i) wood tissue (>3 cm diameter) and (ii) leaf/twig tissue (<3 cm diameter).
- Wet weights measured within 2 hours of felling; subsamples weighed and oven-dried at 80°C to constant weight to determine moisture content; moisture content used to convert wet mass to dry mass; component proportions calculated on a dry-weight basis.

## Canopy area and height details
- Canopy area CA1 derived from manual digitisation of polygon edges on the orthomosaic (GIS-based).
- Canopy geometry also quantified as an ellipse using a and b, yielding CA2 = π/4 * a * b.
- Maximum canopy height recorded as part of the UAV-derived data (max_tree_height).

## Basal and sapwood area measurements
- Root collar diameter (DRC) measured in the field for disks >5 cm; for disks <5 cm, measurements from major/minor axes averaged.
- 200 disk cross-sections collected from 20 trees; disks air-dried for ≥30 days and re-measured to determine DRC Dry.
- Equivalent stem diameter (ESD) calculated for wet and dry conditions from the root collar diameters of all stems per tree.
- Basal area (BA) computed from wet and dry ESDs using BA = π*(ESD/2)^2.
- High-resolution images (300 dpi) of disks captured; basal area (BA_Image) and sapwood area (SWA) measured via ImageJ, using scale information and distinguishing sapwood-heartwood interfaces; results aggregated to a whole-tree basis.

## Data files and key variables
- all_stems.csv: per-disk measurements including
  - Tree_ID, Stem_ID; diameter_at_root_collar_wet/dry; basal_area_from_image; sapwood_area; canopy_area_CA1; canopy diameters a and b; max_tree_height; equivalent stem diameters; basal areas from wet/dry diameters and image analysis; Canopy_area_CA2; Canopy_area_max; and related fields.
- tree_level_data.csv: per-tree measurements including
  - Tree_ID; wet_mass_of_<3cm, wet_mass_of_>3cm, wet_mass_total; water_content_<3cm, water_content_>3cm, water_content_total; dry_mass_<3cm, dry_mass_>3cm, dry_mass_total; stem_number; Equivalent_stem_diameter_wet/dry; Basal_area_from_wet_diameter; Basal_area_from_dry_diameter; Basal_area_from_image_analysis; Sapwood_area; Canopy_area_CA1; a (max canopy diameter); b (perpendicular canopy diameter); CA2; max_tree_height.

## Methods and data processing
- Field measurements followed established protocols; root collar diameter conversions and allometric calculations derived from referenced methods (e.g., ESD-based basal area, wet/dry mass conversions based on moisture content).
- UAV photogrammetry workflow included strict quality controls: calibration with ground control markers, high-quality camera settings, dense point cloud generation, and orthomosaic export for subsequent GIS analysis.
- Image analysis for basal and sapwood areas conducted in ImageJ with calibration against known lengths.

## Study site context and limitations
- Site features: juniper savannah with co-dominant Bouteloua gracilis; low-relief topography enabling reliable terrain height interpolation.
- Limitations: only 18 of 20 targeted trees harvested; study area limited to ~3 ha; canopy area estimates include both polygon-based (CA1) and ellipse-based (CA2) approaches to assess methodological consistency.

## Data quality, governance, and references
- Metadata provide explicit variable definitions, units, and data provenance to support reproducibility and reuse.
- References accompany the work, detailing methods for canopy measurement, biomass estimation, and related allometric frameworks (e.g., Cunliffe et al., 2016–2019; Krofcheck et al., 2016; others).

## Potential applications for monitoring frameworks
- Enables development and validation of allometric models for Juniperus monosperma biomass and sapwood area.
- Supports cross-validation of remote-sensing-derived canopy metrics (CA1 and CA2) against ground-truth measurements.
- Provides a well-documented data infrastructure, including metadata and data processing steps, to overcome data gaps and facilitate governance and sharing in environmental monitoring programs.