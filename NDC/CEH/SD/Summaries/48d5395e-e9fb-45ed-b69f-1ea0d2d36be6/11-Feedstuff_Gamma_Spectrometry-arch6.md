# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

## Overview
- Provides the data dictionary and field explanations for a gamma spectrometry dataset on feedstuff samples.
- Focuses on sample metadata, measurement results for specific radionuclides, and associated uncertainties and detection limits.
- Specifies that activity concentrations are on a dry mass basis and uses a consistent date and unit framework to support data use and re-use.

## Data fields and structure

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (feedstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analyzed (e.g., tissue or component).
  - Collection_Date: Date of sample collection (dd-mm-yyyy).
  - Sample_size: Amount of sample analyzed (kg fresh mass).

- Measurement results (activity concentrations on a dry mass basis)
  - Ra-226_Bq/kg_dm: Activity concentration of Ra-226 (Bq/kg dry mass).
  - Cs-137_Bq/kg_dm: Activity concentration of Cs-137 (Bq/kg dry mass).
  - Ra-228_Bq/kg_dm: Activity concentration of Ra-228 (Bq/kg dry mass).
  - K-40_Bq/kg_dm: Activity concentration of K-40 (Bq/kg dry mass).

- Uncertainties
  - Unc_Ra-226_Bq/kg_dm: Uncertainty for Ra-226 concentration.
  - Unc_Cs-137_Bq/kg_dm: Uncertainty for Cs-137 concentration.
  - Unc_Ra-228_Bq/kg_dm: Uncertainty for Ra-228 concentration.
  - Unc_K-40_Bq/kg_dm: Uncertainty for K-40 concentration.
  - Note: For some isotopes, multiple components are indicated (e.g., 1, 2, 3) to distinguish different uncertainty aspects or context (e.g., equilibrium considerations).

- Detection limits
  - Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929 method), on a dry mass basis.
  - Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929 method), on a dry mass basis.
  - Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929 method), with possible sub-components.
  - Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929 method), on a dry mass basis.
  - Notes indicate detection limits may include contextual qualifiers (e.g., equilibrium with other isotopes).

- Data-availability cue
  - Where fields are blank, the concentration is below the detection limit.

## Units and formats

- Concentrations: Bq/kg dry mass (Bq/kg_dm).
- Sample size: kg fresh mass.
- Collection_Date format: dd-mm-yyyy.
- Some columns list sub-items (e.g., 1, 2, 3) to denote components or contexts (such as equilibrium relationships); blanks indicate non-applicable or not measured.

## Interpretation notes

- Equilibrium relationships referenced (e.g., Pb-214 and Bi-214 in equilibrium with Ra-226; Ac-228 in equilibrium with Ra-228) affect interpretation of the activity data.
- Blank values for activity or uncertainty indicate measurements below the detection limit.
- Data should be interpreted in the context of dry mass normalization and the specified isotope relationships.

## How this supports data use (Data Support perspective)

- Enables clear understanding of what each field represents, supporting data quality assurance and transformation into user-friendly outputs (dashboards, pivot tables, reports).
- Facilitates re-use by providing consistent units, formats, and explicit notes about detection limits and equilibrium conditions.
- Highlights data quality considerations relevant to broader teams (e.g., patchy data, formatting inconsistencies) and how blanks should be treated in analysis.
- Supports end users in self-serve analysis by documenting measurement scope, uncertainty components, and limits of detection, enabling informed decision-making and traceability.