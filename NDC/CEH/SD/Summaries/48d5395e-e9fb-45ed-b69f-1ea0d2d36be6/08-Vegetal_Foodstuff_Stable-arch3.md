# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

## Purpose and scope
- Provides metadata and variable definitions to accompany a dataset on stable element concentrations in vegetal foodstuffs, enabling policy scrutiny, evaluation, and informing future decisions.

## Dataset structure and metadata fields
- Sample metadata:
  - Sample_Code, Location, Sample_Type, Sample_Description, Collection_Date (dd-mm-yyyy), Sample_size (g fresh matter or mL for olive oil and wine).
- Data formatting and units:
  - Results are on a dry mass basis (mg/kg_dm) for most analytes; for olive oil and wine, units may be mg per litre or related field variants.
  - The document specifies date formats and general field expectations; some unit/labeling inconsistencies are present in the draft.

## Analytes and measurement variables
- Analytes covered: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th.
- For each analyte:
  - Concentration field (e.g., Cs_mg/kg_dm).
  - Uncertainty field (e.g., Unc_Cs_mg/kg_dm).
  - Detection limit field (e.g., Detection_Limit_Cs_mg/kg_dm).
  - Notes indicate that if a concentration is below the detection limit, the value may be blank.
- The documentation aligns concentrations with combined uncertainties and detection limits, facilitating transparent reporting of nondetects.

## Data quality, completeness, and governance
- Emphasizes data quality assurance, cleaning, transformation, and clear presentation (reports, charts, dashboards).
- Highlights data governance considerations: openness and sharing of underlying data, and setting data management standards at the source.
- Acknowledges potential barriers relevant to monitoring frameworks, including data access, metadata adequacy, data silos, and the effort required to transform data for use.

## Practical considerations for use
- Ensure consistent field definitions and units across samples.
- Be mindful of date formatting and matrix-specific units (e.g., olive oil and wine).
- Address formatting issues in the draft to support reliable automated ingestion; treat below-detection-limit values appropriately.

## Relevance for monitoring framework authors
- Establishes a standardized, transparent schema for reporting environmental health indicators in vegetal foods.
- Enables comparability across samples and matrices, with explicit recording of uncertainty and detection limits.
- Supports data governance and openness, aiding stakeholder consultation and policy-informed decision-making.