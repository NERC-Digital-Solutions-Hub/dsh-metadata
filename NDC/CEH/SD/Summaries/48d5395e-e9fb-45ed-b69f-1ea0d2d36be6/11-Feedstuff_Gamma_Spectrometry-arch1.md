# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

## Overview
- This document describes the metadata fields and measurement descriptors for the 11-Feedstuff_Gamma_Spectrometry.csv dataset.
- It covers sample identifiers, sample descriptions, collection details, and activity concentration measurements for radionuclides on a dry-mass basis, including associated uncertainties and detection limits.

## Data schema and fields

### Sample metadata
- Sample_Code
  - Explanation: Unique sample identifier
  - Units: n/a
  - Notes: .
- Sample_Type
  - Explanation: General description of sample (e.g., foodstuff group)
  - Units: n/a
  - Notes: .
- Location
  - Explanation: Name of the location where the sample was collected
  - Units: n/a
  - Notes: .
- Sample_Description
  - Explanation: Part of the organism analysed (e.g., where whole organism was divided and analysed separately)
  - Units: n/a
  - Notes: .
- Collection_Date
  - Explanation: Date of sample collection
  - Units: dd-mm-yyyy
  - Notes: .
- Sample_size
  - Explanation: Amount of sample analyzed
  - Units: kg fresh mass
  - Notes: .

### Measurement data (radionuclide activity concentrations on a dry mass basis)
- Ra-226_Bq/kg_dm
  - Explanation: Activity concentration of Ra-226 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214. Where blank, concentration was below the detection limit.
- Unc_Ra-226_Bq/kg_dm
  - Explanation: Uncertainty of activity concentration of Ra-226 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214. Where blank, concentration was below the detection limit.
- Detection_Limit_Ra-226_Bq/kg_dm
  - Explanation: Detection limit of Ra-226 on a dry mass basis, calculated according to ISO 11929
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214.

- Cs-137_Bq/kg_dm
  - Explanation: Activity concentration of Cs-137 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: Where blank, concentration was below the detection limit.
- Unc_Cs-137_Bq/kg_dm
  - Explanation: Uncertainty of activity concentration of Cs-137 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: Where blank, concentration was below the detection limit.
- Detection_Limit_Cs-137_Bq/kg_dm
  - Explanation: Detection limit of Cs-137 on a dry mass basis, calculated according to ISO 11929
  - Units: Bq/kg dry mass
  - Notes: n/a

- Ra-228_Bq/kg_dm
  - Explanation: Activity concentration of Ra-228 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Ac-228. Where blank, concentration was below the detection limit.
- Unc_Ra-228_Bq/kg_dm
  - Explanation: Uncertainty of activity concentration of Ra-228 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Ac-228. Where blank, concentration was below the detection limit.
- Detection_Limit_Ra-228_Bq/kg_dm
  - Explanation: Detection limit of Ra-228 on a dry mass basis, calculated according to ISO 11929
  - Units: Bq/kg dry mass
  - Notes: In equilibrium with Ac-228. Where blank, concentration was below the detection limit.

- K-40_Bq/kg_dm
  - Explanation: Activity concentration of K-40 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: Where blank, concentration was below the detection limit.
- Unc_K-40_Bq/kg_dm
  - Explanation: Uncertainty of activity concentration of K-40 on a dry mass basis
  - Units: Bq/kg dry mass
  - Notes: Where blank, concentration was below the detection limit.
- Detection_Limit_K-40_Bq/kg_dm
  - Explanation: Detection limit of K-40 on a dry mass basis, calculated according to ISO 11929
  - Units: Bq/kg dry mass
  - Notes: n/a

## Notes on interpretation
- All activity concentrations are reported on a dry mass basis (Bq/kg_dm); sample_size is given in kg fresh mass, which may require conversion if comparing to dry-mass references.
- Equilibrium considerations:
  - Ra-226: in equilibrium with Pb-214 and Bi-214.
  - Ra-228: in equilibrium with Ac-228.
- Non-detects are indicated by blank fields for concentration and their corresponding uncertainties.
- Detection limits follow ISO 11929 methodology.

## How this supports analysis
- Provides standardized identifiers and metadata to link samples with measurements and collection context.
- Supplies quantitative radionuclide concentrations with uncertainties and detection limits essential for statistical analyses, trend detection, and risk assessment.
- Enables filtering by sample type, location, collection date, and sample description to support focused queries and model inputs.

## Data quality considerations and caveats
- Some fields use blanks to denote non-detects; ensure proper handling of censored data (non-detects) in analyses.
- Differences between fresh mass and dry mass basis require careful unit consistency when aggregating or comparing across samples.
- Equilibrium assumptions are stated per radionuclide and should be considered when interpreting the activity ratios or when combining isotopes in models.