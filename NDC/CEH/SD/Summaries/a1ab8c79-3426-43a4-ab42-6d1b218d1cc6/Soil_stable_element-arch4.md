# Supporting documentation for Soil_Stable_Element.csv

## Overview
- Provides metadata and data dictionary for the Soil_Stable_Element.csv dataset.
- Documents sample identifiers, sample type and description, collection date, and per-element concentration data with associated detection limits.
- Designed to support data discovery, quality assessment, and reuse across data teams and partners.

## Data structure and fields
- Sample metadata
  - Sample_Code: unique sample identifier.
  - Sample_Type: type of sample.
  - Sample_Description: additional explanation; note that RCN119, 120, and 121 are replicate soil samples.
  - Collection_Date: date of sample collection (format: dd month yyyy).
  - Units (for relevant fields): general concentration units are mg/kg_dw (dry mass basis); some description fields reference centimetres where applicable.

- Per-element data (concentrations on a dry mass basis)
  - I-127_mg_kg_dw, Li_mg_kg_dw, Be_mg_kg_dw, B_mg_kg_dw, Na_mg_kg_dw, Mg_mg_kg_dw, Al_mg_kg_dw, P_mg_kg_dw, S_mg_kg_dw, K_mg_kg_dw, Ca_mg_kg_dw, Ti_mg_kg_dw, V_mg_kg_dw, Cr_mg_kg_dw, Mn_mg_kg_dw, Fe_mg_kg_dw, Co_mg_kg_dw, Ni_mg_kg_dw, Cu_mg_kg_dw, Zn_mg_kg_dw, As_mg_kg_dw, Se_mg_kg_dw, Rb_mg_kg_dw, Sr_mg_kg_dw, Mo_mg_kg_dw, Ag_mg_kg_dw, Cd_mg_kg_dw, Cs_mg_kg_dw, Ba_mg_kg_dw, Tl_mg_kg_dw, Pb_mg_kg_dw, U_mg_kg_dw.
  - Detection_Limit_<element>_mg_kg_dw: corresponding detection limit for the given sample (units: mg/kg_dw).

- Notes on data semantics
  - If the concentration field for an element is blank, the concentration is below the detection limit.
  - If the detection-limit field is blank, the concentration is detectable (i.e., not censored at that limit).
  - Some entries include qualifiers in the notes (e.g., reference to “given sample” or replication context).

- Replicates
  - Replicate samples are indicated (e.g., RCN119, 120, 121) within Sample_Description.

## Measurement units and data semantics
- Concentrations are reported on a dry mass basis (mg/kg_dw).
- Detection limits accompany each element to support censoring-aware analyses.
- The dataset emphasizes clear provenance and metadata to facilitate appropriate interpretation and reuse across projects.

## Replicates and provenance
- Replicate samples are explicitly identified in the sample description.
- CollectionDate provides temporal context for each sample set.
- The structure supports traceability from sample codes through to per-element measurements and detection limits.

## Data quality and governance considerations
- Inclusion of per-sample detection limits enables proper handling of censored data.
- The metadata schema supports discoverability and interoperability with other data assets (consistent units, clear field mappings).
- Some textual formatting in the source shows variations or parsing artifacts; the intended model is standardized mg/kg_dw with corresponding detection limits per sample.

## Practical implications for data strategy (Data Leaders)
- Data ingestion and ETL
  - Use the dictionary to map incoming data to standardized fields: sample metadata plus per-element concentration and detection-limit columns.
  - Implement censoring-aware logic: treat blank concentrations as below detection limit; non-blank with a detection limit present indicates censored data at that limit.

- Metadata governance
  - Ensure complete capture of Sample_Code, Sample_Type, Sample_Description (including replicate notes), and Collection_Date.
  - Maintain and propagate detection-limit fields alongside concentrations for robust analyses.

- Analytical planning and collaboration
  - Align partners on unit conventions (mg/kg_dw) and the meaning of detection limits.
  - Use replicate notes to assess measurement consistency and to calibrate cross-site comparisons.

- Data quality and reuse
  - Leverage detection-limit metadata to properly model censored observations in downstream analyses.
  - Prioritize data quality checks around fields with inconsistent or garbled notes to restore consistent interpretation across the full element list.