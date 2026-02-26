# Water quality data - work packages 3 and 5

## Overview
- A water quality dataset consisting of a primary data file (Water_quality_data.csv) and supporting metadata/files.
- Metadata and methodological context are provided by Sampling_sites.csv, Determinand_list.csv, and Particulate_matter_method.rtf.
- Designed to support assessment of water quality across estuarine and freshwater sites and to be discoverable and usable by data users.

## Dataset Components

- Water_quality_data.csv
  - Core data file containing sampling results.
  - First five columns:
    - SiteRef: unique site reference code (e.g., BCN, TYC, DOL are estuarine; others are freshwater).
    - SiteName: unique site name.
    - Trip: field trip identifier; notes indicate sampling occurred by hand, autosampler, or extended periods; 3-digit codes indicate intermediate dates.
    - Date: sampling date.
    - Time: sampling time.
  - Determinand values: accompanied by qualifiers (usually blank, sometimes <).
  - pH data: includes pHUncorrected (uncorrected values) and pH (a mix of correct and corrected values); a period of instrument failure produced incorrect pH values.
  - Blank fields indicate missing data; zeros are actual measured values.
  - Details for all other columns are provided in Determinand_list.csv.

- Sampling_sites.csv
  - SiteName: unique site name.
  - SiteRef: unique site code.
  - Type: Fresh or Saline (Fresh/Saline indicate tidal influence).
  - Sampling: Spot or Continuous sampling.
  - Easting and Northing: National Grid coordinates.

- Determinand_list.csv
  - Provides definitions and details for the other columns in Water_quality_data.csv (i.e., the determinand measurements and their metadata).

- Particulate_matter_method.rtf
  - Methodology information for analysis of certain particulates.

## Data Quality and Provenance

- Data quality notes:
  - Determinand values include qualifiers; some values are below detection or represent partial measurements.
  - Period of instrument failure affected pH readings; uncorrected pH values are retained separately (pHUncorrected) and corrected values are indicated in the pH column.
  - Missing data represented by blank fields; some variables were not measured for certain samples.
- Data linkage:
  - SiteRef in Water_quality_data.csv should be cross-validated against Sampling_sites.csv to ensure consistent site naming and coordinates.
  - Determinand_list.csv provides essential definitions to interpret all determinand columns in Water_quality_data.csv.
- Documentation:
  - Methodology for particulates is provided in the Particulate_matter_method.rtf to support reproducibility.

## Metadata, Documentation, and Access

- The dataset is supported by separate but linked metadata files, enabling:
  - Clear interpretation of site identifiers and locations.
  - Definition of each determinand and its measurement context.
  - Methodological background for particulate analyses.
- Users can discover and understand the dataset through the combined set of CSVs and the methodology document.

## Data Governance and Use

- Data stewardship considerations:
  - Ensure consistency and alignment between Water_quality_data.csv and Sampling_sites.csv (SiteRef, SiteName, coordinates, and site type).
  - Maintain and communicate the provenance of corrections to pH values (which values were corrected and how).
  - Keep Determinand_list.csv up to date to reflect any changes in column definitions or units.
  - Preserve original (uncorrected) values alongside corrected values with clear qualifiers to enable traceability.
  - Document data processing steps (e.g., how corrections were applied) and maintain an audit trail.
  - Manage data updates and versioning to reflect new samples or corrected measurements; ensure updates propagate across all linked files.
  - Confirm data sharing permissions and any embargoes or usage restrictions at the portal level.

## Practical Recommendations for Data Stewards

- Ensure robust linking and consistency across files:
  - Validate that SiteRef codes in Water_quality_data.csv correspond to entries in Sampling_sites.csv.
  - Ensure determinand columns in Water_quality_data.csv have definitions in Determinand_list.csv.
- Improve clarity for users:
  - Provide a data dictionary or data dictionary appendix that explains each column, units, qualifiers, and any coding conventions (especially Trip codes and pH qualifiers).
  - Document the instrument failure period and its impact on pH data, including which records were affected and how corrections were derived.
- Support usability and discovery:
  - Maintain versioned releases with changelogs noting data additions, corrections, and methodological updates (e.g., any changes in sampling methods or determinations).
  - Consider exporting a consolidated metadata package or data portal record that ties Water_quality_data.csv, Sampling_sites.csv, Determinand_list.csv, and Particulate_matter_method.rtf together with explicit provenance.