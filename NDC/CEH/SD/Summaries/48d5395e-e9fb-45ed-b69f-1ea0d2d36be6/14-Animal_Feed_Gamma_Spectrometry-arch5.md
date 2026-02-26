# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Overview
- Provides variable-level descriptions for a dataset of gamma spectrometry results in animal feed.
- Focuses on activity concentrations of radionuclides per kilogram of dry matter (Bq/kg_dm): Ra-226, Cs-137, Ra-228, and K-40.
- Includes associated uncertainties (Unc_*) and detection limits (Detection_Limit_*) for each radionuclide.
- Notes physical relationships and measurement caveats, such as equilibrium with decay products and how blanks are used to indicate non-detections.

## Dataset Schema and Variables

- Animal
  - Explanation: General type of animal.
  - Notes: N/A for units or further details.
- Location
  - Explanation: Location where the sample was collected.
  - Notes: N/A for units or details.
- Feeding
  - Explanation: Description of the feeding regime.
  - Notes: N/A for units or details.
- Ra-226_Bq/kg_dm
  - Explanation: Activity concentration of Ra-226 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Pb-214 and Bi-214; blank indicates concentration below detection limit.
- Unc_Ra-226_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Ra-226 concentration.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Pb-214 and Bi-214.
- Detection_Limit_Ra-226_Bq/kg_dm
  - Explanation: Detection limit for Ra-226 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Pb-214 and Bi-214; blank indicates below detection limit.
- Cs-137_Bq/kg_dm
  - Explanation: Activity concentration of Cs-137 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates below detection limit.
- Unc_Cs-137_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Cs-137 concentration.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates below detection limit.
- Detection_Limit_Cs-137_Bq/kg_dm
  - Explanation: Detection limit for Cs-137 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates concentration above the detection limit.
- Ra-228_Bq/kg_dm
  - Explanation: Activity concentration of Ra-228 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Ac-228; blank indicates below detection limit.
- Unc_Ra-228_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of Ra-228 concentration.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Ac-228.
- Detection_Limit_Ra-228_Bq/kg_dm
  - Explanation: Detection limit for Ra-228 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: In equilibrium with Ac-228; blank indicates below detection limit.
- K-40_Bq/kg_dm
  - Explanation: Activity concentration of K-40 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates below detection limit (textually aligned with other fields; the line appears to describe detection limits similarly).
- Unc_K-40_Bq/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of K-40 concentration.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates below detection limit.
- Detection_Limit_K-40_Bq/kg_dm
  - Explanation: Detection limit for K-40 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass.
  - Notes: Blank indicates concentration above the detection limit.

> Note: The section for K-40 contains a wording anomaly where the explanation line references Ra-228, which appears to be a copy/paste error. The intended meaning is the activity concentration of K-40 in the total diet on a dry mass basis, with corresponding uncertainty and detection limit fields.

## Data Quality and Interpretation

- Units consistency: All radionuclide concentrations are in Bq/kg dry mass.
- Non-detections: Blank values indicate concentrations below the detection limit for the respective field; detection limits are provided per radionuclide.
- Uncertainties: Unc_* fields capture propagated measurement uncertainty (quadratic propagation) for the concentration estimates.
- Equilibrium notes: Some isotopes are described as being in equilibrium with decay products (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228), which can influence interpretation of related measurements.
- Measurement context: Location, Animal, and Feeding fields provide metadata to contextualize results.

## Metadata and Documentation

- The document serves as supporting metadata for the 14-Animal_Feed_Gamma_Spectrometry.csv dataset, enabling consistent interpretation, quality assurance, and data discovery.
- Clear definitions of each field, units, and detection-limit semantics aid data governance and reuse.

## Governance and Compliance Considerations

- Ensure metadata are kept up to date and aligned with data collection protocols and measurement methods.
- Validate the presence and consistency of detection limits and uncertainty values, especially when blanks occur.
- Maintain provenance: reference measurement methods, calibration, and any data transformations applied before sharing.
- Prepare for data sharing by ensuring fields are clearly described in data catalogs and portals, with notes on handling non-detections and equilibrium relationships.

## Known Issues / Anomalies

- Potential inconsistency in the K-40 section where the explanatory text erroneously mentions Ra-228. Flag for correction to ensure metadata accuracy.
- Blanks and detection-limit semantics should be consistently applied across all radionuclide fields.

## Recommendations for Data Stewards

- Confirm and, if needed, correct the K-40 explanatory text to reflect K-40 as the subject of that field.
- Enforce uniform handling of non-detects: blanks should be interpreted as below detection limit with appropriate downstream imputation or reporting in analyses.
- Document the measurement protocol and detection-limit calculation method to support traceability and reuse.
- Include provenance and versioning for the dataset and metadata to support discovery and governance across large datasets.