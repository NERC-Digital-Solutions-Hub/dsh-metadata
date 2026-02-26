# Radionuclide meta-data

## Overview
- Metadata framework describing radionuclide measurements in plant or soil samples.
- Supports verification, quality assurance, transformation, and standardized presentation of environmental radiological data.
- Facilitates data reuse and integration into reports, maps, and portals.

## Key data fields

- Identification and sampling
  - Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
  - Sampling_Site: Sampling site description.
  - Sampling_date: Date the plant species or soil was sampled.
  - Analysed_date: Date the sample was analysed.
  - Analysis_time_days: Number of days the sample was analysed for gamma-emitting radionuclides.

- Sample composition and taxonomy
  - Species: Latin name of the plant species (n/a if soil sample).
  - Common_name: Common name of the plant species (or soil sample description).
  - Order, Family, Genus: Taxonomic classification (n/a if soil sample).
  - Mass_of_sample_g: Mass of the soil or plant sample (dry weight).

- Data provenance and processing
  - Notes: Information related to the sample that may impact results (or not applicable).

- Radionuclide measurements and quality indicators
  - Activity_concentration_40K_Bq_kg_dry: K-40 activity concentration (Bq per kg dry weight).
  - Counting_error_40K_Bq_kg_dry: Counting error for K-40 concentration.
  - 40K_<: Indicator that K-40 concentration is below the limit of detection (LOD).
  - MDA_40K_Bq_kg_dry: Minimum detectable activity for K-40 (Bq/kg dry).
  - Activity_concentration_1_37Cs_Bq_kg_dry: Cs-137 activity concentration (Bq per kg dry weight).
  - Counting_error_137Cs_Bq_kg_dry: Counting error for Cs-137 concentration.
  - 137Cs_<: Indicator that Cs-137 concentration is below LOD.
  - MDA_137Cs_Bq_kg_dry: Minimum detectable activity for Cs-137 (Bq/kg dry).
  - 7Be_<: Indicator that Be-7 concentration is below LOD.
  - MDA_7Be_Bq_kg_dry: Minimum detectable activity for Be-7 (Bq/kg dry).

- Units and data types
  - Units are specified for numeric fields (e.g., Bq/kg dry, grams).
  - Text fields indicate not applicable when appropriate (e.g., units for non-quantitative fields).

## Data quality, provenance and standardization
- Provides a standardized schema with clear field meanings to ensure consistency across samples and studies.
- Includes detection and reporting limits (LOD, MDA) and measurement uncertainty (counting error).
- Dates and weights follow defined formats to enable reliable time-series analyses.
- Designed to be stored and uploaded to appropriate data portals for broader accessibility.

## How this supports environmental monitoring
- Enables consistent tracking of radionuclide activity across sites and time.
- Facilitates QA and data verification by providing traceable sample and analytical metadata.
- Supports integration into reports, maps, and dashboards for environmental health assessments and policy performance monitoring.

## Considerations for Analysts
- Some fields may be not applicable for soil samples (taxonomy fields).
- Pay attention to LOD indicators (<) and MDAs to interpret whether concentrations are detected or below threshold.
- Ensure proper linkage between sample IDs, sites, dates, and analytical results when aggregating datasets.
- Leverage Notes to capture context that could affect interpretation of results.