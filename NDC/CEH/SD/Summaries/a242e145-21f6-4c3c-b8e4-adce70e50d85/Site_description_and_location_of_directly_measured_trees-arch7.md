# DATA HEADER INFORMATION for Site_description_and_location_of_direct_measured_trees.csv

## Overview
- Metadata describing the characteristics of the target tree environment recorded in the csv dataset.
- Related material: Manual_2_Below_Ground_Root_Survey.
- DOI: https://doi.org/10.5285/ a242e145-21f6-4c3c-b8e4-adce70e50d85
- Programme: ESPA; Project: P4GES.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Data are organized around the Zone of Interest (ZOI), site codes, species, and target-tree codes, with geospatial coordinates and environmental descriptors.

## Data scope and purpose
- Records information on the characteristics of the target tree environment, including spatial location, site coding, species, and diameter class.
- Designed to support GIS-based mapping and analysis of tree environments across multiple sites and zones.

## Related documentation
- See also Manual_2_Below_Ground_Root_Survey for related methods or data context.

## Key fields and their meaning
- ZOI (Zone of Interest)
  - Information: Zone of Interest category.
  - Variable Type: Categorical.
  - Unit: ZOI1: Lakato / ZOI2: Andasibe / ZOI3: Anjahamana / ZOI4: Didy.
  - Field and materials resources: botanist.
- Location
  - Information: Name of village where the target tree was collected.
  - Variable Type: Text string.
- Code_Site
  - Information: Code for the site where the target tree was collected.
  - Variable Type: Text String.
- Species
  - Information: Local name of the species.
  - Variable Type: Text String.
- Code_target_tree
  - Information: Code for each target tree; links to the Code_site, species, and diameter class.
  - Variable Type: Text String.
- Diameter class
  - Information: Three classes: L (Large DBH > 20 cm), M (Medium 10 < DBH < 20 cm), S (Small 5 < DBH < 10 cm).
  - Variable Type: Categorical.
  - Unit: L: Large / M: Medium / S: Small.
- Longitude
  - Information: Longitude of each site.
  - Variable Type: Numeric.
  - Unit: decimal degree (WGS84).
- Latitude
  - Information: Latitude of each site.
  - Variable Type: Numeric.
  - Unit: decimal degree (WGS84).
- Altitude
  - Information: Ellipsoidal height of the tree.
  - Variable Type: Numeric.
  - Unit: Meter.
  - Field and materials resources: GPS eTrex 30 Garmin.
- Slope
  - Information: Slope for each target tree.
  - Variable Type: Numeric.
  - Unit: Degree.

## Data provenance, standards, and usage
- Data are collected in field conditions with noted units and coordinate reference (WGS84) to support spatial analyses.
- The dataset is part of an ecosystem monitoring context (ESP A / P4GES) and should be used in alignment with project metadata and related manuals.
- Data quality considerations (implicit in the related documentation) emphasize data cleaning, validation, and consistent data standards when combining across sites.

## Usage notes and acknowledgments
- Acknowledgement is required for products derived from these data to the Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Related program and project documentation provide context for data collection methods and intended analyses.

## Related resources
- DOI and project pages:
  - DOI: https://doi.org/10.5285/ a242e145-21f6-4c3c-b8e4-adce70e50d85
  - ESPA programme and P4GES project pages.