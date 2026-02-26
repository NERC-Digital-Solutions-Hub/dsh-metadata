# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Describes direct field-measurement results for the above-ground biomass pool, including weights, diameters, heights, coordinates, distances, and related metrics.
- Part of the ESPA Programme, P4GES project; dataset intended for analysis of dendrometric characteristics.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Related to Manual 1_Classical_Survey; DOI provided for the dataset.

## Dataset scope and content
- Direct measurements collected during field work focused on above-ground biomass.
- Includes:
  - Site and location identifiers: Site_ID (P4GES WP4 site Code), Location (sampling point name), ZOI (Zone of Interest).
  - Species information: Species_name (vernacular), Scientific_Name.
  - Species/diameter categorization: Diameter_class (Large/L, Medium/M, Small/S).
  - Structural measurements: DBH (Diameter at Breast Height, cm), Height_total (m), H_trunk (m), Total_length (m), Length_trunk (m), Crown_height (m), X/X'/Y/Y' (ground distances related to crown projection and orientation).
  - Diameter metrics at various heights: Basal_diameter, Middle_diameter, Top_diameter (all in cm).
  - Branch and trunk metrics: Nb_main_branches, Total_length, etc.
  - Biomass samples and weights (both dry and fresh): multiple categories such as Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples; Fresh_weight equivalents for basal diameter, branches, DBH, leaf, middle/top trunk, trunk; units include grams (g) and kilograms (kg) as appropriate.
  - Sample descriptors: Information about samples collected at various trunk heights (basal, middle, top), trunk sections, and whole-tree components.
- Measurements are equipped with units and typified data types (Text/String, Numeric, Categoric) per field.

## Key fields and data structure (highlights)
- Identification and location: Site_ID, ZOI, Location, Location Field materials/resources (e.g., botanist, local guides).
- Taxonomic details: Species_name (vernacular), Scientific_Name.
- Size/classification: Diameter_class; DBH (cm); Height_total (m); H_trunk (m); Total_length (m); Length_trunk (m); Crown_height (m); Basal_diameter, Middle_diameter, Top_diameter (cm).
- Spatial descriptors: X, X', Y, Y' (distances related to crown projection; units in meters/decameters as described).
- Tree structure: Nb_main_branches.
- Biomass sampling: multiple Dry_weight_* and Fresh_weight_* fields for various components (basal diameters, branches, DBH, leaf, trunk), including per-sample and total measurements with units like grams and kilograms.
- Data provenance and care: Field materials/resources indicate who collected or contributed to measurements (e.g., forester compass, decameter, botanist).

## Provenance, access, and usage notes
- DOI provided for dataset discovery and citation.
- Project and program references: ESPA (http://www.espa.ac.uk/); P4GES (https://www.p4ges.org).
- Acknowledgement requirement for outputs derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Cross-reference: Please also see Manual 1_Classical_Survey for methodological context.

## Data quality and notes
- Metadata outlines a comprehensive set of dendrometric and biomass-related variables, including both live measurements and sample weights.
- The header information includes a broad range of measurement types and units; some entries indicate multiple fields per measurement (e.g., Dry_weight_of_*_samples with additional numeric indices and scale notes).
- Field resources and equipment are specified, reflecting in-field data collection practices (e.g., forester compass, decameter, botanist, local guides).

## Practical implications for data use (Data Support perspective)
- Enables self-service exploration of above-ground biomass components across multiple zones of interest and species.
- Supports data integration by providing explicit units, field names, and data types to facilitate cleaning and transformation.
- Useful for creating dashboards or reports that summarize tree dimensions, spatial distribution, and biomass allocations by site/zone/species.
- Highlights the need to acknowledge data provenance and consider cross-referencing with Manual 1_Classical_Survey for methodological consistency.