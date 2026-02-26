# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Overview
- Documents the fields and meanings of the 04-Soil_Gamma_Spectrometry.csv dataset.
- Focuses on soil gamma spectrometry measurements for environmental monitoring.
- Includes sample metadata, radioisotope activity concentrations, uncertainties, detection limits, and related notes.
- Measurements are primarily reported on a dry mass basis and aligned with standard reporting formats to aid data governance and comparability.

## Key fields and definitions
- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: Soil.
  - Location: Name of the sampling location.
  - Sample_Description: Further details (e.g., soil at depth 0-10 cm).
  - Collection_Date: Date of collection (format: dd-mm-yyyy).
  - Sample_size: Amount of sample analyzed (Kg dry matter).

- Isotope activity concentrations (all on a dry mass basis)
  - Ra-226_Bq/kg_dm: Activity concentration of Ra-226.
  - Unc_Ra-226_Bq/kg_dm: Uncertainty for Ra-226.
  - Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (ISO 11929 method).

  - Cs-137_Bq/kg_dm: Activity concentration of Cs-137.
  - Unc_Cs-137_Bq/kg_dm: Uncertainty for Cs-137.
  - Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (ISO 11929).

  - Ra-228_Bq/kg_dm: Activity concentration of Ra-228.
  - Unc_Ra-228_Bq/kg_dm: Uncertainty for Ra-228.
  - Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (ISO 11929).
  - Note: Ra-228 is in equilibrium with Ac-228.

  - K-40_Bq/kg_dm: Activity concentration of K-40.
  - Unc_K-40_Bq/kg_dm: Uncertainty for K-40.
  - Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (ISO 11929).

- Equilibrium references and detection notes
  - Some isotopes include notes such as “In equilibrium with Pb-214 and Bi-214” (Ra-226), or “In equilibrium with Ac-228” (Ra-228).
  - Where concentration fields are blank, the value indicates a concentration below the detection limit.
  - Detection limits are calculated according to ISO 11929.

## Isotopes and measurement context
- Ra-226, Cs-137, Ra-228, and K-40 are measured for soil samples at shallow depth (0-10 cm) to assess radiological contamination and natural background levels.
- All activity concentrations are expressed as Bq per kilogram of dry matter (Bq/kg_dm).
- Depth-specific sampling is noted in sample descriptions.

## Data quality, detection limits, and governance notes
- Uncertainties accompany each measured activity concentration to quantify measurement precision.
- Detection limits follow ISO 11929 methodology, ensuring standardized reporting thresholds.
- Equilibrium assumptions (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228) influence interpretation of related isotopes.
- Blank values indicate non-detects; partial or inconsistent metadata may require reference to data originators.
- Public sharing of underlying data is an anticipated governance consideration, consistent with broader data openness goals and data management standards.

## Implications for Monitoring Frameworks
- Provides a standardized schema for recording soil gamma spectrometry results, promoting consistency across monitoring programs.
- Supports transparency and reproducibility through explicit metadata, uncertainties, and detection limits.
- Facilitates data integration, governance, and decision-making by clarifying unit definitions, depth context, and equilibrium relationships.
- Helps identify potential data gaps (e.g., missing metadata, non-detects) and informs strategies to address silos and data access challenges in environmental monitoring.