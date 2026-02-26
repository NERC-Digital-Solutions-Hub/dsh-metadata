# Supporting documentation for Stable_concentration_means.csv

- The document provides a data dictionary and metadata schema for the Stable_concentration_means.csv dataset.
- It defines how sample data are identified, described, and quantified, enabling consistent ingestion, interpretation, and reuse.

## Purpose and scope
- Establishes unique identifiers for samples (Sample_Code) and specimen details (Species, RAP, Sample_Description).
- Documents that the dataset stores mean concentrations (Mean_Value) of multiple elements/metals in samples, with corresponding measures of dispersion.
- Indicates whether means are geometric or arithmetic and how standard deviations are interpreted.

## Core data model and fields
- Key identifiers:
  - Sample_Code: Unique sample identifier.
  - Species: Latin name of the sampled species.
  - RAP: ICRP Reference Animals and Plants attribution.
  - Sample_Description: Part of the sample analysed.
- Measurement fields:
  - Mean_Value: Mean concentration value (geometric or arithmetic as identified).
  - For each element (e.g., I-127_mg_kg, Li_mg_kg, Be_mg_kg, B_mg_kg, Na_mg_kg, Mg_mg_kg, Al_mg_kg, P_mg_kg, S_mg_kg, K_mg_kg, Ca_mg_kg, Ti_mg_kg, Mn_mg_kg, Fe_mg_kg, Co_mg_kg, Ni_mg_kg, Cu_mg_kg, Zn_mg_kg, As_mg_kg, Se_mg_kg, Rb_mg_kg, Sr_mg_kg, Mo_mg_kg, Ag_mg_kg, Cd_mg_kg, Cs_mg_kg, Ba_mg_kg, Pb_mg_kg, U_mg_kg):
    - Corresponding Standard_Deviation_<element>_mg_kg: Standard deviation (fresh weight basis) for the element.
- Notes accompany many fields to clarify interpretation and data type (geometric vs arithmetic).

## Units and measurement details
- Concentrations expressed on a fresh weight basis.
- Units for concentration fields are milligrams per kilogram (mg/kg).
- Mean_Value is labeled as geometric or arithmetic per record, with standard deviations aligned accordingly.
- Some lines include notes that clarify interpretation, though there are formatting inconsistencies in parts of the text.

## Metadata and provenance
- RAP field links sample data to ICRP Reference Animals and Plants, enabling cross-dataset comparability and broader ecological or radiological context.
- Sample_Description provides context on the portion of the sample analysed, aiding reproducibility and traceability.

## Data quality and constraints
- The schema aims for consistency across numerous elements, enabling reliable data ingestion and comparison.
- Potential quality concerns highlighted by the document:
  - Occasional formatting irregularities and truncated lines (could affect parsing and automated ingestion).
  - Some field descriptions or mappings appear incomplete or inconsistent, requiring data governance and validation updates.
- Recommendations to strengthen quality:
  - Standardize field names and ensure complete, unambiguous metadata for all elements.
  - Validate that Mean_Value and its associated Standard_Deviation fields are consistently labeled as geometric or arithmetic.
  - Implement data validation rules to catch and correct formatting inconsistencies.

## Data access, reuse and governance
- The documented schema supports discoverability and reuse by enabling clear interpretation of sample metadata, measurement values, and units.
- Alignment with RAP and ICRP references indicates an intent to integrate with cross-sector data networks and standards.
- For data leaders, key governance actions include maintaining metadata completeness, enforcing schema conformity in pipelines, and coordinating with cross-network communities of practice to reduce duplication and improve data quality.

## Implications for Data Leaders (archetype-oriented)
- Focus on end-to-end data stewardship: ensure the data dictionary is complete, consistent, and parsable to support scalable data products.
- Prioritize standardization of units, mean types, and dispersion measures to enable aggregation and cross-study comparisons.
- Maintain robust metadata around sampling context, species attribution (RAP), and sample description to enable co-ownership and broader utility of data products.
- Invest in data quality controls to address formatting inconsistencies and ensure reliable data discovery and reuse across networks.