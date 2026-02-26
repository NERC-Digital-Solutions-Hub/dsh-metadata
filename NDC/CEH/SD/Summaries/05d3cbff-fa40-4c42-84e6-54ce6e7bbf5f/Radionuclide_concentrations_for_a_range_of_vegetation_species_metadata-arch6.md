# Radionuclide meta-data

## Overview
- Metadata schema for radionuclide measurements in plant or soil samples, associated with CEH Radiochemistry laboratory.
- Captures sample identity, sampling context, taxonomic information (when applicable), sample mass, analysis timing, and radionuclide activity concentrations.
- Aims to enable data discovery, verification, combination with other datasets, and creation of self-service data products.

## Key fields (schema highlights)
- Sample_ID: unique sample identifier.
- Sampling_Site: location of sampling.
- Sampling_date: date when plant species or soil was sampled.
- Species: Latin name of the plant species (n/a for soil samples).
- Common_name: common name of the plant species (or soil sample description) (n/a if not applicable).
- Taxonomic fields: Order, Family, Genus (n/a if soil sample).
- Mass_of_sample_g: mass of sample in grams (dry weight).
- Analysed_date: date the sample was analysed (dd/mm/yyyy).
- Analysis_time_days: number of days the sample was analysed for gamma-emitting radionuclides.
- Activity_concentration_40K_Bq_kg_dry: K-40 activity concentration (Bq/kg dry weight).
- Counting_error_40K_Bq_kg_dry: counting error for 40K concentration.
- 40K_<: flag indicating that the 40K concentration is below the limit of detection (LOD).
- MDA_40K_Bq_kg_dry: minimum detectable activity for 40K (Bq/kg dry weight).
- Activity_concentration_137Cs_Bq_kg_dry: Cs-137 activity concentration (Bq/kg dry weight).
- Counting_error_137Cs_Bq_kg_dry: counting error for Cs-137 concentration.
- 137Cs_<: flag indicating Cs-137 concentration is below LOD.
- MDA_137Cs_Bq_kg_dry: minimum detectable activity for Cs-137 (Bq/kg dry weight).
- Activity_concentration_7Be_Bq_kg_dry: Be-7 activity concentration (Bq/kg dry weight).
- 7Be_<: flag indicating Be-7 concentration below LOD.
- MDA_7Be_Bq_kg_dry: minimum detectable activity for Be-7 (Bq/kg dry weight).
- Notes: information related to samples that impact results (or not applicable).

## Units and data types
- Activity concentrations: Bq per kg dry weight (Bq/kg_dry).
- Mass: grams (g) for dry weight.
- Analysed_date: dd/mm/yyyy format.
- Analysis_time_days: days.
- LOD and MDA fields provide detection context for each isotope.

## Data quality and interpretation
- Below-LOD indicators (the “<” fields) flag measurements that are not detectable.
- MDA fields report the sensitivity limits for each isotope, aiding uncertainty assessment.
- Counting_error fields quantify measurement uncertainty.
- Some taxonomic fields may be not applicable for soil samples; species-related fields are provided when applicable.

## Data structure notes
- Field names appear with minor formatting inconsistencies (e.g., spaces within field labels such as “Activity_concentration_4 0K_Bq_kg_dry” and “137Cs_B q_kg_dry”). The intended fields pertain to 40K, 137Cs, and 7Be activity concentrations, their errors, detection flags, and MDAs.

## Practical applications for data use
- Enables cross-sample comparisons of radionuclide activities across sites, dates, and sample types.
- Supports creation of dashboards or pivot-based reports to explore isotope-specific patterns.
- Facilitates self-service data exploration with filters on site, date, species (where applicable), and isotope (40K, 137Cs, 7Be).
- Provides metadata to assess data quality and detection limits prior to analysis or reporting.

## Context and source
- Data originate from CEH Radiochemistry laboratory, focusing on gamma-emitting radionuclides in biota and soils, with structured metadata to accompany concentration measurements.