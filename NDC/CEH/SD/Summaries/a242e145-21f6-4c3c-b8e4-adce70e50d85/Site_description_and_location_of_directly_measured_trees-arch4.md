# DATA HEADER INFORMATION for Site_description_and_location_of_direct_measured_trees.csv

- Overview
  - Records characteristics of the target tree environment, focusing on site description and location for measured trees.
  - Cross-referenced with Manual_2_Below_Ground_Root_Survey.
  - DOI provided for dataset access and citation.
  - Programme ESPA and Project P4GES context; acknowledgement required for products derived from these data.

- Provenance and Acknowledgements
  - Data origin linked to ESPA programme and P4GES project.
  - Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

- Data Model and Fields (structure and types)
  - Zone of Interest (ZOI)
    - Information: Zone category (Categorical)
    - Levels: ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy
    - Unit/Resources: ZOI1–ZOI4; field and materials resource = botanist
  - Location
    - Information: Village name where the target tree was collected (Text)
    - Variable Type/Unit: Text string
  - Code_Site
    - Information: Code identifying the site (Text String)
    - Variable Type/Unit: Text String
  - Species
    - Information: Local name of species (Text)
    - Variable Type/Unit: Text String
  - Code_target_tree
    - Information: Code for each target tree; links to site, species, and diameter class (Text String)
    - Variable Type/Unit: Text String
  - Diameter class
    - Information: Size class based on DBH
    - Variable Type/Unit: Categorical
    - Categories: L (large, DBH > 20 cm), M (medium, 10 < DBH ≤ 20 cm), S (small, 5 < DBH ≤ 10 cm)
  - Longitude
    - Information: GPS longitude (WGS84)
    - Variable Type/Unit: Numeric; Unit = decimal degree; WGS84
  - Latitude
    - Information: GPS latitude (WGS84)
    - Variable Type/Unit: Numeric; Unit = decimal degree; WGS84
  - Altitude
    - Information: Ellipsoidal height of the tree
    - Variable Type/Unit: Numeric; Unit = meters; GPS eTrex 30 Garmin
  - Slope
    - Information: Slope at the target tree site
    - Variable Type/Unit: Numeric; Unit = degrees

- Geospatial and Measurement Details
  - Coordinates provided in decimal degrees (WGS84: 4326)
  - Altitude in meters; Slope in degrees
  - Location and field data capture include village name, site code, species (local names), and a unique target tree code

- Access, Use, and Attribution
  - Dataset has a formal DOI for citation and discovery
  - Acknowledgement requirement for products derived from the data
  - Cross-referenced documentation (Manual_2_Below_Ground_Root_Survey) supports supplementary data context
  - Emphasizes standardized field definitions and units to enable interoperability and reuse

- Relevance for Data Leaders
  - Demonstrates end-to-end data structuring: from site codes, zones of interest, and local species names to precise geospatial coordinates and measurements
  - Clear metadata with explicit units, variable types, and categories to support data quality, discoverability, and reuse
  - Aligns with governance practices: provenance, access constraints, attribution, and cross-dataset interoperability (via DOI and linked materials)
  - Provides a model for capturing data at the system level: location, context, measurement classes, and resource documentation to inform data strategy and user-centric product development