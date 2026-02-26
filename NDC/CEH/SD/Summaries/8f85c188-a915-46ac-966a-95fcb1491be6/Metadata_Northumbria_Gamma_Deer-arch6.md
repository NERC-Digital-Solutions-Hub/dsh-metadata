# TREE_Northumbria_Gamma_Deer

## Overview
- Dataset containing radiochemical measurements of Cs-137 in Roe deer samples, linked to UKCEH radiochemistry sampling and descriptions.
- Includes sample identifiers, tissue type, site, mass, sampling/decay date, activity concentrations in fresh and dry mass, measurement uncertainties, detection limits, and concentration ratios with notes.
- Designed to enable comparison and self-service analysis across samples and sites, with metadata to aid data cleaning and interpretation.

## Data fields and definitions

- Latin_Species_Name
  - Explanation: Latin name of species
  - Units: n/a

- CEH_Sample_description
  - Explanation: UKCEH sample description
  - Units: n/a

- Tissue
  - Explanation: Tissue of Roe deer
  - Units: n/a

- CEH_Sample_code
  - Explanation: UKCEH Radiochemistry Laboratory unique sample identifier
  - Units: n/a

- Site
  - Explanation: Sampling site
  - Units: n/a

- Fresh_Mass_Of_Sample_Analysed_g
  - Explanation: Fresh mass of sample analysed
  - Units: g

- Sampling_date_Used_As_Decay_date
  - Explanation: Date the sample was taken, also used as decay date
  - Units: n/a

- Cs-137_Bq_per_kg_FM
  - Explanation: Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling
  - Units: Bq per kg FM

- Counting_Error_Cs-137_Bq_per_kg_DM
  - Explanation: Two sigma counting error of Cs-137 in Bq per kg dry mass
  - Units: Bq per kg DM

- Cs-137 <
  - Explanation: < Marker is used to identify concentration given in column MDA_Cs-137_Bq_per_kg_FM is a 'less than' value
  - Units: n/a

- MDA_Cs-137_Bq_per_kg_FM
  - Explanation: Minimum detectable activity concentration of Cs-137 in Bq per kg fresh mass
  - Units: Bq per kg FM

- Cs-137_Concentration_Ratio_FM
  - Explanation: Cs-137 Concentration ratio (fresh mass) (Bq per kg Fresh mass activity concentration in muscle divided by Bq per kg dry mass activity concentration soil)
  - Units: n/a

- CR_Notes
  - Explanation: Notes related to concentration ratio
  - Units: n/a

## Data quality and interpretation considerations
- Some Cs-137 values may be reported as below detection (indicated by the < marker in Cs-137_BQ_per_kg_FM vs MDA_Cs-137_Bq_per_kg_FM).
- Measurements include two-sigma counting errors for dry-mass concentrations, enabling uncertainty-aware analyses.
- Decay dating is anchored to Sampling_date_Used_As_Decay_date, which may be used for decay corrections if applicable.
- Concentration ratio (Cs-137_Concentration_Ratio_FM) compares fresh-mass tissue activity to dry-mass soil activity, with accompanying notes in CR_Notes for context.

## How this data can be used
- Build dashboards or self-service reports to compare Cs-137 activity across sites, tissues, and sampling dates.
- Analyze relationships between fresh mass and dry mass activity concentrations (via Cs-137_Concentration_Ratio_FM).
- Apply detection-limit awareness using MDA_Cs-137_Bq_per_kg_FM and Cs-137_Bq_per_kg_FM, with associated Counting_Error_Cs-137_Bq_per_kg_DM.
- Link samples to descriptive metadata (CEH_Sample_description, CEH_Sample_code) for traceability and provenance in broader datasets.

## Practical notes for data work
- Ensure consistent handling of units (FM vs DM) when merging with other datasets.
- Use sampling/site metadata to contextualize results and support spatial analyses.
- Leverage CR_Notes for any caveats or special conditions affecting specific samples or measurements.