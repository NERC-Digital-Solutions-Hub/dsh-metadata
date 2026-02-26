# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Describes the sampling scheme (Voronoi) and the field-collected data around root measurements.
- Associated with ESPA programme and P4GES project.
- DOI provided for dataset: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- References a manual for further context (Manual_2_Belowground_Root_Survey, page 9, section 2.3.1, c).

## Governance and provenance
- Dataset scope and method: Root measurements collected via a direct Voronoi-based sampling scheme.
- Spatial context: Zone of Interest (ZOI) with categorical units (ZOI2: Andasibe; ZOI3: Anjahamana).
- Location descriptors: Location (text), Site_Id (site code), Local_name (vernacular species name).
- Data ownership and attribution: clear authorship via ESPA/P4GES framework; DOI enables citation and discovery.
- Update and sharing: references to uploading to portals and catalogues; emphasizes governance around updates and sharing limitations.

## Dataset scope and sampling scheme
- Structural metadata for plan and execution of sampling: sampling points, target trees, Voronoi triangle selection (Code_voronoi, Position_slope).
- Tree targeting and typology: Diameter_class categories (Large >20 cm; 20 cm > Medium > 10 cm; 10 cm > Small) with corresponding Diameter values.
- Tree and site coding: Code_target_tree, Code_site, and mappings to species/local names.

## Metadata and data structure (key variables)
- High-level groupings:
  - ZOI, Location, Site_Id, Local_name, Code_target_tree, Code_voronoi, Position_slope.
  - Diameter_class and Diameter (numeric) with associated units.
- Root and soil measurements by depth:
  - Fine roots (FR): Total_Fresh_weight_FR0_10, Sample_Fresh_weight_FR0_10, Sample_Dry_weight_FR0_10; Total_Fresh_weight_FR10_30, Sample_Fresh_weight_FR10_30, Sample_Dry_weight_FR10_30; Total_Fresh_weight_FR30_50, Sample_Fresh_weight_FR30_50, Sample_Dry_weight_FR30_50.
  - Medium roots (MR): analogous sets for 0-10, 10-30, 30-50 cm.
  - Coarse roots (CR): Total_fresh_weight_CR_t0_10, Sample_fresh_weight_CR_t0_10, Sample_Dry_weight_CR_t0_10; ..._t10_30; ..._t30_50; and neighboring trees (CR_o_*), with similar sub-variables.
  - Coarse target and neighboring tree distinctions include several prefixes: t (target), o (neighbouring), with depth ranges 0-10, 10-30, 30-50 cm.
- Litter and mat root measurements:
  - Thickness_leaf_litter (cm), Fresh total weight of leaf litter, Leaf_litter_sample_dry_weight, Leaf_litter_sample_fresh_weight.
  - Thickness_mat_root (cm), Fresh total weight of mat root, Mat_root_sample_dry_weight, Mat_root_sample_fresh_weight.
- Depth and units:
  - Depth ranges specified as 0-10 cm, 10-30 cm, 30-50 cm for weight-based measurements (grams).
  - Thickness values in centimeters; weights in grams.
- Data quality notes within the header:
  - Some descriptions contain typos or incomplete phrases (e.g., inconsistent use of units like G vs g; truncated phrases in a few fields), indicating potential data quality issues that require harmonization.

## Data quality and limitations
- Mixed and sometimes inconsistent descriptions suggest the need for metadata cleaning and unit harmonization.
- Several fields appear truncated or contain typographical errors; careful curation is required to ensure dataset integrity.
- Wide range of related variables (multiple root types, depth intervals, and related litter/mat measurements) necessitates thorough validation and consistent naming conventions.

## Data sharing, discovery, and usage
- DOI and explicit instruction to upload to relevant data portals/catalogues support discoverability and reuse.
- Clear attribution and acknowledgment requirements for derivatives.
- Emphasizes documenting work performed on datasets to support provenance and reuse.

## Practical considerations for Data Stewards
- Ensure metadata completeness: verify all variable definitions, units, and permissible values (especially ZOI, Diameter_class, and depth ranges).
- Standardize units and naming conventions across FR/MR/CR groups and their depth-specific fields.
- Resolve inconsistencies and incomplete field descriptions to improve interoperability with other datasets.
- Maintain versioning and update processes for the Voronoi-based sampling data and associated measurements.
- Align data with governance policies on data sharing, embargoes, and user needs, while supporting dataset discoverability and usability for downstream researchers.