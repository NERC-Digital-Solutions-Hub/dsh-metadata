# Water quality data - work packages 3 and 5

## Overview
- Describes a water quality dataset composed of one main data file (Water_quality_data.csv) and three supporting files (Sampling_sites.csv, Determinand_list.csv, Particulate_matter_method.rtf).
- Documented metadata and methodology pieces are distributed across these files, enabling interpretation and reuse of the dataset.

## Data files and structure
- Water_quality_data.csv
  - Primary data file containing measurements.
  - First five columns: SiteRef, SiteName, Trip, Date, Time.
  - Other columns contain determinand values; all have a qualifier column (often blank, sometimes <).
  - Some values have issues due to instrument problems (notably pH during a period).
  - Blank fields indicate missing data; zeros are actual measured values.
- Sampling_sites.csv
  - SiteName, SiteRef, Type (Fresh or Saline), Sampling (Spot or Continuous), Easting, Northing.
- Determinand_list.csv
  - Provides details for the determinands (parameters measured).
- Particulate_matter_method.rtf
  - Methodology information for the analysis of certain particulates.

## Key variables and data interpretation
- SiteRef: Unique site code; estuarine sites BCN, TYC, DOL noted; others are freshwater.
- SiteName: Unique site name.
- Trip: Indicates field sampling event; can be a single trip or a date range tied to a routine trip; 3-digit code encodes most recent routine trip for intermediate samples; blank means autosampler or manual sampling over one or two days.
- Date and Time: Timestamp of sampling.
- pH data: pHUncorrected column holds original values; qualifier column marks incorrect values (x) during instrument failure periods; corrected values in pH column are approximate and based on alkalinity.
- Data completeness: Missing data indicated by blanks; some variables were not measured for certain samples.

## Data quality and limitations
- Periods with incorrect pH values due to instrument failure (document notes corrective approach).
- Mix of corrected and uncorrected values in the pH data requires careful handling.
- Some samples have missing measurements or were not all variables measured.
- Metadata for explaining each determinand and measurement method is provided externally (Determinant_list and Particulate_matter_method).

## Metadata, methodology, and data governance
- Metadata are distributed across Water_quality_data.csv and Sampling_sites.csv, Determinand_list.csv, and Particulate_matter_method.rtf.
- Methodology for certain particulates is documented in the Particulate_matter_method.rtf.
- Proper use requires consulting Determinand_list.csv for definitions and units of determinands.

## Sampling details and spatial/temporal coverage
- Sampling sites include estuarine (e.g., BCN, TYC, DOL) and freshwater locations.
- Water Type indicates whether samples are Fresh or Saline (tidal influence).
- Sampling method: Spot or Continuous collection; Trip codes link samples to field campaigns.
- Spatial context provided via Easting/Northing (National Grid); enables GIS-based analysis.

## How the data can be used (data products and analyses)
- Assess water quality across estuarine and freshwater sites over time.
- Analyze relationships between determinands and sampling context (site type, tide state).
- Support trend analysis, reporting, and policy-related data products by providing structured metadata and method references.
- Use site reference and determinand metadata to build reproducible data pipelines and dashboards with clear provenance.

## Gaps and challenges for Data Leaders
- Data discovery: Determinant details and methodology are in separate files; ensure discoverability and proper linking.
- Data quality management: Handle periods with instrument errors (e.g., pH) and maintain provenance of corrected values.
- Data standards and interoperability: Align units, definitions, and metadata across multiple files; manage inconsistent or missing fields.
- Data access barriers: Some methodological details require additional files (e.g., RTF), potentially impacting usability for rapid analysis.

## Next steps and actions for data leadership
- Establish clear governance for linking Water_quality_data.csv with Determinand_list.csv and Sampling_sites.csv (and the RTF methodology) to ensure consistent interpretation.
- Implement data quality checks focused on pH values during instrument failure periods and document the corrections transparently.
- Create a centralized metadata catalog or data dictionary that cross-references SiteRef, SiteName, determinands, and sampling methods.
- Ensure discoverability and access to all supporting documents, with versioning and update notifications.
- Promote data standardization for future work packages to reduce fragmentation across files and improve cross-site comparability.