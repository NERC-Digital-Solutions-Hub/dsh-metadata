# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

## Overview
- Defines metadata and measurement fields for the dataset 17-Transfer_Parameter_Vegetal_Stable.csv.
- Focuses on transfer parameter (Fv) values for stable elements in plant-derived foods, specifically olive oil and wine.
- Includes sample metadata (identifier, type, location, collection date) and a comprehensive set of Fv-related measurements plus uncertainties and detection limits.
- Notes that blank values indicate measurements below detection limits.

## Data structure and fields
- Sample metadata
  - Sample_Code: Unique sample identifier
  - Sample_Type: General description of the sample (e.g., foodstuff group)
  - Location: Location where the sample was collected
  - Sample_Description: Part of the plant analysed (e.g., which portion of the plant)
  - Collection_Date: Date of sample collection (dd-mm-yyyy)
- Transfer parameter measurements (Fv) and related metadata for each element
  - Cs_Fv: Fv value for stable Cs (Unitless or kg dry matter per L for olive oil and wine)
  - Unc_Cs_Fv: Uncertainty of Cs Fv
  - Detection_Limit_Cs_Fv: Detection limit for Cs Fv
  - Sr_Fv: Fv value for stable Sr
  - Unc_Sr_Fv: Uncertainty of Sr Fv
  - Detection_Limit_Sr_Fv: Detection limit for Sr Fv
  - K_Fv: Fv value for stable K
  - Unc_K_Fv: Uncertainty of K Fv
  - Detection_Limit_K_Fv: Detection limit for K Fv
  - Na_Fv: Fv value for stable Na
  - Unc_Na_Fv: Uncertainty of Na Fv
  - Detection_Limit_Na_Fv: Detection limit for Na Fv
  - Ca_Fv: Fv value for stable Ca
  - Unc_Ca_Fv: Uncertainty of Ca Fv
  - Detection_Limit_Ca_Fv: Detection limit for Ca Fv
  - Mg_Fv: Fv value for stable Mg
  - Unc_Mg_Fv: Uncertainty of Mg Fv
  - Detection_Limit_Mg_Fv: Detection limit for Mg Fv
  - P_Fv: Fv value(s) for stable P (multiple entries indicated by indices 1, 2, 3)
  - Unc_P_Fv: Uncertainty of P Fv (corresponding indices)
  - Detection_Limit_P_Fv: Detection limit for P Fv (corresponding indices)
  - Pb_Fv: Fv value(s) for stable Pb (indices 1, 2, 3)
  - Unc_Pb_Fv: Uncertainty of Pb Fv (indices 1, 2, 3)
  - Detection_Limit_Pb_Fv: Detection limit for Pb Fv (indices 1, 2, 3)
  - U_Fv: Fv value for stable U (indices 1, 2, 3)
  - Unc_U_Fv: Uncertainty of U Fv (indices 1, 2, 3)
  - Detection_Limit_U_Fv: Detection limit for U Fv (indices 1, 2, 3)
  - Th_Fv: Fv value for stable Th (indices 1, 2, 3)
  - Unc_Th_Fv: Uncertainty of Th Fv (indices 1, 2, 3)
  - Detection_Limit_Th_Fv: Detection limit for Th Fv (indices 1, 2, 3)

## Measurement details
- Fv values represent transfer parameters for stable radionuclides/elements from plant sources to olive oil and wine contexts.
- Units and interpretation
  - Cs_Fv: Unitless or kg dry matter per L (olive oil and wine)
  - Other elements (Sr, K, Na, Ca, Mg, P, Pb, U, Th): Unitless or kg dry matter per L (olive oil and wine) as specified
- Notes on limits
  - Where a Fv value is blank, it indicates values below the detection limit for that measurement.

## Data quality and documentation notes
- The document includes explicit fields for uncertainty (Unc_*) and detection limits (Detection_Limit_*) to support QA/QC and data interpretation.
- Some entries show formatting inconsistencies (e.g., misaligned equals signs or stray labels), but the intended structure is consistent: each element has corresponding Fv, Unc_Fv, and Detection_Limit_Fv fields, with additional indexed variants for certain elements (P_Fv, Pb_Fv, U_Fv, Th_Fv).
- Emphasizes standardised data handling, enabling clear categorisation of environmental transfer parameters across samples and time.

## Data handling and accessibility
- The dataset is intended to be stored and uploaded to appropriate data portals, aligning with the goal of ensuring datasets are accessible for scrutiny, reuse, and policy monitoring.
- By providing standardized metadata and measurement fields, the dataset supports transparent comparisons and long-term environmental health assessment.

## Relevance for environmental monitoring analysts
- Supports consistent reporting of transfer parameters for stable elements in plant-derived food matrices (olive oil and wine).
- Facilitates monitoring over time and across locations by standardising sample metadata and measurement definitions.
- Helps analysts assess data quality via uncertainties and detection limits, and enables integration with other environmental datasets to enhance the value of monitored data.