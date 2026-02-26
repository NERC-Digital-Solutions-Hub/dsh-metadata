# Supporting documentation for Sample_list.csv

- Purpose and scope
  - Defines the fields and metadata for the Sample_list.csv dataset to enable traceability, discovery, and reuse.
  - Supports data exploration, combination with other datasets, and creation of data products (dashboards, reports, maps).

- Field definitions
  - Sample_Code
    - Explanation: Unique sample identifier.
    - Units: n/a
    - Notes: .
  - RAP
    - Explanation: ICRP Reference Animals and Plant (RAP) into which the sampled species can be attributed.
    - Units: n/a
    - Notes: .
  - Sample_Description
    - Explanation: Part of the organism analysed (e.g., where whole organism was divided and analysed separately).
    - Units: n/a
    - Notes: .
  - Collection_Date
    - Explanation: Date of sample collection.
    - Units: dd-mmm-yy
    - Notes: .
  - Dry/Fresh_Ratio
    - Explanation: Dry to fresh weight ratio.
    - Units: unitless
    - Notes: .
  - Coordinates_of_the_Sample
    - Explanation: Grid reference of sampling location.
    - Units: decimal degrees and minutes
    - Notes: .
  - Sample_Association
    - Explanation: Unique sample identifier of soil which was sampled at the same site.
    - Units: n/a
    - Notes: .
  - Notes
    - Explanation: Additional comments (where applicable).
    - Units: n/a
    - Notes: .

- Data types, units and formatting considerations
  - Collection_Date uses a date format (dd-mmm-yy) that should be consistently parsed.
  - Coordinates_of_the_Sample uses decimal degrees and minutes; consider standardizing to decimal degrees for mapping.
  - Dry/Fresh_Ratio is unitless; ensure consistent calculation/measurement across samples.
  - Sample_Association links samples collected at the same site; ensure referential integrity if linking to other datasets.

- Data quality and challenges
  - Potentially patchy data fields or missing values (e.g., Notes may be blank).
  - Variability in data formats across related datasets; need harmonization when merging.
  - Coordinates may require conversion or validation to ensure accurate mapping.
  - Ensuring RAP, Sample_Description, and other descriptive fields remain consistent across records.

- How this supports data exploration and reuse
  - Provides clear definitions and expected formats to aid data discovery and self-service analysis.
  - Enables joins with other data (e.g., location data, organism taxonomy) using Sample_Code, RAP, or Sample_Association.
  - Facilitates creation of dashboards and reports by exposing key dimensions: RAP groups, collection dates, sample descriptions, and geospatial locations.

- Practical guidance for end users
  - Use Sample_Code as the primary key when linking to raw measurements or analyses.
  - Map Coordinates_of_the_Sample to visualize sampling locations; convert if needed to the preferred coordinate system.
  - Group or filter by RAP to analyze patterns across reference animal/plant categories.
  - Use Collection_Date to track sampling time trends and align with other time-series data.
  - Inspect Sample_Association to aggregate or compare related soil samples from the same site.
  - Refer to Notes for any context that may affect interpretation or data quality.