# Radionuclide_Distribution_Down_Soil_Profiles_metadata

- Scope
  - Metadata describing the distribution of radionuclides (Cs-137 and Sr-90) in soil profiles and associated litter/ash samples around specified sites.
  - Notes that the site identifier is numerical and the same as used in a related dataset ("Description of Trees").

- Key spatial and sampling metadata
  - Site_Identifier: numerical site ID (used consistently across related datasets).
  - Site_Latitude_WGS84_Decimal_Degrees: latitude in decimal degrees (GPS, WGS84).
  - Site_Longitude_WGS84_Decimal_Degrees: longitude in decimal degrees (GPS, WGS84).
  - Sampling_Point: numerical identifier for each sampling point.
  - Sampling_Date: date of sampling in DD/MM/YYYY.

- Fire impact and sample context
  - Fire_Impact_At_Site: classification of fire impact observed on trees at the site (None, Slightly impacted, Heavily Impacted).

- Sampling specifics
  - Soil_Layer: depth or layer of soil sampled (in cm).
  - Litter/ash sampling note: area of 0.078 m^2 sampled.

- Radionuclide measurements and detection
  - <_Identifier_Cs-137: marker indicating where Cs-137 activity concentration was below minimum detectable activity (n/a).
  - Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Cs-137 in dry mass (Bq/kg).
  - Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty of Cs-137 concentration (percent).
  - <_Identifier_Sr-90: marker indicating where Sr-90 activity concentration was below minimum detectable activity (n/a).
  - Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Sr-90 in dry mass (Bq/kg).
  - Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty of Sr-90 concentration (percent).

- Sample mass and data completeness
  - Sample_Dry_Mass_kg_m-2: reported as "kg/m^2" (dry mass per area); may include "ND" (not determined) for some entries.

- Data labeling and interpretation notes
  - <_Identifier_ fields indicate measurements below detection limits.
  - ND (not determined) and n/a (not applicable) used for specific fields to signal data gaps or irrelevance.
  - Units specified for each field (e.g., DD for degrees, cm for depth, Bq/kg for activity concentration, kg/m^2 for mass per area).

- Data quality and governance implications
  - Uncertainties are explicitly provided (2-sigma), enabling propagation of measurement error in analyses.
  - Clear differentiation between detected values and below-detection indicators supports data quality assessment.
  - Metadata aligns with geographic and sampling standards (GPS-based coordinates, standardized date formats).

- Data availability, maintenance, and use
  - Datasets are prepared for upload to portals and catalogues; care should be taken to respect sharing limitations, embargoes, and provenance.
  - Documentation notes linking to related datasets (e.g., “Description of Trees”) for cross-dataset discoverability.
  - Ongoing updates and versioning should be tracked to maintain currentness and interoperability.

- Challenges and considerations for Data Stewards
  - Incomplete user needs regarding specific radionuclide concentration reporting or metadata depth.
  - Ensuring consistent metadata definitions across datasets (e.g., fire impact categories, detection-limit markers).
  - Managing interoperability across different systems, formats, and legacy databases.
  - Handling large, geo-referenced datasets with precise sampling contexts and multiple radionuclide metrics.

- Recommendations for governance and quality assurance
  - Maintain a data dictionary with explicit definitions for all fields (including <_Identifier_ markers and ND/n/a conventions).
  - Enforce standardized units and formatting (e.g., decimal degrees, DD/MM/YYYY, Bq/kg).
  - Capture provenance and data processing steps (e.g., how dry mass was determined, any transformations before reporting).
  - Implement controlled vocabularies for Fire_Impact_At_Site and ensure clear indications of detection limits.
  - Provide cross-references to related datasets to enhance discoverability and reuse.