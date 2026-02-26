# Metadata for 6_Ivankov_background_radiation.csv

- Purpose of the dataset
  - Metadata describes a dataset of background radiation measurements at Ivankov, including geolocation, measurement types, and dose-rate readings at two heights.

- Key fields and what they mean
  - latitude: Location latitude in decimal degrees; uses WGS-84; GPS accuracy stated as 10 m or less; notes reference Garmin GPSmap 78S.
  - longitude: Location longitude in decimal degrees; same GPS/coordinate system and accuracy notes as latitude.
  - Analysis_type_1_or_2: Indicates site role
    - 1 = site for both dose measurement and soil sampling
    - 2 = only dose measurement
  - at_0.1m: Ambient equivalent dose rate at height 0.1 meters above ground; measured with certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
  - at_1m: Ambient equivalent dose rate at height 1 meter above ground; measured with the same type of dosimeters.
  - Sampling_site_description: Habitat type for each site; notes that seven sites were inaccessible, but locations are retained for completeness.
  - Notes and methodology fields: Some fields show "n/a" or explanatory notes; Notes mention specific equipment and system details.

- Data collection context
  - Measurements taken at two heights to assess ambient dose rates.
  - Dosimeters used are certified gamma-beta irradiation devices (RKS-01, Stora-TU, Ukraine).
  - Site descriptions provide habitat context; GPS metadata aims to document precise locations, with acknowledgement of potential accessibility issues.

- Data quality, completeness, and gaps
  - GPS accuracy documented (10 m or less), but some site access notes indicate incomplete field collection.
  - Several fields contain "n/a" placeholders, indicating missing or not applicable data in certain columns.
  - Inaccessible sites noted, which could affect dataset completeness and representativeness.

- Access, discoverability, and governance considerations
  - Metadata explicitly links locations, site roles, measurement heights, and device types, supporting data discovery and reuse.
  - Clear provenance through equipment and methodology notes aids data quality assessment and potential replication.
  - For Data Leaders: ensure consistent unit usage, fill in gaps where possible, document data provenance, and consider coordinating with related datasets to address accessibility gaps and standardize metadata across collections.