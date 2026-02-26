# DATA HEADER INFORMATION for Site_description_and_location_of_direct_measured_trees.csv

- Overview
  - The dataset records characteristics of the target tree environment.
  - Related documentation: Manual_2_Below_Ground_Root_Survey.
  - DOI: https://doi.org/10.5285/ a242e145-21f6-4c3c-b8e4-adce70e50d85
  - Programme and project: ESPA (programme) and P4GES (project).

- Provenance and acknowledgments
  - Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

- Dataset and usage context
  - Captures environmental characteristics around each target tree site (geography, tree properties, and positional data).
  - Data can be used to explore relationships between location, tree size class, and environmental factors.

- Core dataset structure
  - ZOI (Zone of Interest)
    - Information: Zone identifiers (ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy)
    - Type: Categorical
    - Field and resources: botanist
  - Location
    - Information: Name of village where the target tree was collected
    - Type: Text string
  - Code_Site
    - Information: Code assigned to the site
    - Type: Text string
  - Species
    - Information: Local name of species
    - Type: Text string
  - Code_target_tree
    - Information: Code for each target tree; links to site, species, and diameter class
    - Type: Text string
  - Diameter class
    - Information: Size class of tree
    - Type: Categorical
    - Classes: L (Large, DBH > 20 cm), M (Medium, 10 cm < DBH < 20 cm), S (Small, 5 cm < DBH < 10 cm)
  - Longitude
    - Information: GPS longitude (WGS84)
    - Type: Numeric
    - Unit: Decimal degrees
  - Latitude
    - Information: GPS latitude (WGS84)
    - Type: Numeric
    - Unit: Decimal degrees
  - Altitude
    - Information: Ellipsoidal height of the tree
    - Type: Numeric
    - Unit: Meter
    - Field and resources: GPS eTrex 30 Garmin
  - Slope
    - Information: Slope for each target tree
    - Type: Numeric
    - Unit: Degree

- Data notes and references
  - Location data, coordinate references, and field methods are described in the header.
  - Cross-reference with Manual_2_Below_Ground_Root_Survey for related measurements.