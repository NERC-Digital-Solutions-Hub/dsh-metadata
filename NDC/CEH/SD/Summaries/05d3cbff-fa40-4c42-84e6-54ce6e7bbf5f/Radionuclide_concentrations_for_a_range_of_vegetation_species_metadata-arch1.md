# Radionuclide meta-data

- Purpose
  - Metadata and activity-concentration measurements from CEH Radiochemistry laboratory for plant or soil samples, enabling correlation analysis and interpretation of radionuclide levels.

- Core sample identifiers and context
  - Sample_ID: unique sample identifier
  - Sampling_Site: sampling location
  - Sampling_date: date of sampling
  - Analysed_date: date analysis was performed
  - Analysis_time_days: duration of gamma-emitting radionuclide analysis

- Biological and taxonomic information
  - Species: Latin name of plant species (n/a if soil sample)
  - Common_name: common name (n/a if not available) or soil description
  - Order, Family, Genus: taxonomic classification (n/a if soil sample)

- Sample description and mass
  - Mass_of_sample_g: mass of the sample in grams (dry weight)

- Data normalization and units
  - Activity concentrations reported as Bq per kg dry weight
  - Units for Mass_of_sample_g: grams
  - Analyzed_date format: dd/mm/yyyy

- Radionuclide measurements and quality indicators
  - 40K (potassium-40)
    - Activity_concentration_40K_Bq_kg_dry
    - Counting_error_40K_Bq_kg_dry
    - MDA_40K_Bq_kg_dry (Minimum Detectable Activity)
    - 40K_<: indicates concentration below the limit of detection (LOD)
  - 137Cs (cesium-137)
    - Activity_concentration_137Cs_Bq_kg_dry
    - Counting_error_137Cs_Bq_kg_dry
    - MDA_137Cs_Bq_kg_dry (Minimum Detectable Activity)
    - 137Cs_<: indicates concentration below the limit of detection (LOD)
  - 7Be (beryllium-7)
    - Activity_concentration_7Be_Bq_kg_dry
    - Counting_error_7Be_Bq_kg_dry
    - MDA_7Be_Bq_kg_dry (Minimum Detectable Activity)
    - 7Be_<: indicator related to LOD

- Notes and data-context fields
  - Notes: information related to the sample that may impact results (or not applicable)

- Data quality and interpretation considerations for analysts
  - Enables assessment of radionuclide levels by site, sampling date, and plant species (when applicable)
  - Includes detection limits (LOD) and measurement uncertainties to support robust statistical analyses
  - Facilitates data provenance through explicit metadata fields (sample ID, dates, mass)
  - Some fields may be not applicable for soil samples (e.g., taxonomic fields) and formatting in the source text may vary (e.g., Cs-137 and Be-7 indicators)