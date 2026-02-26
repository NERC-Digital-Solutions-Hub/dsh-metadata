# TREE_Northumbria_Gamma_Vegetation

- Purpose: A data dictionary for a Northumbria vegetation gamma-activity dataset, capturing plant species, sampling details, and radiometric measurements to enable consistent assessment of environmental radioactivity over time.

## Key data elements

- Taxonomy and sampling context
  - Latin_Species_Name
  - Common_Species_Name
  - Plant_Part_Analysed
  - Site
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Sampling_Date_Used_As_Decay_Date

- Sample metadata
  - Dry_Mass_Of_Sample_Analysed_g

- Radionuclide measurements (activity concentrations)
  - K-40_Bq_per_kg_DM
  - Counting_Error_K-40_Bq_per_kg_DM
  - K-40_< (less-than flag)
  - MDA_K-40_Bq_per_kg_DM
  - K-40_Bq_per_kg_FM
  - Counting_Error_K-40_Bq_per_kg_FM
  - K-40_< (FM) (less-than flag)
  - MDA_K-40_Bq_per_kg_FM

  - Cs-137_Bq_per_kg_DM
  - Counting_Error_Cs-137_Bq_per_kg_DM
  - Cs-137_DM_< (less-than flag)
  - MDA_Cs-137_Bq_per_kg_DM
  - Cs-137_Bq_per_kg_FM
  - Counting_Error_Cs-137_Bq_per_kg_FM
  - Cs-137_FM_< (less-than flag)
  - MDA_Cs-137_Bq_per_kg_FM

- Cs-137 concentration ratios
  - Cs-137_Concentration_Ratio_DM
  - Cs-137_Concentration_Ratio_DM_< (less-than flag)
  - Cs-137_Concentration_Ratio_FM
  - Cs-137_Concentration_Ratio_FM_< (less-than flag)

- Notes and general guidance
  - Notes_Related_to_137Cs_Concentration_Ratio
  - General_Notes (e.g., notes about data interpretation)

## Data quality, processing, and provenance

- Data are derived from established radiochemistry workflows (e.g., UKCEH laboratory context) with unique sample identifiers and descriptive sampling metadata.
- Measurements include:
  - Two-sigma counting errors for K-40 and Cs-137
  - Minimum detectable activity (MDA) values for both dry mass (DM) and fresh mass (FM) measurements
  - Less-than flags to indicate concentrations below MDAs
- Date handling includes using the sampling date as the decay date where applicable to support time-based comparisons.

## How the data support environmental monitoring

- Enables standardized outputs (reports, maps, charts) to compare environmental radioactivity across sites and over time.
- Allows categorization of environmental health against standards using concentration data for K-40 and Cs-137.
- Ensures datasets are stored and accessible via appropriate data portals for transparency and reuse.

## Key challenges and opportunities

- Increase the value of datasets by integrating with other relevant environmental data (multi-source analyses, not single-use).
- Improve accessibility of underlying data used to generate final outputs, supporting broader scrutiny and reuse by stakeholders.