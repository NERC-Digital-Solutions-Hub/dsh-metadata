# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- A data dictionary/schema for ICP-MS measured concentrations of multiple elements in bee samples from Northumbria.
- Captures both sample metadata and per-sample element concentrations (in mg/kg fresh mass).
- Designed to support environmental health monitoring, giving policymakers and program managers the data needed to assess exposure, compare sites/times, and inform future decisions.
- Indicates use of UK Centre for Ecology & Hydrology (UKCEH) sample codes and descriptions, with fields for notes and sample details.

## Data schema (core fields)

- Latin_Species_Name: Taxonomic scientific name.
- Common_Species_Name: Common name of the species.
- Site: Sampling location.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Codes: UKCEH sample codes.
- CEH_Sample_Description: Description of the UKCEH sample.
- Sample_Details: Additional details about the sample.
- Notes: Notes on bees.
- I_mg_kg_FM: Concentration of Iodine (I) in mg/kg fresh mass.
- Li_mg_kg_FM: Concentration of Lithium (Li) in mg/kg fresh mass.
- Be_mg_kg_FM (and <Be_mg_kg_FM): Beryllium concentration in mg/kg fresh mass; "<" marker indicates a below-threshold value.
- Na_mg_kg_FM: Sodium concentration (mg/kg FM).
- Mg_mg_kg_FM: Magnesium concentration (mg/kg FM).
- Al_mg_kg_FM: Aluminum concentration (mg/kg FM).
- P_mg_kg_FM: Phosphorus concentration (mg/kg FM).
- K_mg_kg_FM: Potassium concentration (mg/kg FM).
- Ca_mg_kg_FM: Calcium concentration (mg/kg FM).
- Ti_mg_kg_FM: Titanium concentration (mg/kg FM).
- V_mg_kg_FM: Vanadium concentration (mg/kg FM).
- Cr_mg_kg_FM: Chromium concentration (mg/kg FM).
- Mn_mg_kg_FM: Manganese concentration (mg/kg FM).
- Fe_mg_kg_FM: Iron concentration (mg/kg FM).
- Co_mg_kg_FM: Cobalt concentration (mg/kg FM).
- Ni_mg_kg_FM: Nickel concentration (mg/kg FM).
- Cu_mg_kg_FM: Copper concentration (mg/kg FM).
- Zn_mg_kg_FM: Zinc concentration (mg/kg FM).
- As_mg_kg_FM: Arsenic concentration (mg/kg FM).
- Se_mg_kg_FM (and <Se_mg_kg_FM): Selenium concentration in mg/kg FM; "<" indicates below-threshold value.
- Rb_mg_kg_FM: Rubidium concentration (mg/kg FM).
- Sr_mg_kg_FM: Strontium concentration (mg/kg FM).
- Mo_mg_kg_FM: Molybdenum concentration (mg/kg FM).
- Ag_mg_kg_FM: Silver concentration (mg/kg FM).
- Cd_mg_kg_FM: Cadmium concentration (mg/kg FM).
- Cs_mg_kg_FM: Cesium concentration (mg/kg FM).
- Ba_mg_kg_FM: Barium concentration (mg/kg FM).
- Tl_mg_kg_FM: Thallium concentration (mg/kg FM).
- Pb_mg_kg_FM: Lead concentration (mg/kg FM).
- U_mg_kg_FM (and <U_mg_kg_FM): Uranium concentration (mg/kg FM); "<" indicates below-threshold value.

- Note: All concentration values are reported as mg/kg fresh mass (FM). Some fields include a less-than marker to denote detected below-threshold values. Several fields include "n/a" placeholders where data is not applicable or not provided.

## Units, interpretation, and data notes

- Primary unit for concentrations: mg/kg fresh mass.
- Some fields include placeholders (n/a) or explanatory text to describe the field purpose.
- "<" values indicate concentrations below reporting/limits of detection for Be, Se, U, etc.
- Metadata and sample descriptors (Site, Date_Sample_Collected, CEH codes) enable temporal and spatial analysis across sites.

## Data quality, metadata, and governance considerations

- Metadata accessibility: Some fields rely on external originators or additional metadata to be fully verifiable.
- Data sharing expectations: The structure is designed to support public sharing of underlying data, consistent with data governance and openness standards.
- Data cleaning and transformation: Raw data may require cleaning, standardization, and transformation prior to analysis; some fields contain inconsistent or incomplete metadata.
- Data completeness: There may be gaps (e.g., placeholder n/a) that could affect cross-site or longitudinal comparisons.
- Data silos and access: As a monitoring framework artifact, integrating this dataset with other datasets may require harmonization to avoid silo effects.
- Source and provenance: CEH_Sample_Codes and descriptions indicate source provenance; ensuring traceability to originators supports data quality and reuse.

## How this supports monitoring frameworks

- Provides a comprehensive, standardized set of variables to monitor environmental exposure of bees to a broad suite of elements.
- Enables:
  - Comparative analysis across sites and collection dates.
  - Trend analysis to inform policy evaluation and decisions.
  - Integration with other bioindicator and environmental datasets (species, site, timing, notes).
- Supports transparent reporting through clear data fields and explicit measurement units.

## Practical considerations for implementation and use

- Ensure complete metadata coverage (species, site, date, sample IDs) to maximize interpretability.
- Develop clear data governance processes for data sharing, storage, versioning, and provenance.
- Establish procedures for handling "<" values and censored data in analyses.
- Promote data harmonization to mitigate silos and facilitate cross-program comparisons.
- Plan for regular metadata enrichment to address n/a fields and improve verification of data quality.