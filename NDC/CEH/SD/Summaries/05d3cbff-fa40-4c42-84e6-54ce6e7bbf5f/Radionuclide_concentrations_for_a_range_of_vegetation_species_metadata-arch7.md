# Radionuclide meta-data

- The document defines a data schema for radionuclide measurements from the CEH Radiochemistry laboratory.
- It lists field names, explanations, and units to support consistent data capture and GIS-ready integration.

## Key fields and their purpose

- Sample_ID
  - Explanation: CEH Radiochemistry laboratory unique sample identifier
  - Units: not applicable
- Sampling_Site
  - Explanation: Sampling site
  - Units: not applicable
- Sampling_date
  - Explanation: Date plant species or soil was sampled
  - Units: not applicable
- Species
  - Explanation: Latin name of the plant species (n/a if soil sample)
  - Units: not applicable
- Common_name
  - Explanation: Common name of the plant species if available (n/a if none) or soil description
  - Units: not applicable
- Order, Family, Genus
  - Explanation: Taxonomic classification (n/a if soil sample)
  - Units: not applicable
- Mass_of_sample_g
  - Explanation: Mass of soil or plant species in grams (dry weight)
  - Units: gram
- Analysed_date
  - Explanation: Date plant species or soil was analysed
  - Units: dd/mm/yyyy
- Analysis_time_days
  - Explanation: Number of days the sample was analysed for gamma-emitting radionuclides
  - Units: days

- Activity_concentration_40K_Bq_kg_dry
  - Explanation: Measurement of K-40 activity concentration
  - Units: Bq per kg dry weight
- Counting_error_40K_Bq_kg_dry
  - Explanation: Counting error for K-40 activity concentration
  - Units: Bq per kg
- 40K_<
  - Explanation: Indicator that K-40 concentration was below the limit of detection (LOD)
  - Units: not applicable
- MDA_40K_Bq_kg_dry
  - Explanation: Minimum detectable activity (MDA) for K-40
  - Units: Bq per kg
- Activity_concentration_1 37Cs_Bq_kg_dry
  - Explanation: Measurement of Cs-137 activity concentration
  - Units: Bq per kg dry weight
- Counting_error_137Cs_Bq_kg_dry
  - Explanation: Counting error for Cs-137 activity concentration
  - Units: Bq per kg
- 137Cs_<
  - Explanation: Indicator that Cs-137 concentration was below the LOD
  - Units: not applicable
- MDA_137Cs_Bq_kg_dry
  - Explanation: Minimum detectable activity (MDA) for Cs-137
  - Units: Bq per kg
- 7Be_<
  - Explanation: Indicator that Be-7 concentration was below the LOD
  - Units: not applicable
- MDA_7Be_Bq_kg_dry
  - Explanation: Minimum detectable activity (MDA) for Be-7
  - Units: Bq per kg
- Notes
  - Explanation: Information related to the sample that may impact results
  - Units: not applicable

## Data quality, standards, and formats

- Some field names contain formatting inconsistencies (e.g., spaces in “Activity_concentration_40K_Bq_kg_dry” vs “Activity_concentration_4 0K_Bq_kg_dry”) that should be standardized for GIS ingestion.
- Units vary by field; many metadata fields use “not applicable,” while mass and activity fields use standard SI units (grams; Bq per kg dry weight).
- LOD and MDA indicators are embedded as dedicated fields (e.g., 40K_<, 137Cs_<, 7Be_<) to flag measurements below detection limits.
- Date fields use specific formats (dd/mm/yyyy for analysed dates) and temporal information is available via Sampling_date and Analysed_date.
- Taxonomic fields (Species, Genus, Family, Order) enable spatial joins with ecological or vegetation layers; soil samples are indicated by n/a in certain taxonomic fields.

## How this supports GIS workflows

- Spatial tagging: Sampling_Site and Sampling_date enable mapping of radionuclide data across sites and time.
- Taxonomic and habitat context: Species, Common_name, Genus, Family, and Order allow layering with vegetation or land-use GIS datasets.
- Quantitative mapping: Activity_concentration fields for K-40, Cs-137, and Be-7 support choropleth or proportional symbol maps by site and time.
- Data quality visualization: LOD (indicated by <) and MDA fields help display detection limits and data reliability in maps and dashboards.
- Data integration: The schema supports joining to external GIS layers (sites, plant communities) and to other lab-derived datasets using Sample_ID.

## Practical considerations for GIS data ingestion

- Standardize field names and fix any formatting anomalies before loading into GIS (e.g., remove unintended spaces, unify K-40 field naming).
- Normalize and document units consistently; convert to a single dry-weight basis if combining datasets.
- Preserve LOD and MDA indicators as explicit attributes to maintain data interpretation during visualization.
- Handle n/a taxonomic fields appropriately for soil samples to avoid mislabeling sites.
- Validate date formats and ensure temporal sequencing (Sampling_date vs Analysed_date) is preserved for time-series analyses.

## Endnotes

- The dataset provides a comprehensive metadata schema for radionuclide measurements, enabling robust GIS-enabled analysis and visualization of spatial and temporal patterns in radionuclide concentrations across plant and soil samples.