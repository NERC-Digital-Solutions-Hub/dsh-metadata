# Metadata for 6_Ivankov_background_radiation.csv

- Purpose and scope
  - Describes metadata for the 6_Ivankov_background_radiation.csv dataset.
  - Captures sampling site location, measurement type, and dose-rate readings at two heights (0.1 m and 1 m) using specified dosimeters.
  - Notes that seven sites were inaccessible but their locations are retained for completeness.

- Data fields and definitions
  - latitude
    - Explanation: Location of sampling site.
    - Units/Methodology: Decimal degrees; WGS-84; accuracy ≤ 10 m.
    - Notes: GPS-receiver (Garmin, GPSmap 78S) using WGS-84 with accuracy ≤ 10 m.
  - longitude
    - Explanation: Location of sampling site.
    - Units/Methodology: Decimal degrees; WGS-84; accuracy ≤ 10 m.
    - Notes: GPS-receiver (Garmin, GPSmap 78S) using WGS-84 with accuracy ≤ 10 m.
  - Analysis_type_1_or_2
    - Explanation: 1 or 2 indicates measurement scope.
    - Units/Methodology: n/a.
    - Notes: 1 = site for dose measurement and soil sampling; 2 = only dose measured.
  - at_0.1m
    - Explanation: Ambient equivalent dose rate at height 0.1 m above ground.
    - Units/Methodology: n/a.
    - Notes: Measured with certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
  - at_1m
    - Explanation: Ambient equivalent dose rate at height 1 m above ground.
    - Units/Methodology: n/a.
    - Notes: Measured with certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
  - Sampling_site_descriptio n
    - Explanation: Habitat type at the sampling site.
    - Units/Methodology: n/a.
    - Notes: Seven sites were inaccessible; locations retained in data for completeness.

- Provenance and data quality
  - Data are tied to geographic coordinates using the WGS-84 system with stated accuracy.
  - Instrumentation specified (RKS-01 dosimeters) for dose-rate measurements.
  - A potential metadata naming irregularity is present (Sampling_site_descriptio n) indicating a need for normalization.
  - The dataset records both presence/absence of site access and completeness of site descriptions.

- Access, sharing, and governance
  - Metadata should accompany the dataset when uploading to portals and catalogues to support discoverability and reuse.
  - Ensure consistent field naming, units, and methodology descriptions across related datasets.
  - Document any data limitations (e.g., inaccessible sites) and their impact on analyses.

- Data challenges and considerations for Data Stewards
  - Incomplete picture of site accessibility and its effect on temporal updates or replication.
  - Handling multiple systems/formats and potential non-interoperable records across datasets.
  - Ensuring timely updates and synchronization of site descriptions and measurement records.

- Recommendations for Data Stewards
  - Standardize field names (e.g., Sampling_site_description) and correct any typographical inconsistencies.
  - Validate coordinates against GPS data and confirm WGS-84 usage with ≤10 m accuracy.
  - Clarify and document Analysis_type_1_or_2 coding in a data dictionary.
  - Maintain a clear record of inaccessible sites and rationale, while preserving their coordinates for completeness.
  - Include metadata provenance, measurement dates, and any data embargo or sharing restrictions in the dataset metadata.