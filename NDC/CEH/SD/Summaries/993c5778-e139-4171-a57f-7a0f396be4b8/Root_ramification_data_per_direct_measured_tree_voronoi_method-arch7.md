# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv Please also see Manual_2_Belowground_Root_Survey, page 10.

## Overview
- Records the target tree root architecture: for each target tree, each coarse root (up to 1 cm diameter) branching was tagged and measured.

## Provenance and references
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA; Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Spatial and tabular schema (data fields)
- ZOI (Zone of Interest)
  - Information: Zone of Interest
  - Variable Type: Categorical
  - Unit: ZOI2: Andasibe / ZOI3: Anjahamana
- Site
  - Information: Code given to the site where the sample was collected
  - Variable Type: Text string
  - Unit: .
- Local name
  - Information: Vernacular/local name of the inventoried species
  - Variable Type: Text string
  - Unit: .
- DBH Class
  - Information: Diameter at Breast Height (1.3 m)
  - Variable Type: Categorical
  - Unit: L: Large / M: Medium / S: Small
- Code_target_tree
  - Information: Code given to each target tree (Code_site + species name + diameter class)
  - Variable Type: Text String
  - Unit: .
- Number of ramification
  - Information: Number of ramification from the north
  - Variable Type: Numeric
  - Unit: .
- DiH
  - Information: Horizontal diameter beginning of each ramification (cm)
  - Variable Type: Numeric
  - Unit: Centimeter
- DiV
  - Information: Vertical diameter beginning of each ramification (cm)
  - Variable Type: Numeric
  - Unit: Centimeter
- DfV
  - Information: Vertical diameter ending of each ramification (cm)
  - Variable Type: Numeric
  - Unit: Centimeter
- DfH
  - Information: Horizontal diameter ending of each ramification (cm)
  - Variable Type: Numeric
  - Unit: Centimeter
- DfM
  - Information: Mean of diameter ending of each ramification (DfH and DfV) [DfM = (DfH+DfV)/2]
  - Variable Type: Numeric
  - Unit: Centimeter
- Total_weight
  - Information: Weight of each ramification
  - Variable Type: Numeric
  - Unit: grams (g)
- Total_length
  - Information: Length of each ramification
  - Variable Type: Numeric
  - Unit: Centimeter
- Orientation
  - Information: Directional movement of each branch
  - Variable Type: Categorical
  - Unit: N, S, E, W; PV (taproot), NA (not available)
  - Notes: PV indicates a vertical taproot; Vor indicates ramification from the Voronoi triangle where roots were excavated
- Vor
  - Orientation indicator
  - Variable Type: Categorical
  - Unit: N/A
  - Notes: Vor = ramification from the Voronoi triangle; PV = taproot; NA = not available

## GIS and data use considerations
- Purpose: Facilitates map-based visualization and spatial analysis of root architectures across sites (Andasibe, Anjahamana) by linking ramification metrics to target trees.
- Data integration: Likely requires joining by Site and Code_target_tree; may require additional geospatial coordinates or Voronoi polygon affiliations for spatial mapping.
- Data quality: Data may come from multiple sources with variable resolutions; standardization of fields (e.g., units, categorical classes) recommended before GIS integration.
- Method context: Data collected using Voronoi-based excavation approach; orientation helps spatial interpretation (N/S/E/W, with PV for taproot).

## Usage notes and constraints
- Data derived products require explicit acknowledgement as per the dataset and project guidelines.
- Consistency and complete coverage (e.g., resolution, standard naming) may be variable; plan for cleaning and transformation in GIS workflows.