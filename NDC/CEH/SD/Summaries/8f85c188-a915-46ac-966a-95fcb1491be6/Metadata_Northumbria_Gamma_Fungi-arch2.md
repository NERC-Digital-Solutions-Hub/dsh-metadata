# TREE_Northumbria_Gamma_Fungi

## Overview
- A radiochemical dataset detailing activity concentrations of potassium-40 (K-40) and cesium-137 (Cs-137) in soil and fungi at a Northumbria site.
- Captures both fresh mass and dry mass measurements, including associated uncertainties and detection metrics.
- Includes comprehensive sample metadata (species, site, sample identifiers, dates) and notes to support quality assurance and traceability.
- Intended for standardized analysis, reporting, and longitudinal monitoring of environmental radiological status.

## Data scope and structure
- Sample identifiers and context:
  - Latin_Species_Name (for fungi)
  - CEH_Sample_Identifier (UKCEH Radiochemistry Laboratory unique sample ID)
  - Site (sampling location)
  - Sampling_Date_Used_As_Decay_Date (date used for decay calculations)
- Mass and preparation:
  - Mass_of_Sample_analysed_g (mass analyzed in grams)
  - Fresh_Mass_Dry_Mass_Ratio (moisture content ratio)
- Measurements (activity concentrations):
  - K-40_Bq_per_kg_DM (dry mass)
  - K-40_Bq_per_kg_FM (fresh mass)
  - Cs-137_Bq_per_kg_DM (dry mass)
  - Cs-137_Bq_per_kg_FM (fresh mass)
- Uncertainty and detection:
  - Counting_Error_K-40_Bq_per_kg_DM
  - Counting_Error_K-40_Bq_per_kg_FM
  - Counting_Error_Cs-137_Bq_per_kg_DM
  - Counting_Error_Cs-137_Bq_per_kg_FM
  - MDA_K-40_Bq_per_kg_DM (minimum detectable activity, dry mass)
  - MDA_K-40_Bq_per_kg_FM (minimum detectable activity, fresh mass)
  - MDA_Cs-137_Bq_per_kg_DM
  - MDA_Cs-137_Bq_per_kg_FM
  - "<" markers indicating values below the stated MDA (K-40_<, Cs-137_<)
- Derived metrics:
  - Cs-137_Concentration_Ratio_Fungi_FM (ratio: fungi Bq/kg FM / soil Bq/kg DM)
  - Cs-137_Concentration_Ratio_Fungi_DM (ratio: fungi Bq/kg DM / soil Bq/kg DM)
  - Note: Concentration ratio fields are labeled with dedicated notes (CR_Notes)
- Notes and contextual information:
  - CR_Notes (Concentration ratio notes)
  - General_Notes (General notes)

## Key measurements and units
- Activity concentrations in Bq per kg:
  - Dry Mass (DM) and Fresh Mass (FM) for K-40 and Cs-137
- Uncertainty and detection:
  - Two-sigma counting errors accompanying each concentration
  - Minimum detectable activities (MDAs) for both DM and FM
  - “Less than” markers to indicate sub-MDA concentrations
- Derived ratios:
  - Concentration ratios comparing fungi to soil for Cs-137 (both DM and FM contexts)

## Metadata, provenance, and workflow
- Sample provenance:
  - Site, Latin species name, and unique sample identifiers provide traceability
  - Sampling date is recorded and used as the decay date when applicable
- Sample mass and preparation:
  - Mass of sample analysed and moisture content guidance (Fresh vs Dry mass)
- Data quality and handling:
  - Data are verified, quality assured, cleaned, and transformed
  - Standardised analytic methods drive outputs (e.g., categorising environmental radiological status)
  - Datasets are stored and uploaded to appropriate data portals

## Data usage and purpose
- Supports monitoring and scrutiny of environmental radiological health over time
- Enables standardised reporting, mapping, and charting for policy performance assessment
- Facilitates accessibility of underlying data to enhance transparency and reuse
- Aligns with routine responsibilities of environmental monitoring organisations and topic-specific analysts

## Challenges and opportunities
- Enhancing dataset value by integrating with related datasets (e.g., other radionuclides, habitats, or temporal datasets) beyond single-use analyses
- Improving access to underlying data used to produce final outputs to support broader analysis and cross-study comparisons