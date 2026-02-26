# DATA HEADER INFORMATION for Site_description_and_location_of_direct_measured_trees.csv

## Overview
- Dataset records characteristics of the target tree environment.
- Part of ESPA Programme and P4GES Project.
- DOI provided for data access: https://doi.org/10.5285/a242e145-21f6-4c3c-b8e4-adce70e50d85
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Cross-reference suggested: Please also see Manual_2_Below_Ground_Root_Survey.

## Context and Provenance
- Focus: direct measurements of environmental context around target trees.
- Zone of Interest (ZOI) categories used to designate study areas: ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy.
- Field data collected by botanist; location details and site codes accompany each observation.
- GPS-based positioning and elevation data collected with standard equipment (WGS84 coordinates; ellipsoidal height).

## Key fields and definitions
- ZOI
  - Information: Zone of Interest
  - Variable Type: Categorical
  - Examples: ZOI1: Lakato; ZOI2: Andasibe; ZOI3: Anjahamana; ZOI4: Didy
- Location
  - Information: Name of village where the target tree was collected
  - Variable Type: Text String
- Code_Site
  - Information: Code given to the site where the target tree was collected
  - Variable Type: Text String
- Species
  - Information: Local name of species
  - Variable Type: Text String
- Code_target_tree
  - Information: Code given to each target tree (associated with site, species, and diameter class)
  - Variable Type: Text String
- Diameter class
  - Information: Diameter class categories
  - Variable Type: Categorical
  - Definition: L = Large (DBH > 20 cm); M = Medium (10 cm < DBH < 20 cm); S = Small (5 cm < DBH < 10 cm)
- Longitude
  - Information: Longitude of each site (GPS coordinates)
  - Variable Type: Numeric
  - Unit: decimal degree (WGS84)
- Latitude
  - Information: Latitude of each site (GPS coordinates)
  - Variable Type: Numeric
  - Unit: decimal degree (WGS84)
- Altitude
  - Information: Ellipsoidal height of the tree
  - Variable Type: Numeric
  - Unit: Meter
  - Field/source: GPS eTrex 30 Garmin
- Slope
  - Information: Slope for each target tree
  - Variable Type: Numeric
  - Unit: Degree

## Data quality, metadata and documentation
- Metadata includes explicit units, coordinate reference system (WGS84), and platform used for measurements.
- Encourages linkage to additional related datasets (e.g., below-ground root survey documented in Manual_2_Below_Ground_Root_Survey).
- Clear coding for site, target trees, and diameter classes supports reproducibility and cross-dataset integration.

## Data governance and usage notes
- Data use requires acknowledgement of the data originators and project context (as specified).
- DOI and project information facilitate data discovery and provenance tracking.
- Cross-border and cross-project data sharing considerations implied by the need to acknowledge originators and the presence of standardized metadata fields.

## Implications for monitoring frameworks
- Demonstrates a structured approach to metadata for environmental health indicators:
  - Standardized zone identifiers (ZOI)
  - Clear spatial (Longitude/Latitude/Altitude) and biometric (Diameter class) fields
  - Linkage between site, species, and individual trees via codes
  - Explicit units and coordinate reference systems
- Supports transparent data governance, data provenance, and reproducibility in monitoring reports and dashboards.
- Highlights the need for complementary datasets (e.g., root surveys) to provide a fuller environmental context.

## Practical considerations for reuse
- Ensure metadata completeness when integrating with other datasets (e.g., confirm ZOI codes, species local names).
- Maintain data sharing compliance and proper acknowledgements as per the dataset’s requirements.
- Verify cross-reference documents (Manual_2_Below_Ground_Root_Survey) for integrated analyses.